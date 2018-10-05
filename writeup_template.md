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

There are several steps to the pipeline:
1. The image is placed into grayscale
2. We utilize gaussian blurring to smooth things & reduce noise
3. We utilize canny edge detection

[canny]: ./writeup/canny.png "Canny"

[logo]: https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png "Logo Title Text 2"



4. We mask the image with region processing to isolate the lane lines further
5. We utilize hough transformations to discover points that could be connected via a line.
6. We calculate & extrapolate lines from the bottom of the camera perspective through the rest of the image based on the output of #5
7. Finally, we draw those lines overlayed on the original image.

As a result, we can take each frame of a video and show lines on it into a final video.


### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when ... 

Another shortcoming could be ...


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to ...

Another potential improvement could be to ...
