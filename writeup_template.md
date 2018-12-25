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

---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 5 steps. First, I converted the images to grayscale, then I applied Gaussian smoothing with kernelsize 11 
to  smooth edges, after that i applied canny edge detection with minimume threshold 90 and maximum threshold 180 over the blur images. 
The next task was to define the region of interest for that i have modified the get_vertices function to define a rectangluar region. 
Once I manged to detect the lane lines correctly over the test images I have applied my pipeline over the video and it acurately able 
to detect the lane lines. 

In order to draw a single line on the left and right lanes, I modified the draw_lines() function by introducing a new function called 
separate_left_right_lines which takes lines and image as an input and return the point of the left and right lane lines. Once i got those 
points i extrapolated and draw the left and right lines. 




### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when there are stip curves because my solution has some dificulties in detecting them 
priciesly. 

Another shortcoming could be detecting shodows and blured lane lines 


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to use a better extrapolation method to detect curves

Another potential improvement could be to use another colour space to detect lanes even when their is shadow
