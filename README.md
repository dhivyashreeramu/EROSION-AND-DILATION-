# EXPERIMENT 9 – IMPLEMENTATION OF EROSION AND DILATION USING OPENCV
# NAME : DHIVYASHREE R
# REGNO: 212225040077

## Aim

To write a Python program using OpenCV to perform morphological operations such as Erosion and Dilation on an image.

The program performs the following operations:

- Image Erosion
- Image Dilation

## Software Used

1. Anaconda – Python 3.7
2. Jupyter Notebook / VS Code
3. OpenCV (cv2)
4. NumPy
5. Matplotlib

## Algorithm

**Step 1:** Import the required libraries: OpenCV, NumPy and Matplotlib.

**Step 2:** Create a blank image using NumPy with a size of 500 × 500 pixels.

**Step 3:** Insert the text "DHIVYASHREE .R" onto the image using OpenCV's `cv2.putText()` function.

**Step 4:** Display the original input image using Matplotlib.

**Step 5:** Create a structuring element (kernel) of size 3 × 3 using NumPy.

**Step 6: Image Erosion**

- Apply erosion using `cv2.erode()`.
- Remove pixels from the boundaries of foreground objects.
- Display the eroded image.

**Step 7: Image Dilation**

- Apply dilation using `cv2.dilate()`.
- Add pixels to the boundaries of foreground objects.
- Display the dilated image.

**Step 8:** Compare the original, eroded and dilated images.

## Program

```python
# Step 1: Import the required libraries
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Step 2: Create a blank image
image = np.zeros((500, 500, 3), dtype=np.uint8)

# Step 3: Add text on the image using cv2.putText
font = cv2.FONT_HERSHEY_SIMPLEX

cv2.putText(image, 'DHIVYASHREE .R', (100, 250),
            font, 1, (255, 255, 255), 2, cv2.LINE_AA)

# Step 4: Display the input image
plt.figure()
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title("Input Image with Text")
plt.axis('off')
plt.show()

# Step 5: Create a simple square kernel (3x3)
kernel = np.ones((3, 3), np.uint8)

# Step 6: Apply erosion (shrinking effect)
eroded_image = cv2.erode(image, kernel, iterations=1)

# Display the eroded image
plt.figure()
plt.imshow(cv2.cvtColor(eroded_image, cv2.COLOR_BGR2RGB))
plt.title("Eroded Image")
plt.axis('off')
plt.show()

# Step 7: Apply dilation (expanding effect)
dilated_image = cv2.dilate(image, kernel, iterations=1)

# Display the dilated image
plt.figure()
plt.imshow(cv2.cvtColor(dilated_image, cv2.COLOR_BGR2RGB))
plt.title("Dilated Image")
plt.axis('off')
plt.show()
```


## Output

### 1. Original Image

<img width="389" height="410" alt="image" src="https://github.com/user-attachments/assets/e1ab1aa6-4f8e-4fc5-85c3-7e4be6df3867" />


### 2. Erosion

<img width="389" height="410" alt="image" src="https://github.com/user-attachments/assets/99ded35c-21e8-49ac-88fc-57ef7ec8cb16" />

### 3. Dilation

<img width="389" height="410" alt="image" src="https://github.com/user-attachments/assets/a529e9d6-c04c-45a7-8c2c-2ba3c1936659" />


## Result

Thus, the morphological operations Erosion and Dilation are successfully implemented using OpenCV in Python.
