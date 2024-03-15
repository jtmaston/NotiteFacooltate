# Chapter 5: Mapping and Simulation

Remember the "Process" tab? Time to run the next step! Make sure both "Map trace" and "Verilog simulation file" are
ticked for this part, then run the process by double-clicking it. Your output should display "completed successfully",
alongside green checkmarks.
![image_27.png](image_27.png)

Next up, let's set up the simulation. In the top bar, select the icon below, or go to "Tools > Simulation wizard".
![image_28.png](image_28.png)

Give it a name, then, once you reach the "process stage", select "post-map gate-level". This will generate a more
like-life simulation of the circuit than plain RTL.
![image_29.png](image_29.png)
![image_30.png](image_30.png)

Note to self: I bonked something here and the simulation doesn't detect sources. Classify this as a WIP section! Sorry!