# EDGE-DETECTION
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import all the necessary modules for the program.

### Step2:
Load a image using imread() from cv2 module.

### Step3:
Convert the image to grayscale

### Step4:
Using Sobel operator from cv2,detect the edges of the image.

### Step5:

Using Laplacian operator from cv2,detect the edges of the image and Using Canny operator from cv2,detect the edges of the image.

## PROGRAM:
``````````````
import cv2
import matplotlib.pyplot as plt
img = cv2.imread('rome.png')
gray = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)
gray = cv2.GaussianBlur(gray, (3, 3), 0)
sobelx = cv2.Sobel(gray, cv2.CV_64F, 1, 0, ksize=5)
plt.figure(figsize=(8, 8))
plt.subplot(1, 2, 1)
plt.imshow(gray, cmap='gray')
plt.title("Original Image")
plt.axis("off")
plt.subplot(1, 2, 2)
plt.imshow(sobelx, cmap='gray')
plt.title("Sobel X axis")
plt.axis("off")
plt.show()

sobely = cv2.Sobel(gray, cv2.CV_64F, 0, 1, ksize=5)

plt.figure(figsize=(8, 8))
plt.subplot(1, 2, 1)
plt.imshow(gray, cmap='gray')
plt.title("Original Image")
plt.axis("off")
plt.subplot(1, 2, 2)
plt.imshow(sobely, cmap='gray')
plt.title("Sobel Y axis")
plt.axis("off")
plt.show()

sobelxy = cv2.Sobel(gray, cv2.CV_64F, 1, 1, ksize=5)

plt.figure(figsize=(8, 8))
plt.subplot(1, 2, 1)
plt.imshow(gray, cmap='gray')
plt.title("Original Image")
plt.axis("off")
plt.subplot(1, 2, 2)
plt.imshow(sobelxy, cmap='gray')
plt.title("Sobel XY axis")
plt.axis("off")
plt.show()
``````````````
## Output:
<img width="438" height="321" alt="image" src="https://github.com/user-attachments/assets/86e20f97-87d9-44e0-8815-8ecf46157e21" />
<img width="462" height="300" alt="image" src="https://github.com/user-attachments/assets/137ae441-3c87-46a5-af02-8eee436aad9c" />
<img width="444" height="305" alt="image" src="https://github.com/user-attachments/assets/13ced2e9-bbc5-4e90-8bb2-0503d1dc3316" />
<img width="439" height="314" alt="image" src="https://github.com/user-attachments/assets/6ba2d7ba-a6b9-42c6-93f4-b1585a194165" />





## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
