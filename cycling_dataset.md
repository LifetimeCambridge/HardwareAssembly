# Creating a cycling dataset
The LiFETIME battery cycler performs constant current (CC) charging. This means that a constant current is injected into the battery, and the resulting cell potential is read out. The potential is measured across the two terminals of the battery, and varies with state of charge of the battery. 

## Starting up the device {pagestep}

## Defining cut-off cell potentials for each cell {pagestep}

* In order to perform charging within the specifications of the battery, its lower and upper cut-off voltages for charging must be determined:
* The lower cut-off voltage defines the state-of-charge at which the battery is sufficiently depleted. 
* The upper cut-off voltage defines the state-of-charge at which the battery is sufficiently charged. 
* These values are pre-defined in the datasheets of battery cells, and characteristic of the battery chemistry used.  

Alternatively, arbitrary values can be set for the cut-off voltages. This presupposes knowledge of the safety limits of the battery. By observing the curve resulting from charging and discharging the battery, appropriate voltage bands may be established.  

## Setting the charging current for each cell {pagestep}

* The device contains a rotary encoder. This encoder can be set to modify the charging and discharging current. 
* As with the cut-off voltages, safety bands for the charging and discharging currents are generally given in the batteries’ datasheets. In literature, charging currents from C/20 to C/5 are used for ICA analysis. The LiFETIME team uses charging rates of C/5 for ICA analysis. 
* The device supports charging and discharging currents of up to 3A, with 5A being theoretically possible.  

## Defining rest steps for each cell {pagestep}

* The rest step between charging and discharging is crucial for internal processes of the battery and the charging current to settle. A period of 15-30 minutes should be defined.  

## Set desired sampling rate {pagestep}

* The sampling rate for measurements of voltage and current is set using the .config setup file. For the LiFETIME dataset, a sampling rate of 0.1Hz is used during constant charging.  

## Inserting cells into the cycler {pagestep}

* Once the parameters are set, each cell can be inserted into its respective slot, taking care to connect the electrodes in the correct way. 

## Define state of batteries {pagestep}

* The firmware of the device detects batteries that are depleted and cannot be used for cycling anymore.  

## Charge, dwell and discharge {pagestep}

* During this step, the battery charges at its pre-defined rate, includes a rest step of pre-defined duration, and discharges at a pre-defined rate.  

## Read out data of device {pagestep}
* The data is read out onto an SD-card in .csv format.
