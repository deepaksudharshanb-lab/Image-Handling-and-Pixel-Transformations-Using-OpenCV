# Image-Handling-and-Pixel-Transformations-Using-OpenCV 
## Name:Deepak sudharshan.b
## register number:212225230045
## AIM:
Write a Python program using OpenCV that performs the following tasks:

1) Read and Display an Image, and draw basic shapes/text on it.  
2) Convert the image between different color spaces (HSV, Grayscale, YCrCb).  
3) Access and modify individual pixels/pixel blocks of an image.  
4) Resize, crop, and flip an image.  
5) Save the final modified image to the local directory.

## Software Required:
- Anaconda - Python 3.7
- Jupyter Notebook (for interactive development and execution)

## Algorithm:

### Step 1:
Load an image from your local directory and display it.

### Step 2:
- Draw a line from the top-left to the bottom-right of the image.
- Draw a circle at the center of the image.
- Draw a rectangle around a specific region of interest in the image.
- Add the text "OpenCV Drawing" at the top-left corner of the image.

### Step 3:
- Convert the image from RGB to HSV and display it.
- Convert the image from RGB to GRAY and display it.
- Convert the image from RGB to YCrCb and display it.
- Convert the HSV image back to RGB and display it.

### Step 4:
- Access and print the value of the pixel at coordinates (100, 100).
- Modify the color of the pixel at (200, 200) to white.

### Step 5:
Resize the original image to half its size and display it.

### Step 6:
Crop a region of interest (ROI) from the image (e.g., a 100x100 pixel area starting at (50, 50)) and display it.

### Step 7:
- Flip the original image horizontally and display it.
- Flip the original image vertically and display it.

### Step 8:
Save the final modified image to your local directory.

## Program Developed By:
- **Name:** B. Deepak Sudharshan  
- **Register Number:** 212225230045

  ### Ex. No. 01

#### 0. Import required libraries
```python
import cv2
import matplotlib.pyplot as plt
```

#### 1. Read and display the original image
```python
# Read the image using OpenCV
img = cv2.imread('Qno. 1.jpg', cv2.IMREAD_COLOR)

# Convert BGR (OpenCV's default) to RGB (Matplotlib's expected color order)
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)

# Display the image using Matplotlib
plt.imshow(img_rgb)
plt.title("Original Image")
plt.axis('off')
plt.show()
```
<img width="697" height="447" alt="image" src="https://github.com/user-attachments/assets/25125afa-811f-4326-ac79-7c6be9ed8ab6" />



#### 2. Draw a line, circle, rectangle, and text on the image

**a) Draw a line from the top-left to the bottom-right of the image**
```python
image = cv2.imread('Qno. 1.jpg')
img_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)

line_img = cv2.line(img_rgb, (0, 0), (768, 600), (0, 255, 255), 4)  # cyan line

plt.imshow(line_img)
plt.title("Image with Line")
plt.axis('off')
plt.show()
```
<img width="666" height="436" alt="image" src="https://github.com/user-attachments/assets/3ecc326f-dbe0-45e9-947c-71b66145839c" />


**b) Draw a circle at the center of the image**
```python
image = cv2.imread('Qno. 1.jpg')
img_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)

circle_img = cv2.circle(img_rgb, (350, 250), 120, (255, 0, 255), 8)  # magenta circle

plt.imshow(circle_img)
plt.title("Image with Circle")
plt.axis('off')
plt.show()
```
<img width="677" height="436" alt="image" src="https://github.com/user-attachments/assets/eb71bb3b-9535-492b-8957-6fc076ea899f" />


**c) Draw a rectangle around a region of interest**
```python
image = cv2.imread('Qno. 1.jpg')
img_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)

rectangle_img = cv2.rectangle(img_rgb, (20, 20), (748, 580), (0, 255, 0), 6)  # green rectangle

plt.imshow(rectangle_img)
plt.title("Image with Rectangle")
plt.axis('off')
plt.show()
```
<img width="692" height="427" alt="image" src="https://github.com/user-attachments/assets/b045dfe1-60da-4898-9f17-bcc8b972f04d" />


**d) Add the text "OpenCV Drawing" at the top-left corner**
```python
image = cv2.imread('Qno. 1.jpg')
img_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)

text_img = cv2.putText(img_rgb, "OpenCV Drawing", (10, 40), cv2.FONT_HERSHEY_SIMPLEX, 1.3, (255, 165, 0), 3)  # orange text

plt.imshow(text_img)
plt.title("Image with Text")
plt.axis('off')
plt.show()
```
<img width="706" height="426" alt="image" src="https://github.com/user-attachments/assets/00988a6b-a79b-4415-8b85-e266653ef692" />


#### 3. Convert the image between color spaces
```
python
image = cv2.imread('Qno. 1.jpg')
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)

# Original RGB Image
plt.imshow(image_rgb)
plt.title("Original RGB Image")
plt.axis("off")
plt.show()
```
<img width="687" height="441" alt="image" src="https://github.com/user-attachments/assets/d3afb235-a890-45b4-a772-7e36f51f494a" />



```
# Convert RGB to HSV
image_hsv = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2HSV)
plt.imshow(image_hsv)
plt.title("HSV Image")
plt.axis("off")
plt.show()
```
<img width="673" height="433" alt="image" src="https://github.com/user-attachments/assets/bebdfe53-c4e5-4437-a779-35fc46ad0fce" />



