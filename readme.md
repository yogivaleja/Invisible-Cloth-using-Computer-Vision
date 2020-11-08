# Invisible Cloth  
  
If you are a Harry Potter fan, you would know what an Invisibility Cloak is. Yes! It;s the cloak that makes Harry Potter invisible.  
It is possible to create an illusion of Invisibility using the power of Computer Vision in Python.

# Instructions  
  
Simply run the python code and dont stand near the screen and when the webcam turns ON take a red cloth and cover yourself and become magician.

# How it works?  
  
This technique is opposite to the Green Screening. In green screening, we remove background but here we will remove the foreground frame.  
  
1. Capture and store the background frame.    
2. Detect the defined color using color detection and segmentation algorithm.  
3. Segment out the defined colored part by generating a mask.  
4. Generate the final augmented output to create a magical effect. [ output.avi ]  
  
# HSV  
  
HSV stands for Hue Saturation Value.  

## H:Hue  
  
Hue is the colour portion of the model, expressed as a number from 0 to 360 degrees:  
Red falls between 0 and 60 degrees.  
Yellow falls between 61 and 120 degrees.  
Green falls between 121–180 degrees.  
Cyan falls between 181–240 degrees.  
Blue falls between 241–300 degrees.  
Magenta falls between 301–360 degrees.  

## S:Saturation  
  
Saturation describes the amount of grey in a particular colour, from 0 to 100 percent. Reducing this component toward zero introduces more grey and produces a faded effect. Sometimes, saturation appears as a range from just 0–1, where 0 is grey, and 1 is a primary colour.  
  
## V:Value  
  
Value works in conjunction with saturation and describes the brightness or intensity of the colour, from 0–100 percent, where 0 is completely black, and 100 is the brightest and reveals the most colour.  
  
# Detecting the define color portion in each frame  
  
In this step, we will put our focus on detecting the red part in the image. We will convert the RGB (red-blue-green) to HSV(hue-saturation-value) because RGB values are highly sensitive to illumination. After the conversion of RGB to HSV, it is time to specify the range of color to detect red color in the video. Below color values are for red color.  

#  Replacing the red portion with a mask image in each frame

  
Now, we have a red part of the video in the ‘mask’ image, we will segment the mask part from the frames. We will do a morphology open and dilation for that.

