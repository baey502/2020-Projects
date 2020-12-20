As a reminder to always be safe during this pandemic,
this program will use face recognition to apply glasses, a face shield, and a mask on a face.  
It will read points on the face and replace that area with a mask image. Referenced from Youtube tutorial: https://www.youtube.com/watch?v=tpWVyJqehG4

First, the libraries cv2, dlib, sys, numpy will be imported. 

The face detector and shape predictor will be initialized.
The shape predictor points out face landmarks from an image.

Then, the video for this example and the overlay mask image
with a transparent background will be loaded as well. 

The overlay function displays the mask image onto the video.

While loop: this will read the frames of the video, but if there
aren't any, it will break and end.

Resize frame section: the video used for this program is a 
bit large, so it will be resized to a more reasonable size. 

Find faces section: it detects the

Find facial landmarks section: this will use the shape predictor
to apply the 68 points of facial landmarks. 

Compute face boundaries section: this will find the size of the face, 
and the center of the face by finding the top and bottom corner.
This will draw a blue circle at the top left corner and 
bottom right corner.

Draw min, max coords section: the center of the face will be 
indicated with a red circle. Finding the center will help 
center the image mask. 

The mask image will be placed on the center point and will be 
resized to fit into the video. The mask image size is a bit small,
so it is enlarged 1.8 and the overlay is moved a bit on both
x and y coordinates in order to make the image more centered onto the face.