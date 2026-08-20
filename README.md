# Image Segmentation Using Thresholding Techniques in OpenCV

## Developed By

**Name:** P.Bhavankumar


**Register No:**212225240026

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

## Program :
### Original Grayscale Image

```
import cv2
import matplotlib.pyplot as plt
img = cv2.imread("lego.jpg")
plt.imshow(cv2.cvtColor(img, cv2.COLOR_BGR2RGB))
plt.title("Original Image")
plt.axis("off")
plt.show()
```
<img width="473" height="522" alt="637321126-9df96033-637b-43c4-9545-864998a1fa02" src="https://github.com/user-attachments/assets/2380d93a-0891-448e-938c-7addaddea54f" />


### Global Thresholding
```
import cv2
import matplotlib.pyplot as plt
img = cv2.imread("lego.jpg", cv2.IMREAD_GRAYSCALE)
plt.imshow(img, cmap="gray")
plt.title("Original Grayscale Image")
plt.axis("off")
plt.show()
```

<img width="494" height="504" alt="637321432-355d33a6-184c-4ef2-aef2-1d6943c95d04" src="https://github.com/user-attachments/assets/5112eeb2-a972-463a-b55f-1a2376a0127e" />


### Adaptive Thresholding
```
import cv2
import matplotlib.pyplot as plt
img = cv2.imread("lego.jpg", cv2.IMREAD_GRAYSCALE)
_, result = cv2.threshold(img, 127, 255, cv2.THRESH_BINARY)
plt.imshow(result, cmap="gray")
plt.title("Global Thresholding")
plt.axis("off")
plt.show()
```
<img width="542" height="510" alt="637321660-59418527-c870-45d7-8adc-15a4cbdc4991" src="https://github.com/user-attachments/assets/31f7eed1-7ac7-423d-aada-de2d4ce37e64" />


### Otsu's Thresholding
```

import cv2
import matplotlib.pyplot as plt
img = cv2.imread("lego.jpg", cv2.IMREAD_GRAYSCALE)
_, result = cv2.threshold(
    img, 0, 255,
    cv2.THRESH_BINARY + cv2.THRESH_OTSU
)
plt.imshow(result, cmap="gray")
plt.title("Otsu's Thresholding")
plt.axis("off")
plt.show()
```

<img width="483" height="509" alt="637322210-b2f18eae-7ffa-4afe-a1e8-853102ac0bab" src="https://github.com/user-attachments/assets/74936961-50cf-46c7-882d-0bcee874c31f" />

## Result

Thus, image segmentation is successfully performed using **Global Thresholding, Adaptive Thresholding, and Otsu's Thresholding** techniques in OpenCV. 
