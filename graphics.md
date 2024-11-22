## Graphics Programming

- it is a programming technique which is used to draw different graphics(shapes)
like lines rectangles, circles, arcs or even text with different graphics styles
- graphics.h header file contains the different functions needed for graphics programming like line(), rectangle(),circle() etc.

Steps involved
1. include graphics.h header file in your program
2. convert the output mde from CUI(Character User Interface) to GUI(Graphical User Interface) by using initgraph() method
 for eg.:
  ``initgraph()`` uses three args; graphics driver, graphics mode, path to graphics library;
```
int gd = DETECT, gm;
initgraph(&gd,&gm,"c:\\turboc\\bgi");
```
- ``DETECT`` is a macro which finds the best suitable graphics driver installed in the computer and also find the best suitable 
graphics mode for the selected graphics driver
3. now draw the req shape by using the respective function
  for e.g. ``circle(100,100,50)``
4. close the graphics mode by using ``closegraph()``;
