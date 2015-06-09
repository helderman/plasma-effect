# How to...

All backdrops have been created using [GIMP](http://www.gimp.org).
Here is a walkthrough for each one of them.

## Plasma

1. Open the [New Image dialog](http://docs.gimp.org/en/gimp-file-new.html).
2. Set the width to 480 and the height to 360 (both in pixels) and click button 'OK'. This should create a new empty image.
3. Open the [Solid Noise](http://docs.gimp.org/en/plug-in-solid-noise.html) dialog.
4. Fill in: random seed = 0, randomize = off, turbulent = off, detail = 1, tilable = on, X size = 4.0, Y size = 4.0. Click button 'OK'. This should fill the image with some grey 'clouds'.
5. In the [Gradients Dialog](http://docs.gimp.org/en/gimp-gradient-dialog.html), find the gradient named 'Full saturation spectrum CCW'. Right-click it; a context menu should appear.
6. From the context menu, select 'Duplicate Gradient'. A new window 'Gradient Editor' should appear.
7. Right-click anywhere on the gradient (the colored bars) in the gradient editor; a context menu should appear.
8. From the context menu, select 'Replicate Segment'. A dialog 'Replicate Segment' should appear.
9. In the dialog, set the slider on '4' and click button 'Replicate'.
10. Close the gradient editor. Verify that your new gradient 'Full saturation spectrum CCW copy' is the selected gradient in the gradients dialog.
11. Apply [Gradient Map](http://docs.gimp.org/en/plug-in-gradmap.html). The clouds, initially grey, are now in full color.

Note: in steps 2, 4 and 9, there is plenty of room for variation.

## HeldLaw

1. Open the [New Image dialog](http://docs.gimp.org/en/gimp-file-new.html).
2. Set the width to 480 and the height to 360 (both in pixels) and click button 'OK'. This should create a new empty image.
3. Select the [blend tool](http://docs.gimp.org/en/gimp-tool-blend.html). In the tool options, select gradient 'Full saturation spectrum CCW', shape 'linear', repeat 'sawtooth wave'.
4. Drag the mouse anywhere across your image, drawing a diagonal line in south-east direction (i.e. in the direction of the bottom right corner) roughly 50 pixels long. As soon as you release the mouse button, colorful diagonal bars should fill the entire image.
5. [Create a new layer](http://docs.gimp.org/en/gimp-layer-new.html); name it 'displacer'.
6. Fill the new layer with color #808080 (which is grey). This color is important, as it is the 'neutral' color for 'displace' mapping.
7. Put some black text on this layer. Make sure there is no floating text layer left; merge down into the grey layer.
8. Apply a gaussian blur with a blur radius of 15 pixels (both X and Y).
9. Select the 'background' layer (the one with the colorful bars).
10. Open the Displace Map dialog. X displacement: 20 pixels, layer 'displacer'. Y displacement: the same. Displacement mode: Cartesian. Click button 'OK'.

## Rising (INCORRECT)

Roughly done like this:
1. Open the [New Image dialog](http://docs.gimp.org/en/gimp-file-new.html).
2. Set both width and height to 480 pixels and click button 'OK'. This should create a new empty image.
3. Select the [blend tool](http://docs.gimp.org/en/gimp-tool-blend.html). In the tool options, select gradient 'Full saturation spectrum CCW', shape 'linear', repeat 'sawtooth wave'.
4. Drag the mouse downward anywhere across your image, drawing a vertical line roughly 120 pixels long (i.e. 1/4 of the height of your image). As soon as you release the mouse button, colorful horizontal bars should fill the entire image.
5. [Create a new layer](http://docs.gimp.org/en/gimp-layer-new.html); name it 'Displace X'.
6. Open the [Solid Noise](http://docs.gimp.org/en/plug-in-solid-noise.html) dialog.
7. Fill in: randomize = on, turbulent = off, detail = 1, X size = 6.0, Y size = 6.0. Click button 'OK'. This should fill the image with some grey 'clouds'.
8. [Create another new layer](http://docs.gimp.org/en/gimp-layer-new.html); name it 'Displace Y'.
9. Open the [Solid Noise](http://docs.gimp.org/en/plug-in-solid-noise.html) dialog.
10. Fill in: randomize = on, turbulent = on, detail = 1, X size = 4.0, Y size = 1.0. Click button 'OK'. This should fill the image with some grey flame-like shapes.
11. With layer 'Displace Y' still active, open the [Levels Dialog](http://docs.gimp.org/en/gimp-tool-levels.html).
12. In the 'input levels' section, change the rightmost number from 255 to 128. Click button 'OK'. This should make the 'flames' brighter.
13. In the [Layers Dialog](http://docs.gimp.org/en/gimp-dialogs-structure.html#gimp-layer-dialog), select the original 'Background' layer (the one filled with the colorful gradient). Make the other two layers invisible (by clicking their 'eye').
- Displace map
- Distort - Polar coordinates; uncheck 'To Polar'
- Reduce size to 480x360
