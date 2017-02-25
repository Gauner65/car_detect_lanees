#**Finding Lane Lines on the Road** 

##Writeup Template

###You can use this file as a template for your writeup if you want to submit it as a markdown file. But feel free to use some other method and submit a pdf if you prefer.

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

[image1]: ./examples/grayscale.jpg "Grayscale"
[image2]: ./result.jpg "Result"
---

### Reflection

###1. In the following I describe my pipline to detect the ego lanes on a strait road:

1. convert image to grayscale
2. apply a gaussian noise kernel of size 5
3. detect edges within the image with the canny edge function implementation from opencv
4. apply a quadrilateral image mask as a ROI
5. use the hough transform to detect lines
6. to seperate the left and right lanes I apply a filter threshold on the slope
7. fitting a line through all points
8. plot the results

![alt text][image2]




###2. Identify potential shortcomings with your current pipeline

* currently only working for strait lanes since only first order line fitting is used (possible to extend to higher order)
* image ROI might not fit for all scenarios
* only ego lane is detected


###3. Suggest possible improvements to your pipeline

 * higher order lane fitting
 * additional outlier filter like ransac

