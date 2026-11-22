# Implementation of Erosion and Dilation Using OpenCV
# Aim
To write a Python program using OpenCV to perform morphological operations such as Erosion and Dilation on an image.

The program performs the following operations:

Image Erosion

Image Dilation

# Software Used
Anaconda – Python 3.7

Jupyter Notebook / VS Code

OpenCV (cv2)

NumPy

Matplotlib

# Algorithm

# Step 1:
Import the required libraries: OpenCV, NumPy, and Matplotlib.

# Step 2:
Create a blank image using NumPy.

# Step 3:
Insert text onto the image using OpenCV's text drawing function.

# Step 4:
Display the original image.

# Step 5:
Create a structuring element (kernel) of suitable size.

# Step 6: Image Erosion
Apply the erosion operation using the created kernel.
Remove pixels from the boundaries of foreground objects.
Display the eroded image.

# Step 7: Image Dilation
Apply the dilation operation using the same kernel.
Add pixels to the boundaries of foreground objects.
Display the dilated image.
# Step 8:
Compare the original, eroded, and dilated images.

Developed By
Name: Kanishka V

Register No: 212224100030

# PROGRAMM
# Original Image
```
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = np.zeros((300, 600), dtype=np.uint8)

cv2.putText(
    image,
    "EROSION AND DILATION",
    (50, 160),
    cv2.FONT_HERSHEY_SIMPLEX,
    1.2,
    255,
    3
)

kernel = np.ones((5, 5), np.uint8)

eroded = cv2.erode(image, kernel, iterations=1)

dilated = cv2.dilate(image, kernel, iterations=1)

plt.figure(figsize=(8, 4))
plt.imshow(image, cmap="gray")
plt.title("Input Image")
plt.axis("off")
plt.show()
```
# Erosion
```
plt.figure(figsize=(8, 4))
plt.imshow(eroded, cmap="gray")
plt.title("Eroded Image")
plt.axis("off")
plt.show()
```
# Dilation
```
plt.figure(figsize=(8, 4))
plt.imshow(dilated, cmap="gray")
plt.title("Dilated Image")
plt.axis("off")
plt.show()
```
# Comparison of all three
```
plt.figure(figsize=(12, 4))

plt.subplot(1, 3, 1)
plt.imshow(image, cmap="gray")
plt.title("Input image")
plt.axis("off")

plt.subplot(1, 3, 2)
plt.imshow(eroded, cmap="gray")
plt.title("Eroded image")
plt.axis("off")

plt.subplot(1, 3, 3)
plt.imshow(dilated, cmap="gray")
plt.title("Dilated image")
plt.axis("off")

plt.show()
```
# output:

# Input image:

<img width="549" height="297" alt="image" src="https://github.com/user-attachments/assets/eb89ac4a-e3a3-4379-a625-8947bf4bc831" />

# erosion:

<img width="578" height="282" alt="image" src="https://github.com/user-attachments/assets/82a1b2f1-4f33-4f32-b396-1a99ed908b82" />

# Dilation:

<img width="555" height="276" alt="image" src="https://github.com/user-attachments/assets/1d077862-4f06-4836-9cf8-f031719068e0" />

# comparison of all three:

<img width="676" height="126" alt="image" src="https://github.com/user-attachments/assets/0f39dc78-5e36-4e75-b582-cf1c1e0ff3dd" />

# Result:
Thus, the morphological operations Erosion and Dilation are successfully implemented using OpenCV.
