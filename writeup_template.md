# **Finding Lane Lines on the Road** 

## Writeup Template

### You can use this file as a template for your writeup if you want to submit it as a markdown file. But feel free to use some other method and submit a pdf if you prefer.

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

[image1]: ./examples/grayscale.jpg "Grayscale"
[image2]: C:\Users\ravit\Desktop\SDC_Nano_Degree\CarND-LaneLines-P1-master\test_images\solidWhiteCurve.jpg
[image3]: C:\Users\ravit\Desktop\SDC_Nano_Degree\CarND-LaneLines-P1-master\test_images\Lines_Drawn\solidWhiteCurve_detected.jpg

---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 3 major steps and sub-steps as well. 

First, I detected the lanes in the image.

Second, I extracted the liens of the lanes detected and then made them into connected lines.

Third, I then used the connected lines, had a smoothing function with size of 10 and then finally added these to the video.

The first part is very similar to the procedure followed in the class. I firstly used canny lane detection and then used hough transform for finding the lines.

Second part, I calculated slope, identified the positive and negative slopes and then applied smooth function and found out the connected lines not by using basic extrapolation but by joining positive slopes and negative slopes.

The image comparison before and after detecting is shown below:

![alt text][image2]
![alt text][image3]


### 2. Identify potential shortcomings with your current pipeline

Identifying the methodology for connecting Hough Lines is a big shortcoming. Identifying the right algorithm for finding smooth lines is a challenge


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to finding a better methodology for joining hough lines
