**Finding Lane Lines on the Road** 
---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report

[//]: # (Image References)
[image1]: ./examples/grayscale.jpg "Grayscale"

---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

As the first step, I chose a static image to develop test my code on. My pipeline was divided into 3 main parts: image preprocessing, edge detection, and line finding.

In preprocessing stage I grayscaled the image, then I applied Gaussian smoothing. This step was done to reduce the size of the image and to reduce noise in the image before working on it further.

After that, I fed the image through the Canny function to get the array of points signifying edges of objects.
Then, assuming stationary camera, I limited the are of interest further by applying region masking on the Canny edges array, limiting it to the bottom half of the image in the shape of a trapezoid.

The last stage was line detection using Hough transform. The parameters fed into it decide when a 




### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when ... 

Another shortcoming could be ...


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to ...

Another potential improvement could be to ...