```
# Convert RGB to GRAY
image_gray = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2GRAY)
plt.imshow(image_gray, cmap='gray')
plt.title("Grayscale Image")
plt.axis("off")
plt.show()
```
<img width="663" height="432" alt="image" src="https://github.com/user-attachments/assets/03f7e35b-59de-4d04-97ca-4ca83dea697b" />
```
# Convert RGB to YCrCb
image_ycrcb = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2YCrCb)
plt.imshow(image_ycrcb)
plt.title("YCrCb Image")
plt.axis("off")
plt.show()
```
<img width="695" height="433" alt="image" src="https://github.com/user-attachments/assets/5f5d61ba-7576-4683-9ff1-188c276b41d5" />
```
# Convert HSV back to RGB
image_hsv_to_rgb = cv2.cvtColor(image_hsv, cv2.COLOR_HSV2RGB)
plt.imshow(image_hsv_to_rgb)
plt.title("HSV to RGB Image")
plt.axis("off")
plt.show()
```
<img width="717" height="430" alt="image" src="https://github.com/user-attachments/assets/06237163-71ac-4df5-936b-de8b22fcd366" />


#### 4. Access and modify pixel values
```python
image = cv2.imread('Qno. 1.jpg')

# Access and print the value of the pixel at (100, 100)
pixel_value = image[100, 100]
print("Pixel value at (100, 100):", pixel_value)

# Modify the color of the pixel at (200, 200) to white
image[200, 200] = [255, 255, 255]

# Modify a block of pixels (250x250) to a color, starting from (150, 150)
image[150:400, 150:400] = [128, 0, 255]  # purple-ish block (BGR order)

# Convert BGR to RGB for displaying with Matplotlib
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)

# Display the modified image
plt.imshow(image_rgb)
plt.title("Image with Modified Pixels")
plt.axis("off")
plt.show()
```
<img width="646" height="450" alt="image" src="https://github.com/user-attachments/assets/9501691a-bfe9-41fe-9b53-5a4920794491" />

#### 5. Resize the image to half its size
```python
image = cv2.imread('Qno. 1.jpg')

# Resize the image to half of its original size
resized_image = cv2.resize(image, (image.shape[1] // 2, image.shape[0] // 2))

# Convert BGR to RGB for displaying with Matplotlib
resized_image_rgb = cv2.cvtColor(resized_image, cv2.COLOR_BGR2RGB)

# Display the resized image
plt.imshow(resized_image_rgb)
plt.title("Resized Image (Half Size)")
plt.axis("off")
plt.show()
```
<img width="610" height="528" alt="image" src="https://github.com/user-attachments/assets/d183dd85-5d49-4da9-9ec7-9de5ac746c65" />

#### 6. Crop a region of interest (ROI)
```python
image = cv2.imread('Qno. 1.jpg')

# Crop a 100x100 region starting from (50, 50)
roi = image[50:150, 50:150]  # Rows: 50-149, Columns: 50-149

# Convert BGR to RGB for displaying with Matplotlib
roi_rgb = cv2.cvtColor(roi, cv2.COLOR_BGR2RGB)

# Display the cropped region (ROI)
plt.imshow(roi_rgb)
plt.title("Cropped Region of Interest (ROI)")
plt.axis("off")
plt.show()
```
<img width="488" height="525" alt="image" src="https://github.com/user-attachments/assets/ac42e5bb-b72e-48e0-939f-8ded3e1ca352" />

#### 7. Flip the image horizontally and vertically
```python
image = cv2.imread('Qno. 1.jpg')

# Flip the image horizontally (left-right)
flipped_horizontally = cv2.flip(image, 1)
flipped_horizontally_rgb = cv2.cvtColor(flipped_horizontally, cv2.COLOR_BGR2RGB)

plt.imshow(flipped_horizontally_rgb)
plt.title("Flipped Horizontally")
plt.axis("off")
plt.show()
```
<img width="681" height="467" alt="image" src="https://github.com/user-attachments/assets/337d2a86-8e40-4119-be11-4e32dc059454" />
```

# Flip the image vertically (up-down)
flipped_vertically = cv2.flip(image, 0)
flipped_vertically_rgb = cv2.cvtColor(flipped_vertically, cv2.COLOR_BGR2RGB)

plt.imshow(flipped_vertically_rgb)
plt.title("Flipped Vertically")
plt.axis("off")
plt.show()
```
<img width="633" height="425" alt="image" src="https://github.com/user-attachments/assets/7ffb754e-934b-4155-9b49-814ef2ad625c" />


#### 8. Save the final modified image
```python
# Save the final modified image to your local directory
cv2.imwrite('final_output.jpg', image)
print("Saved final_output.jpg")
```

## Output:
- **i)** Original image displayed with a line, circle, rectangle, and text drawn on it.  
- **ii)** Image displayed in HSV, Grayscale, and YCrCb color spaces, and converted back from HSV to RGB.  
- **iii)** Pixel value at (100, 100) printed, and pixel(s) modified to a new color.  
- **iv)** Resized (half-size), cropped (ROI), and flipped (horizontal & vertical) versions of the image displayed.  
  

## Result:
Thus, the image was read and displayed, basic shapes and text were drawn on it, color space conversions were performed, pixel values were accessed and modified, and the image was resized, cropped, flipped, and saved successfully using Python and OpenCV.
