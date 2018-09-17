## Welcome to FabLab Machine Guide

Documentation about FabLab Machine's and Guides how to use them in proper way. https://salmanfarisvp.github.io/fablab-docs/

### Roland Modela MDX-20 3D Milling Machine

![Roland Modela](https://raw.githubusercontent.com/salmanfarisvp/fablab-docs/master/img/modela/main.jpg)

The Roland Modela MDX-20 is a desktop 3D scanning and milling machine that is compatable with many popular 3D CAD software.The machine can be used to mill ABS,a crylic, wood, plaster,styrene foam, chemical wood, wax, and light metals such as aluminum and brass. The Modela Software can accept .STL, .DXF and .MDJ file types , and we can also use Fab Modes to work with these files for milling and scanning .

#### Specifications :

- Maximum Working Area: 203.2 mm (X) x 152.4 mm (Y) x 60.5 mm (Z)
- Maximum Table Load Weight: 1 kg (2.2 lbs)
- Compatible Materials: ABS,acrylic, wood, plaster, styrene foam, chemical wood, wax, plaster, polyacetal, ploycarbonate , Sandomur SS , aluminum, brass
- Weight of Unit: 13.7 kg (30.2 lbs)

![Specifications](https://raw.githubusercontent.com/salmanfarisvp/fablab-docs/master/img/modela/spec.jpg)


#### HOW IT'S WORK (MODELLA MDX 20)....?

<iframe src="https://giphy.com/embed/vguYDhPXW7ZTLj6iCf" width="480" height="270" frameBorder="0" class="giphy-embed" allowFullScreen></iframe>

Modella is like an ordinary 3-Axis CNC machines, Each axis is driven by a stepper motor and the cutting program tells the machine where to go by giving coordinates by G.code to the machine in real time.

The Fab Module software will convert .png image in to a we series of tool paths, these tool paths are defined by their coordinates and G-code. The .png image is a black and white layout of the board, and the black portions will be milled and the white portion is where the copper will be left.
We have two processes in making a PCB, The first one is milling the traces to get the circuit board pattern, and the second is cutting out the board from the base copper clad and For milling traces, we use the **1/64**  inch (0.4mm) bit and for cutting **1/32** (0.8mm) inch bit.i'll examplain all things one by one.

#### SETTING UP THE MACHINE 

1. First Make sure to use some Sacrificial material on top of the bare metal base , it will prevent the damage of bit or the machine’s table.

    ![step1](https://raw.githubusercontent.com/salmanfarisvp/fablab-docs/master/img/modela/step1.jpg)

2. Check the Drilling bit's , first we need mill the trace then cut,and make sure to use the correct bit.when we start to mill trace check the bit because the previous person will cut his board with cutting bit and that will be the default when we start to work.

3. Fix the PCB on top of the Sacrificial layer, better to use a double sided tape

    ![step3](https://raw.githubusercontent.com/salmanfarisvp/fablab-docs/master/img/modela/step3.jpg)

4. For tighten the bit ,first click view then the table should come out and the head will move to the far right,now load the bit you want to use, for milling traces, we use the **1/64** inch bit and for cutting **1/32** inch bit. Now insert the bit and use the Allen key to tighten the screw. Make sure it is tight on both sides.

    ![step2](https://raw.githubusercontent.com/salmanfarisvp/fablab-docs/master/img/modela/step4.jpg)

5. For Move the (0,0) Position click the View mode again.

6. Now Set the X'axis and Y'axis for by clicking on **move to Xmin and Ymin** on the Fab Module.

7. Before starting Milling check your speed and depth settings and the tool position on the fab modules window.

#### PCB FABRICATION

Here we are going to make a FabISP.First Download the Milling and Cutting Schematics here 

1. Trace 
    ![trace](https://raw.githubusercontent.com/salmanfarisvp/fablab-docs/master/img/modela/trace.png)

2. Outline cutout
    ![outline](https://raw.githubusercontent.com/salmanfarisvp/fablab-docs/master/img/modela/outline.png)

We are using **FR-1** Grade PCB.

![copper](https://raw.githubusercontent.com/salmanfarisvp/fablab-docs/master/img/modela/copper.jpg)

open **Fab Modules** by typing `fab` on linux terminal or you can use the online version.
In Fab Module Select **Image(.png)** as Input and **Roland MDX-20 mill(rml)** as ouput Process and Click **make_png_rml** .

![fabmod1](https://raw.githubusercontent.com/salmanfarisvp/fablab-docs/master/img/modela/fabmod1.png)

Now Fab Module will open a new window, and here we need to image for milling by clicking **load.png** , and don't forget to select the **mill trace (1/64)** for milling and click the **make.path** to create path for milling.

![fabmod2](https://raw.githubusercontent.com/salmanfarisvp/fablab-docs/master/img/modela/fabmod2.png)

Now set the 'X'axis and 'Y'axis

First clik the **View** button on the Modela Control panel.

<iframe src="https://giphy.com/embed/1AdZgc5HgWmcNj637V" width="480" height="270" frameBorder="0" class="giphy-embed" allowFullScreen></iframe>

Now change the bit ,For milling we use **1/64** bit.

![64bit](https://raw.githubusercontent.com/salmanfarisvp/fablab-docs/master/img/modela/64bit.jpg)

<iframe src="https://giphy.com/embed/2zZlPjbnyCYcEEYOlQ" width="480" height="270" frameBorder="0" class="giphy-embed" allowFullScreen></iframe>

After tighten the bit, click the **View** button to get back to Home position.

<iframe src="https://giphy.com/embed/1YjoCFA4Jt1o8Q6xIL" width="480" height="270" frameBorder="0" class="giphy-embed" allowFullScreen></iframe>


Now set the Correct X and Y axis based on our PCB board Position.

For setting Z'axis ,set the x and y then by using **UP** and **Down** button just stop the nearby the PCB and then losen the 'Bit' and tight it when it's touch the PCB , that's all we now set the Z axis.

Note :- Don't forget the X and Y axis.if we face any issue like power failure of application forzen we can't start it same postion without the X and Y axis.

Now Click **Make.rml** to genrate instruction after that click **Send it** ! to start Milling.

<iframe src="https://giphy.com/embed/4EFqZyy4xbS4fZQQjF" width="480" height="270" frameBorder="0" class="giphy-embed" allowFullScreen></iframe>

Now we successfully milled the Trace

![mill1](https://raw.githubusercontent.com/salmanfarisvp/fablab-docs/master/img/modela/mill1.jpg)

Next Cut the Trace, First change the Bit,For Cutting we use **1/32**

![32bit](https://raw.githubusercontent.com/salmanfarisvp/fablab-docs/master/img/modela/32bit.jpg)

so first load the Image in **Fab Module** and make the path after that send it to machine to cutting

![fabmod3](https://raw.githubusercontent.com/salmanfarisvp/fablab-docs/master/img/modela/fabmod3.png)

make sure to set the bit as the **cut board(1/32)** and do the same that we did for milling , **make.path** and **make.rml** and start process by clicking **Send it!**

![pcb1](https://raw.githubusercontent.com/salmanfarisvp/fablab-docs/master/img/modela/pcb1.jpg)

We successfully completed cuting .

![pcb2](https://raw.githubusercontent.com/salmanfarisvp/fablab-docs/master/img/modela/pcb2.jpg)



