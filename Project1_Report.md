**Finding Lane Lines on the Road** 
---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect findings in a written report

[//]: # (Image References)
[image1]: ./examples/grayscale.jpg "Grayscale"

---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline was divided into 3 main parts: image preprocessing, edge detection, and line finding.

In preprocessing stage I grayscaled the image, then I applied Gaussian smoothing. This step was done to reduce the size of the image and to reduce noise in the image before working on it further.

After that, I fed the image through the Canny function to get the array of points which are the coordinates of the edges.
Then, assuming stationary camera, I limited the area further by applying region masking on the Canny edges array, limiting it to the bottom half of the image in the shape of a trapezoid.

The last stage was line detection using Hough transform. The parameters fed into it decide when a 

I chose a static image to test my code on as a starting point.
Since a video is just a series of images, the process would remain the same throughout the iterations.
The challenge then would be to figure out a just-right setting that can be applied to a wide range of scenario.



### 2. Identify potential shortcomings with your current pipeline

There were several assumptions I made that would make my pipeline fail. 

One of which was the availability of good lighting condition. The lines need to be easily distinguishable from the background for edge detection to work.

Another one would be that the street remain fairly straight. Sharp turns would place the lines out of the masked area, and it is possible that there would not be enough of the lane line visible to  


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to ...

Another potential improvement could be to ...
