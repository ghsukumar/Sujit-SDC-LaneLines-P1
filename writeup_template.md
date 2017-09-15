# **Finding Lane Lines on the Road** 

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road first for static images.
* Make a pipeline that finds lane lines on the road next for a video clip re-using code used to find lanes lines for the static images.

Images are in the git repo under the test_images_output folder.  
Generated videos are in the git repo under the test_videos_output folder.  

---

### Reflection

### 1. Description of the pipeline.

My pipeline consisted of the following steps:
* Read all the images
* For each image, convert to gray scale
* Using the provided helper (utility) methods, 
* do gaussian blur,
* get canny edges, 
* determine area of interest by selecting the vertices of the polygon,
* apply hough transform and get the lane lines from the images.

Images are in the git repo under the test_images_output folder.  
https://github.com/ghsukumar/Sujit-SDC-LaneLines-P1/tree/master/test_images_output  
  
Generated videos are in the git repo under the test_videos_output folder.  
https://github.com/ghsukumar/Sujit-SDC-LaneLines-P1/tree/master/test_videos_output  

### 2. Potential shortcomings with current pipeline

Lane lines on the generated videos are not bright. It shows in a faint red. The process image callback returns a weighted image of the original image and an image with the lines on canny edges image.

### 3. Possible improvements to the current pipeline

1) Work on playing with the weighted image params to show a darker line for the lane lines.  
2) Some of the images don't have the lane lines marked all through. Need to improve the draw lines method.  
