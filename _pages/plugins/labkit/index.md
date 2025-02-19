---
mediawiki: Labkit
title: Labkit

artifact: net.imglib2:imglib2-labkit
categories: [Uncategorized]
---

<img src="/media/plugins/labkit-illustration.jpg" width="700"/>

Labkit is a user-friendly Fiji plugin for the segmentation of microscopy image data.  It offers easy to use manual and automated image segmentation routines that can be rapidly applied to single- and multi-channel images as well as timelapse movies in 2D or 3D. Labkit is specifically designed to work efficiently on big image data and users of consumer laptops can conveniently work with multiple terabytes large image data. This efficiency is achieved by using Imglib2 and BigDataViewer as the foundation of our software. Furthermore, memory efficient and fast random forest based pixel classification based on the Waikato Environment for Knowledge Analysis (WEKA) is implemented, optionally exploiting the power of graphics processing units (GPUs) to gain additional performance and can even be used on high performance computing clusters (HPC) for distributed processing of big image data. Finally, manual tools for ground-truth annotation are available. 

<!---

## Publication

If you find Labkit useful for your research, please cite it:
-->

## Installation

1. Install [Fiji](https://imagej.net/software/fiji/downloads)
2. Install Labkit's [update site](/update-sites/following):
   1. Start Fiji
   2. From the menu, select {% include bc path="Help | Update" %}
   3. Click on `Manage Update Sites`, then select `Labkit` in the table
   4. Close, click on `Apply changes` and then `Ok`
   5. Restart Fiji
3. Find Labkit in the plugin menu of Fiji, under "Labkit".

## Documentation, tutorials and guidelines

- The [documentation](/plugins/labkit/documentation) provides details of Labkit functionalities 
- In the [tutorials page](/plugins/labkit/tutorials), you fill find diverse general and advanced tutorials, from manual and automatic segmentation, to macro, GPU-acceleration and running labkit on HPC clusters.
- The [guidelines](/plugins/labkit/guidelines) page gives insight in how to improve the automatic segmentation

## FAQ

**Is it possible to manually segment a 3D image slice by slice?**

Yes, this can be achieved by a workaround: Simple convert your image to 2D+time before opening it with Labkit. In Fiji use "Image > Hyperstacks > Re-order Hyperstack ..." to convert your image from 3D to 2D+time. 

**After starting Labkit the window that should show my image is black?**

This often happens if Labkit can't find proper brightness & contrast settings. Please click the button that says "auto contrast".

**How I manually select the colors and brightness settings that are used to show the image?**

Click {% include key key='S' %} on your keyboard. This should show the BigDataViewer brightness & color dialog. Use it to manually adjust those settings.

**Can Labkit distinguish more than two classes "foreground" and "background"**

Yes, simple click the "Add label" button this will add a new class. You are free to name labels / classes as you would like, simple double click on the label.

**How can I change the color of the labels?**

Just click on the colored rectangle left of the labels name. This will show a color selection dialog.


## Keyboard Shortcuts

### Basic Navigation

Labkit is based on BigDataViewer. Navigation the image works as in BigDataViewer, and many shortcuts work too. Click [here](/plugins/bdv) for a description of the shortcuts.

-   {% include key keys='Ctrl|Shift|mouse-wheel' %} to zoom in and out
-   {% include key keys='right-drag' %} to move the image
-   {% include key keys='left-drag' %} to rotate a 3d image
-   {% include key key='mouse-wheel' %} to scroll through the z-slices of a 3d image


### Drawing Tool
-   {% include key keys='D|left-click' %} to draw with the pencil tool.
-   {% include key keys='E|left-click' %} to erase with the pencil tool.
-   {% include key keys='F|left click' %} to use the flood fill tool.
-   {% include key keys='R|left-click' %} to remove a connected component.
-   {% include key key='N' %} - switch to next label

