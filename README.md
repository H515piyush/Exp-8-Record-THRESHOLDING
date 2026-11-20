# Image Segmentation Using Thresholding Techniques in OpenCV

## Aim

To segment an image using Global Thresholding, Adaptive Thresholding, and Otsu's Thresholding techniques using Python and OpenCV.

The program performs the following operations:

- Global Thresholding
- Adaptive Thresholding
- Otsu's Thresholding

## Software Used

- Anaconda – Python 3.7
- Jupyter Notebook / VS Code
- OpenCV (cv2)
- NumPy
- Matplotlib

## Algorithm

### Step 1:

Import the required libraries: OpenCV, NumPy, and Matplotlib.

### Step 2:

Load the input image using OpenCV.

### Step 3:

Convert the input image into grayscale format.

### Step 4: Global Thresholding

- Select a fixed threshold value.
- Apply thresholding to separate foreground and background pixels.
- Display the thresholded image.

### Step 5: Adaptive Thresholding

- Compute threshold values for small regions of the image.
- Apply Adaptive Mean Thresholding.
- Apply Adaptive Gaussian Thresholding.
- Display the segmented images.

### Step 6: Otsu's Thresholding

- Automatically determine the optimal threshold value.
- Apply Otsu's thresholding technique.
- Display the segmented image.

### Step 7:

Compare the results obtained from Global, Adaptive, and Otsu's thresholding methods.

## Program
```
import cv2
import matplotlib.pyplot as plt
```
## Read the Image and convert to grayscale:
```
image=cv2.imread('pandas.jpg')
gray_img=cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
```
## Original image:
```
plt.subplot(2,2,1)
plt.imshow(cv2.cvtColor(image,cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```
## Use Global thresholding to segment the image:
```
_,global_thresholded = cv2.threshold(gray_img, 127, 255, cv2.THRESH_BINARY)
```
### Use Adaptive thresholding to segment the image:
```
adaptive_thresholded = cv2.adaptiveThreshold(gray_img, 255, cv2.ADAPTIVE_THRESH_GAUSSIAN_C, cv2.THRESH_BINARY, 11, 2)
```
### Use Otsu's method to segment the image:
```
_,otsu_thresholded = cv2.threshold(gray_img, 0, 255, cv2.THRESH_BINARY + cv2.THRESH_OTSU)
```
### Global Thresholding:
```
plt.subplot(2, 2, 2)
plt.imshow(global_thresholded, cmap='gray')
plt.title("Global Thresholding")
plt.axis('off')
```
### Adaptive Thresholding:
```
plt.subplot(2, 2, 3)
plt.imshow(adaptive_thresholded, cmap='gray')
plt.title("Adaptive Thresholding")
plt.axis('off')
```
### Otsu's Method:
```
plt.subplot(2, 2, 4)
plt.imshow(otsu_thresholded, cmap='gray')
plt.title("Otsu's Method")
plt.axis('off')
```
### Show the plot:
```
plt.tight_layout()
plt.show()
```

## Developed By

## Name: Piyush kumar
## Register number: 212223220075

## Output

### Original Grayscale Image

<img width="295" height="262" alt="Screenshot 2026-11-20 132852" src="https://github.com/user-attachments/assets/34a02a3c-a4a7-4708-bc33-02ead5393f09" />




- The grayscale version of the input image is displayed.
- Serves as the input for thresholding operations.

### Global Thresholding

<img width="362" height="300" alt="Screenshot 2026-11-20 132858" src="https://github.com/user-attachments/assets/bfacc2d3-2cb6-4adc-ba3c-ca7121ca6a16" />


- Original image is displayed.
- Thresholded image is displayed.
- A fixed threshold value is used for segmentation.
- Pixels are classified as foreground or background.

### Adaptive Thresholding

<img width="326" height="315" alt="Screenshot 2026-11-20 132907" src="https://github.com/user-attachments/assets/ad5e928e-1eb7-4aae-8203-335254c6ae88" />


- Original image is displayed.
- Adaptive Mean Thresholded image is displayed.
- Adaptive Gaussian Thresholded image is displayed.
- Threshold values vary across different regions of the image.
- Suitable for images with uneven illumination.

### Otsu's Thresholding

<img width="320" height="305" alt="Screenshot 2026-11-20 132903" src="https://github.com/user-attachments/assets/a12d856c-d98e-4f38-b5a6-1bca9a24ed6e" />

- Original image is displayed.
- Otsu segmented image is displayed.
- Optimal threshold value is calculated automatically.
- Produces improved segmentation for bimodal histograms.


## Result

Thus, image segmentation is successfully performed using **Global Thresholding, Adaptive Thresholding, and Otsu's Thresholding** techniques in OpenCV. 
