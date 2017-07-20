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

My pipeline was based from the quiz that we had on Hough Transform. However, one of the problems I bumped into was that I was only changing one picture out of the 6 so I had to find a way to create a loop that will iterate through each picture and modify all of them. Since I was following the code from the quiz, I was creating my loop at the top and then applying the different changes to the pictures. Consequently, this just transformed one picture of the bunch until I eventually looked in the forums and found out that putting the for loop at the end was the solution to my problem.
Besides that, the polygon was actually scaled to the right size of the different picture and the grayscaling work very efficiently.

# My pipeline consisted of 5 steps. First, I converted the images to grayscale, then I .... 

# In order to draw a single line on the left and right lanes, I modified the draw_lines() function by ...

# If you'd like to include images to show how the pipeline works, here is how to include an image: 

![alt text][image1]


### 2. Identify potential shortcomings with your current pipeline

The optional challenge showed that my code is not able to adapt to curves or changes in the path of the car. In the last video I could see that many things were highlighted red which makes sense since my code is only trained to highlight white lines in within the polygon.
Another shortcoming is that during the video, the highlight sometimes go a little crazy because they are tracing the lanes but they have a hard time marking them because some dissapear (bottom of the screen) and others appear (top of the screen). Sometimes there are cracks in the highways and the code is not able to differentiate those cracks with actual lanes.

# One potential shortcoming would be what would happen when ... 

# Another shortcoming could be ...


### 3. Suggest possible improvements to your pipeline

The main improvement I could make is to make my code recoginize changes within the polygon, recognize curves and other deficiencies on the road. I think I can accomplish this by having the top 2 ends of the polygon follow the lanes rather than having them be a specific value. Also, making the draw_lines() function be more selective with the white lines will help reduce the noise and the highlights (like cracks on the road). 

# A possible improvement would be to ...

# Another potential improvement could be to ...
