# **Finding Lane Lines on the Road** 

### Reflection

### 1. Pipeline Description. 

My pipeline consisted of 6 steps, which are as follows: 

Step 1 (Make a copy of the Image): Make a copy of the original image, so that I can re-use later

Step 2 (Convert Image to Grayscale): Converted the original image to grayscale image for processing

Step 3 (Remove Background Noise): I applied a guassian blur to the grayscale image to remove backgroung unwanted noise

Step 4 (Edge Detection) : I applied a canny edge detection on the blurred image.

Step 5 (Set Region of Interest): There are so many edges that are not needed in the image,sub image representing the area needed is cut out of the main image and compare with the main image to set the area as ROI and every other area is set black

Step 6 (Apply Hough): Hough transform is applied to the image to perform grouping of edges.

Step 7 (Draw Line on Right and Left Lane): To draw the right and left lane on the image, lines output of the hough transform is use to estimate the average slope of lines in both the left and right lane. The average slope of the lines with some reference point taking from the lines is used to compute the lane line start point and end point.


Sample Image
[image1]: ./test_images/solidYellowCurve2.jpg "Sample"
[image1]: ./test_images_output/solidYellowCurve2.jpg "Sample2"



### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when there is noise edges in between the Lane line. 
