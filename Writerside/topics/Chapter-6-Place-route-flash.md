# Chapter 6: Place, route, flash!

Now, let's place and route our design. This means locating all components onto the silicon of the FPGA. In the "Process"
tab, select both "Place & route trace" and "I/O timing analysis", in order to also get the frequencies checked out. 
Double-click "Place and route design", and...
![image_31.png](image_31.png)

Huh. Something failed. Let's check the console.
![image_32.png](image_32.png)

Well, that's vague. What could that error mean?
I'll admit, this took me much more than it should have to figure out, but... I just had to scroll up in the console
output :).
![image_33.png](image_33.png)

Okay, this tells us much more about the problem. Let's double-check the LPF file then the Spreadsheet view.
![image_34.png](image_34.png)

Huh. That's odd. The LPF is directing the FPGA to clamp the voltage on the pin, effectively constantly pulling it to
that voltage. I removed the directive (I could have edited from the Spreadsheet view) and...
![image_36.png](image_36.png)

Voilà! All routed.

We can now take a more in-depth look at the design we just created. Looking at the top bar, there's plenty of menus to
explore.
![image_37.png](image_37.png)
1. Spreadsheet view, we're used to this
2. Package view, shows pin assignments on the FPGA chip itself
    ![image_38.png](image_38.png)
    Notice slightly more gray symbols for pins in use, as well as green interior for inputs. Hovering over any pins
    reveals their use and assignment.
3. Netlist analyzer, displays the netlist of the design, allowing for a visualization of the logical blocks of our device
    ![image_39.png](image_39.png)
    I'm afraid my inexperience leaves me incapable of further explaining this topic :).
4. Netlist view, displays inputs and outputs, as well as their types (if clock inputs or not)
    ![image_40.png](image_40.png)
5. NCD view: I'm not sure what this is, from what I've found, it refers to the "Native Circuit Description", a tree
    that shows resources (logical blocks of an FPGA) used.
    ![image_41.png](image_41.png)
6. We'll skip Clarity designer for now, as well as the Reveal modules
7. Floorplan view: Shows the location of each logical block
    ![image_42.png](image_42.png)
8. Physical view: Shows the location of each block, the links between them, as well as the elements that comprise each
   block. You're further able to dive into each "Slice and see its components"
    ![image_43.png](image_43.png)
    ![image_45.png](image_45.png)

Now, all that's left is to export your desired file type, and flash it onto an FPGA. Neat!