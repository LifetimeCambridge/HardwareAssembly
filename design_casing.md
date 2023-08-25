
[Perspex panels]:materials
[Aluminium extrusion pieces]:materials
[M4 Rubber Surrounded Feet]:materials
[L-bracket]:materials
[S6 cube connectors]:materials

[Bosch Rexroth M4 t-slot nuts]:mechcomp
 [9mm M4 threaded rod]:mechcomp
 [8mm M4 bolts]:mechcomp
[M4 nuts]:mechcomp
[6.5mm spacers]:mechcomp
[M3 20mm bolts]:mechcomp
[M3 nuts]:mechcomp
[D12 cover caps]:mechcomp
 [S6 bolts]:mechcomp
 [40mm M4 bolts]:mechcomp
[M4 washers]:mechcomp
[Plastic washers]:mechcomp

[Rubber mallet]:tools
[Laser cutter]:tools

# Casing assembly
This set of guidelines guides the fabrication and assembly of the casing required to build the oepn-source battery cycler with eight slots. The technology used for fabrication is laser cutting. Hence, all files are in the .dfx format.

{{BOM}}

# Files
All of the .dfx files are included in the following 


# Design
The casing is designed with modularity in mind. Hence, simple metal extrusions are used as a base frame for the casing. Acrylic plates then can be slid into the extrusions. The plates contain openings for wiring and the battery cycler slots. 

# Assembly
## Cut aluminium extrusions {pagestep}
* Cut the [Aluminium extrusion pieces]{Qty: 12, cat:'Materials', Note: 'Pieces of varying lengths, 20x20mm with 6mm grooves.  We used 2 x Bosch Rexroth Silver Aluminium Profile Strut, 20 x 20 mm, 6mm Groove, 3000mm Length (3842992888/3000) '} to size. Pieces with the following lengths are required: 4 x 412mm, 4 x 272mm, and 4 x 212mm.

![](images/Case_assembly_1.png)

## Laser-cut erspex panels {pagestep}
* Cut [Perspex panels]{Qty: 6, cat:'Materials', Note: 'Thickness  5mm, any colour (preferably black). Size: large enough to make 2 x 420mm x 280mm pieces (front/back), 2 x 420mm x 220mm pieces(base/top), and 2 x 280mm x 220mm pieces (sides).  We used Hobarts 5.0MM BLACK PERSPEX® CAST ACRYLIC (AC.BLK0962.05.6040) 3 x 600mm x 400mm sheets and 2 x 600mm x 300mm sheets (both sides cut on 1 sheet.'} panels with a [Laser cutter]{Qty:1, cat:'tools'}, using the provided .dfx files.
* In total, five distinct parts shall be cut out, where the base parts are cut out twice.


![](images/Case_assembly_2.png)

## Create base {pagestep}

* Select 4 pieces of [Aluminium extrusion pieces] for the base frame (2 x 414mm and 2 x 214mm). 
* Connect two [M4 Rubber Surrounded Feet]{Qty: 4,  cat:'Materials', Note: 'We used FIBET Cylindrical M4 Anti Vibration Mount, Female Buffer Foot with 16.2kg Compression Load (1610DE04-45).'} 10mm from each end of the two longest pieces using a [Bosch Rexroth M4 t-slot nuts]{Qty: 2} and a piece of [9mm M4 threaded rod]{Qty: 2} for each foot. 
* Then, assemble three pieces of the base frame with the [S6 cube connectors]{Qty:4, cat:'Materials', Note:'We used Bosch Rexroth S6 Cube Connector Connecting Component, Strut Profile 20 mm, Groove Size 6mm (3842549861), which came with bolts and caps (see mechanical components).'} and [S6 bolts]{Qty:8} (you may need to tap the extrusion into the corner connectors with a [Rubber mallet]{qty:1, cat:'tools'}. 

![](images/Case_assembly_3.png)


## Slide in base panel and fasten {pagestep}
* Slide the base panel into the frame.
* Attach the fourth piece of extrusion to close this part of the frame (using the [S6 bolts]).  

![](images/Case_assembly_4.png)

## Screw to power board and power supply to the base {pagestep}
* Connect the power board to the base with 3 [8mm M4 bolts]{Qty: 3}, 3 [M4 nuts]{Qty:3}, and 3 [6.5mm spacers]{Qty:3}.
* Wire the power supply and mount to the base using 4 [8mm M4 bolts]{Qty:4}.  

![](images/Case_assembly_5.png)

## Assemble components for front panel {pagestep}
* Bolt the (dis)charge PCBs to the front panel with [M3 20mm bolts]{Qty:16} and [M3 nuts]{Qty: 32}. 
* Mount the IO-board to the [L-bracket] with [Plastic washers]{Qty:2} between board and bracket, use 2 [M3 20mm bolts]{Qty:2} and 2 [M3 nuts]{qty:2}. 
* Mount the [L-bracket]{Qty: 1,  cat:'Materials', Note: 'We cut a piece of aluminium extrusion with an L-cross-section to length of IO board an drilled 4 x M3 holes ino it.'} to the front panel using 2 [M3 20mm bolts]{Qty:2} and 2 [M3 nuts]{Qty:2}. 
* Mount the LCD screen with 2 [M3 nuts]{Qty:2} and [M3 20mm bolts]{Qty:2}.
* Attach button, buzzer, rotary encoder, and temperature sensor to the front panel, using glue.  

![](images/Case_assembly_6.png)

## Attach fans {pagestep}
* Bolt the fans to the side panels using 8 [40mm M4 bolts]{Qty:8}, 8 [M4 washers]{Qty:8}, and 8 [M4 nuts]{Qty:8}. 

>i **Note**
>i
>i Take care to attach them as shown in the picture to ensure air flow (bottom of air fan to left side, top of fan to left side).


![](images/Case_assembly_7.png)

## Attach the control board and socket {pagestep}

* Bolt the socket to the back panel using 2 [M3 20mm bolts]{Qty: 2} and 2 [M3 nuts]{Qty: 2}. 
* Bolt the control board to the back panel using four [M3 20mm bolts]{Qty:4}, four [M3 nuts]{Qty:4} and 4 [6.5mm spacers]{Qty:4}.

![](images/Case_assembly_8.png)

## Assemble vertical extrusions and panels {pagestep}
* Secure the four shortest [Aluminium extrusion pieces] perpendicularly to the base frame, using [S6 bolts]{Qty:8} . 
* Then, slide front, back and side panels into the frame. 

![](images/Case_assembly_9.png)

## Wire everything else up {pagestep}

## Seal the box {pagestep}
* Secure three of the remaining [Aluminium extrusion pieces] to the top of the frame, using [S6 bolts]{Qty:8}. Then, slide the top panel into the frame and secure the two final [Aluminium extrusion pieces].

![](images/Case_assembly_11.png)

## Check that box is stable {pagestep}
*  Check all the screws are secure. Attach [D12 cover caps]{Qty: 24, Note:'We used the ones in the connector kits (3842517132)'} if you have them (optional). Note: we manufactured only 2 (dis)charge PCBs when building this prototype. 



![](images/Case_assembly_12_back.png)
![](images/Case_assembly_12_corner.png)
![](images/Case_assembly_12_front.png)
![](images/Case_assembly_12_side.png)


