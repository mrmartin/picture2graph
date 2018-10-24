# picture2graph

Use this script to convert raster graphs into continuous functions. Requires manually placing a bezier curve on the image.

The python code is in [process_bezier_svg.ipynb](../master/process_bezier_svg.ipynb)

How it works:
1. start with a [spec sheet](../master/334-15__T1C1-4WYA.pdf)
2. get a screenshot of your graph, like this
![alt text](../master/screenshot.png "Raster graph")
3. use InkScape (or whatever) to import the graph, and draw a bezier curve on top. Make sure to start and end the curve at marked edges
![alt text](../master/inkscape.png "Inkscape screenshot")
4. remove the image from InkScape, and save the svg
5. use the python code to convert the svg to a path
6. you're done!
![alt text](../master/result.png "Result")
