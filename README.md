# picture2graph

Use this script to convert raster graphs into continuous functions. Requires manually placing a bezier curve on the image. I use this to extract spectral response wavelengths from LED specsheets, but it can be used anywhere where the data for a graph you see can't be got, like when replicating published results.

The python code is in [process_bezier_svg.ipynb](../master/process_bezier_svg.ipynb)

How it works:
1. start with a [spec sheet](../master/334-15__T1C1-4WYA.pdf)
2. get a screenshot of your graph, like this

![alt text](../master/screenshot.png "Raster graph")
3. use InkScape (or whatever) to import the graph, and draw a bezier curve on top. Make sure to start and end the curve at marked edges

![alt text](../master/inkscape.png "Inkscape screenshot")

4. remove the image from InkScape, and save the svg

5. use the [python code](../master/process_bezier_svg.ipynb) to convert the svg to a path

6. Don't forget to set your x-range and y-range

![alt text](../master/result.png "Result")

An example application if the convertsion of the sensitivity of human eye color receptors to a continuous function

<img src="../master/human_vision_berkeley_cecilia77.png" alt="Input" width="381"/>
![alt text](../master/human_vision_berkeley_cecilia77_output.png "Output")
