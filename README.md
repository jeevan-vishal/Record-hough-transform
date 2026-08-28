
# Exp.No : 7 ( Record-HOUGH TRANSFORM )

# Name : Jeevan Vishal.G.D
# Reg.no : 212224240062

# Edge-Linking-using-Hough-Transform

# Aim:
To write a Python program to detect the lines using Hough Transform.

# Software Required:
Anaconda - Python 3.7

# Algorithm:
## Step1:
Import all the necessary modules for the program.

## Step2:
Load a image using imread() from cv2 module.

## Step3:
Convert the image to grayscale.

## Step4:
Using Canny operator from cv2,detect the edges of the image.

## Step5:
Using the HoughLinesP(),detect line co-ordinates for every points in the images.Using For loop,draw the lines on the found co-ordinates.Display the image.


# Program : 
```py

import cv2
import numpy as np
import matplotlib.pyplot as plt

# Step 2: Load the image using imread() from cv2 module
image = cv2.imread('Tamizh.jpeg')  # Replace 'image.jpg' with your image path

# Step 3: Convert the image to grayscale
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)

# Input image and grayscale image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert image to RGB for displaying
plt.title("Input Image")
plt.axis('off')
plt.imshow(gray_image, cmap='gray')
plt.title("Grayscale Image")
plt.axis('off')

# Using Canny operator from cv2, detect the edges of the image
edges = cv2.Canny(gray_image, 50, 150)  # Canny edge detection with threshold values 50 and 150
# Canny Edge Detector output
plt.imshow(edges, cmap='gray')
plt.title("Canny Edge Detector")
plt.axis('off')


# Draw detected lines on the original image

for line in lines:
    x1, y1, x2, y2 = line
    cv2.line(image, (x1, y1), (x2, y2), (0, 255, 0), 2)

plt.figure(figsize=(10, 6))
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title("Detected Lines")
plt.axis('off')
plt.show()




```

# Output
## Input image and grayscale image

<img width="295" height="408" alt="image" src="https://github.com/user-attachments/assets/b02e68a9-6b06-417b-8f98-72c61d9ddd44" />

<img width="295" height="412" alt="image" src="https://github.com/user-attachments/assets/fad7fc8a-2a24-4891-8ab2-d89176e668a4" />



## Canny Edge detector output

<img width="297" height="405" alt="image" src="https://github.com/user-attachments/assets/5450dd87-3b2f-436d-82cb-b96e44616061" />


## Display the result of Hough transform

<img width="365" height="502" alt="image" src="https://github.com/user-attachments/assets/5113b4a2-16a9-4f22-9892-a6c525810d1f" />





# Result :
The edges and significant lines in the given image were successfully detected using the Canny Edge Detector and Hough Transform.
