[No. 2 Phillips screwdriver]:Parts.yaml#Screwdriver_Philips_No2
[Inkjet Printer]: tool.yaml#printer
[UV Box]:tool.yaml#UVbox
[Copper Board]:tool.yaml#copperboard
[Alkaline Solution (NaOH)]:chemical.yaml#NaOH
[Ferric Chloride (Fe(III)Cl3)]:chemical.yaml#fecl3
[Tongs]:tool
[Tinning Solution]:chemical.yaml#tinn
[Drill]:tool
[Green Protective Coating]:tool
# PCB Fabrication
## Power Distribution Board

{{BOM}}

## Create photomask {pagestep}

* Print photomask onto a plastic sheet using an [Inkjet Printer]{Qty: 1, Cat: tool}. Wait until the ink is dry (about an hour).

![](images/Picture1.jpg)

## Insert into UV printer {pagestep}

* Cut out the outline of the board.
* Place the outline into the [UV Box]{Qty: 1, Cat: tool} with the ink side facing up. 

![](images/Picture2.jpg)

## Prepare for curing {pagestep}

* Dark room required.
* Peel the protective layer of the plastic from the [Copper Board]{Qty:1}, exposing the photoresist. 
* Align the board with the photomask and place face down in the [UV box]. 


![](images/Picture3.jpg)


## UV exposure {pagestep}

* Expose the board to UV light for two and a half minutes. 


![](images/Picture4.jpg)



## Wash off photoresist {pagestep}
* Take the board out from the [UV box].
* Immerse it in [Alkaline Solution (NaOH)]{Qty:1, Cat: chemical} to wash off the photoresist. 
* Gently rock the container until the pattern appears on the surface of the board. This may take several minutes. 
* Quickly rinse the board under water to rinse off chemicals, using [Tongs]{Qty: 1, Cat: tool}. Then, dry the board. 


![](images/Picture5.jpg)



## Cutting {pagestep}
* Cut the board to its correct size.

![](images/Picture6.jpg)


## Etching {pagestep}
* Place the board inside [Ferric Chloride (Fe(III)Cl3)]{Qty: 1, Cat: chemical}, apply heat and constant stirring, which will etch away unwanted copper.

>! **Caution**
>!
>! Ferric Chloride is toxic, so keep the container closed at all times.

* Etch for 20 minutes or until all the exposed copper is washed away.

![](images/Picture7.jpg)


* Turn the board over 10 minutes into the etching.
* Wash the board under water, remebering to use [Tongs]. 

![](images/Picture8.jpg)


## Further exposure {pagestep}
* Place the board back into the [UV box], facing down, and expose to UV light for 10 minutes.

![](images/Picture9.jpg)


* Then, reimmerse in alkaline solution to wash off the photoresist whilst gently rocking the container.
* On the image, the washed off black layer is visible, leaving behind the pink copper layer.

![](images/Picture10.jpg)


* Use fine sandpaper to clean the surface, exposing the pink copper tracks. 

![](images/Picture11.jpg)



## Tinning {pagestep}
* Put [Tinning Solution]{Qty: 1, Cat: chemical} into a container.

![](images/Picture12.png)


* Place the board inside the tinning solution, using [Tongs]. The pink copper turns shiny as tin is deposited onto it. This layer protects the traces from oxidation.

![](images/Picture13.jpg)


* Then, rinse under water and dry off.

![](images/Picture14.jpg)



## Troubleshooting tinning {pagestep}
* Cracks may appear on the tracks, which will block the flow of current.

![](images/Picture15.jpg)


* The tracks are fixed by putting Solder with flux across the breaks, then wash off the flux.

![](images/Picture16.jpg)


## Drilling {pagestep}
* The power distribution board contains different sized holes from 0.8 to 2.6mm diameter, which were created using a [Drill]{Qty: 1, Cat: tool}.

![](images/Picture17.jpg)


* After drilling, sand and tin the board again.

![](images/Picture18.jpg)


## Protective coating {pagestep}
* Finally, spray the PCB with [Green Protective Coating]{Qty: 1, Cat: chemical}. Leave to dry overnight.

![](images/Picture19.jpg)


* The board is now finished. 

![](images/Picture20.jpg)


