# Chapter 2: Project creation

![latticeDiamond.jpg](latticeDiamond.jpg)

Welcome to Lattice Diamond! Project creation is rather straightforward. File > New > Project. Then, select where to
save the project.


Select where you'd like to save the project: my advice is to create a new directory with the name of the project, then
select that. Diamond creates a *metric tonne* of files when running, so it's recommended you create files for each
project. As for the implementation, this is where the compiled verilog code and physical implementation reside, and
I like to keep this as a subdir of the project being worked on.
![latticeDiamond2.jpg](latticeDiamond2.jpg)

If you have any already-available source files, now's the time to add them to the project. They'll be copied (i.e.
copied, not referenced) to the project directory, and be available in the file toolbar. As I'm starting a blank
project, nothing to add here.
![image_11.png](image_11.png)

Next up, select your device from the dropdown list. Make sure you pick the correct performance grade and conditions.
Since we're here, it's also advised to click the
["Online Data Sheet for Device"](https://www.latticesemi.com/view_document?document_id=50461), to save the datasheet for
future reference.
![image_12.png](image_12.png)

Now, select a synthesis tool. I haven't played around enough with the software to be able to tell you the difference
between the tools given, so I just generally leave it to the default value.
![image_13.png](image_13.png)

Finally, check that all data is correct, and hit "Finish". Congrats! You've just created your first Lattice Diamond
project!
![image_14.png](image_14.png)

You should arrive at the project summary window.
![image_15.png](image_15.png)

