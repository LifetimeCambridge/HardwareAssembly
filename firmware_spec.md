
# Firmware Specification
## 1. Introduction
The purpose of this specification document is to lay out the functionality of the firmware implemented
on the Lifetime Battery Health Estimator device. It does not contain the actual source
code (which can be found here: GIT LINK), but rather the logic of the firmware. The firmware is
built around a basic state machine system, with each state being responsible for a logical unit of
the overall device operation. This state machine is described, along with flowcharts outlining the
function of each state.

![](images/Picture1.png)


## 2. State Machine
The firmware is structured around a state machine, where each functional unit of the device is
defined as a state. There are 17 states in all, for the most part executing sequentially. The only
exceptions to this are the ABORT state (which can be entered from any state which sets an error
code), and the REPLACE CELLS state (which can return to the VOLTAGE CHECK state, if the user
indicates that a depleted cell has been replaced with another cell to test). Fig. 1 shows all these
states and their transitions.

### 2.1 States
Each state has an associated flowchart which defines its logic in detail, but a summary of each state is given here.
#### STARTUP
The device enters this state on power-on. It initialises variables and sets up the Bluetooth broadcasting.
#### INSERT CELLS
This state allows the user to input which of the 8 channels they have populated with a cell to test.
#### VOLTAGE CHECK
Part of the pre-test screening of cells. The voltage of each populated channel is measured, and any channels where the voltage is below the defined acceptable minimum are marked as potentially depleted cells.
#### START TRICKLE
Part of the pre-test screening of cells. Turns on a low (trickle) current to cells marked as potentially depleted. This is to determine if the cells can be recovered back to an acceptable voltage.
#### TRICKLE CHARGING
Part of the pre-test screening of cells. Monitors channel voltages as trickle charging is attempted to recover potentially depleted cells. Has a timer after which any cells which haven’t recovered to a minimum acceptable voltage are considered depleted. 
#### POST-TRICKLE DWELL
Part of the pre-test screening of cells. A wait step to determine whether cells have a stable voltage or rapidly deplete charge following the trickle charging stage.
#### POST-TRICKLE VOLTAGE CHECK
Part of the pre-test screening of cells. Channel voltages are measured to determine which cells (if any) have depleted significantly during POST-TRICKLE DWELL; these cells are marked as depleted cells.

#### REPLACE CELLS
A step which shows the user which (if any) channels contain depleted cells and provides them the opportunity to replace them. If they choose to replace any cells, then the pre-screen test is re-run, otherwise they can press the confirm button to proceed with the main testing stage.
#### START CHARGE
Turns on the defined charge current to all populated channels (excluding any determined to be depleted cells).
#### CHARGING
Monitors channel voltages and cuts off charge current to any channel reaching the defined cut-off voltage.
#### POST-CHARGE DWELL
A rest step following the charging step.
#### START DISCHARGE
Begins discharging of populated channels at the defined discharge current (excluding any channels determined to contain depleted cells).
#### DISCHARGING
Monitors channel voltages and stops discharging any channel reaching the defined minimum cell voltage.
#### POST-DISCHARGE DWELL
A rest step following cell discharging.
#### SOH CALCULATION
State of health model evaluates data from charge cycle and calculates a score for each cell.
#### SD WRITE
All measured cell voltage, current, and state of health data is written to the SD card.
#### FINISH
Final state of health data is made available to app via Bluetooth.
