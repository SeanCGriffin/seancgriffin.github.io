---
layout: page
title: BurstCube
description: A CubeSat for gravitational waves
img: /assets/img/BurstCube_open.png
importance: 2
category: work
---


BurstCube is a 6U (30 cm x 20 cm x 10 cm) CubeSat. The instrument comprises four CsI(Tl) scintillator crystals read out with arrays of silicon photomultipliers (SiPMs). 
BurstCube's primary sciecne goal is to detect and characterize the electromagnetic counterparts to gravitational waves, namely short gamma-ray bursts (sGRBs).     

In addition to being a member of the BurstCube science team, I am also part of the team that designed and built the instrument. 
My main task on BurstCube is to implement the FPGA interface between the instrument and the instrument flight software (iFSW) running on the flight computer.     

<div class="row">
    <div class="col-sm-4 mt-3 mt-md-0">
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/BurstCube_open.png' | relative_url }}" alt="" title="BurstCube CAD Image"/>
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
    </div>
</div>
<div class="caption">
    CAD image of BurstCube. 
</div>


The BurstCube flight computer is built around the <a href="https://www.spacemicro.com/products/">SpaceMicro CubeSat Space Processor (CSP)</a> which is a space-qualified board built around the Xilinx Zynq SoC platform. 
The Zynq is a combined dual-core ARM processor with configurable FPGA fabric. 
BurstCube has uses two FPGAs (technically three if you count the radio).
The first handles data acquisition from the different detectors and overall instrument control and the generation of housekeeping telemetry (temperatures, currents and voltages, etc.).
The second (which is what I work on) is the Command and Data Handling (C&DH) FPGA. 
This FPGA interface must process data as it arrives from the instrument, binning it into different energy channels and integrating it in time to reduce the overall data volume being sent to ground. 

<div class="row justify-content-sm-center">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/vhdl_sims.PNG' | relative_url }}" alt="" title="VHDL simulations"/>
    </div>
</div>
<div class="caption">
    In this example, I am simulating the FPGA logic that handles defining energy bins for one of the BurstCube datastreams, and then reading them back to verify that they are correct. 

    When the RAM write-enable goes high, some the RAM is loaded (near the yellow line towards the top). Then, at a later point (where the blue markers are) the RAM is read out and into an output register. 
</div>
 



Every project has a beautiful feature showcase page.
It's easy to include images in a flexible 3-column grid format.
Make your photos 1/3, 2/3, or full width.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/BurstCube_open.png' | relative_url }}" alt="" title="example image"/>
    </div>
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/3.jpg' | relative_url }}" alt="" title="example image"/>
    </div>
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/5.jpg' | relative_url }}" alt="" title="example image"/>
    </div>
</div>
<div class="caption">
    Caption photos easily. On the left, a road goes through a tunnel. Middle, leaves artistically fall in a hipster photoshoot. Right, in another hipster photoshoot, a lumberjack grasps a handful of pine needles.
</div>

You can also put regular text between your rows of images.
Say you wanted to write a little bit about your project before you posted the rest of the images.
You describe how you toiled, sweated, *bled* for your project, and then... you reveal it's glory in the next row of images.


<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/6.jpg' | relative_url }}" alt="" title="example image"/>
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/11.jpg' | relative_url }}" alt="" title="example image"/>
    </div>
</div>
<div class="caption">
    You can also have artistically styled 2/3 + 1/3 images, like these.
</div>


The code is simple.
Just wrap your images with `<div class="col-sm">` and place them inside `<div class="row">` (read more about the <a href="https://getbootstrap.com/docs/4.4/layout/grid/">Bootstrap Grid</a> system).
To make images responsive, add `img-fluid` class to each; for rounded corners and shadows use `rounded` and `z-depth-1` classes.
Here's the code for the last row of images above:

```html
<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/6.jpg' | relative_url }}" alt="" title="example image"/>
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/11.jpg' | relative_url }}" alt="" title="example image"/>
    </div>
</div>
```
