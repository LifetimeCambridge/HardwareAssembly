**I/O Board Assembly Instructions**

# Introduction

This document explains how to assemble the I/O board for the Lifetime
device onto stripboard. The schematic is provided so, if you have some
electronics experience, you may wish to simply use that to construct
your own stripboard circuit or PCB. However, an example stripboard
assembly is also shown, which can be replicated for ease of assembly.

<figure id="fig:ioSch">

<figcaption>Schematic of I/O board, also available as a standalone
document for easier viewing.</figcaption>
</figure>

# Stripboard Assembly

![Top of stripboard assembly of I/O board. Pins are labelled, and 'X'
marks where a track has been broken.](res/board_top.jpg){#fig:ioBoardTop
width="\\textwidth"}

![Underside of stripboard assembly of I/O board, showing soldering
connections. Pins are labelled, and 'X' marks where a track has been
broken.](res/board_bottom.jpg){#fig:ioBoardUnderside
width="\\textwidth"}

Transferring the schematic to a stripboard assembly is simply a case of
placing the components in logical locations and soldering them up. If
you decide to do your own layout, try to minimise wire jumps, using the
copper tracks of the stripboard where possible - this will simplify
assembly and make the circuit easier to follow. If you aren't interested
in doing your own layout, you can replicate what we've done, shown in
Figures [2](#fig:ioBoardTop){reference-type="ref"
reference="fig:ioBoardTop"} and
[3](#fig:ioBoardUnderside){reference-type="ref"
reference="fig:ioBoardUnderside"}. We've marked which pin header
connections are which, and where tracks need breaking. To break a track,
ideally you should use a track breaking tool (typically a drill bit
attached to a handle, or some other similar cutting implement). If you
don't have a 'proper' track breaker to hand, you can just as easily use
a small drill bit. The important thing is that there is no copper left
connecting the two sides which are to be broken. We recommend you check
this with a multimeter in continuity mode after breaking a track, to be
sure. When soldering up the circuit, we recommend you construct it in
'sections', rather than putting every component in and soldering
everything in one go. This will make it much easier to diagnose if you
make a mistake.
