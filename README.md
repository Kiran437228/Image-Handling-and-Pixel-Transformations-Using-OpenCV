# Image-Handling-and-Pixel-Transformations-Using-OpenCV 

## AIM:
Write a Python program using OpenCV that performs the following tasks:

1) Read and Display an Image.  
2) Adjust the brightness of an image.  
3) Modify the image contrast.  
4) Generate a third image using bitwise operations.

## Software Required:
- Anaconda - Python 3.7
- Jupyter Notebook (for interactive development and execution)

## Algorithm:
### Step 1:
Load an image from your local directory and display it.

### Step 2:
Create a matrix of ones (with data type float64) to adjust brightness.

### Step 3:
Create brighter and darker images by adding and subtracting the matrix from the original image.  
Display the original, brighter, and darker images.

### Step 4:
Modify the image contrast by creating two higher contrast images using scaling factors of 1.1 and 1.2 (without overflow fix).  
Display the original, lower contrast, and higher contrast images.

### Step 5:
Split the image (boy.jpg) into B, G, R components and display the channels

## Program Developed By:
- **Name:** Kiran Kumar CS
- **Register Number:** 212224240076

  ### Ex. No. 01

1. Read the image ('Eagle_in_Flight.jpg') using OpenCV imread() as a grayscale image.
```PYTHON
import cv2
import matplotlib.pyplot as plt
```

Read the image using OpenCV
```
img = cv2.imread('VIN.jpeg', cv2.IMREAD_COLOR)
```
Convert BGR (OpenCV's default) to RGB (Matplotlib's expected color order)#
```
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
```
Display the image using Matplotlib
```
plt.imshow(img_rgb, cmap='viridis')  # You can change 'viridis' to another cmap or use None for RGB images
plt.title("Original Image")
plt.axis('off')  # Removes axis ticks and labels
plt.show()
```
Load the image
```
image = cv2.imread('VIN.jpeg')
```
Convert BGR (OpenCV's default) to RGB (Matplotlib's expected color order)
```
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
img_rgb.shape
(1536, 941, 3)
```
Draw a line from top-left to bottom-right
```
line_img = cv2.line(img_rgb, (0, 0), (768, 600), (255, 0, 0), 2) # cv2.line(image, start_point, end_point, color, thickness)
plt.imshow(line_img, cmap='viridis')  
plt.title("Image with Line")
plt.axis('off')  
plt.show()
```
Load the image
```
image = cv2.imread('VIN.jepg')
```
Convert BGR (OpenCV's default) to RGB (Matplotlib's expected color order)
```
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
img_rgb.shape
(1536, 941, 3)
circle_img = cv2.circle(img_rgb,(400,300),150,(255,0,0),10) # cv2.circle(image, center, radius, color, thickness)
plt.imshow(circle_img, cmap='viridis')  
plt.title("Image with Circle")
plt.axis('off')  
plt.show()
```
Load the image
```
image = cv2.imread('VIN.jpeg')
```
Convert BGR (OpenCV's default) to RGB (Matplotlib's expected color order)
```
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
img.shape
(1536, 941, 3)
```
Draw a rectangle around the Whole image
```
rectangle_img = cv2.rectangle(img_rgb, (0, 0), (768, 600), (0, 0, 255), 10)  # cv2.rectangle(image, start_point, end_point, color, thickness)
plt.imshow(rectangle_img, cmap='viridis')  
plt.title("Image with Rectangle")
plt.axis('off')  
plt.show()
```

Load the image
```
image = cv2.imread('VIN.jpeg')
```
Convert BGR (OpenCV's default) to RGB (Matplotlib's expected color order)
```
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
```
Add text to the image
```
text_img = cv2.putText(img_rgb, "Opencv Drawing", (10, 35), cv2.FONT_HERSHEY_SIMPLEX, 1, (255, 255, 255), 10)  ## cv2.putText(image, text, position, font, font_scale, color, thickness)
plt.imshow(text_img, cmap='viridis')  
plt.title("Image with Text")
plt.axis('off')  
plt.show()
```
Load the image
```
image = cv2.imread('VIN.jpeg') 
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
```



## Output:

## original image
<img width="636" height="382" alt="image" src="https://github.com/user-attachments/assets/064d6439-93f7-4756-8e65-fe2dc2fecbb0" />


## Image with Line
<img width="620" height="382" alt="image" src="https://github.com/user-attachments/assets/ed69f6a9-9d7e-4af0-bfb2-5a2633f158bc" />

## Image with Circle
<img width="620" height="386" alt="image" src="https://github.com/user-attachments/assets/7b88fa49-8d42-4487-a989-bba58e657568" />


## Image with Rectangle
<img width="627" height="383" alt="image" src="https://github.com/user-attachments/assets/e5ecf087-1a88-432e-b10c-c529b4380696" />


## Image with Text
<img width="625" height="383" alt="image" src="https://github.com/user-attachments/assets/edb11ee9-2407-49d3-af68-ee24c5d7fc05" />


## Original RGB Image
<img width="625" height="386" alt="image" src="https://github.com/user-attachments/assets/bd9eaf3d-177d-49a1-9daa-2ed4914e59cc" />


## HSV Image
<img width="622" height="375" alt="image" src="https://github.com/user-attachments/assets/5fd951c7-910a-424b-aa4b-d6bee29d7766" />


## Grayscale Image
<img width="622" height="380" alt="image" src="https://github.com/user-attachments/assets/28c064ec-e85c-4185-9892-7cd74131452b" />


## HSV to RGB Image
<img width="627" height="377" alt="image" src="https://github.com/user-attachments/assets/7b4623af-3f12-4a24-883a-64f1521d9c70" />


## Image with 300x300 White Block
<img width="617" height="385" alt="image" src="https://github.com/user-attachments/assets/d91a36d1-27fc-4fd8-90fd-070f60d3a61e" />


## Resized Image (Half Size)
<img width="595" height="496" alt="image" src="https://github.com/user-attachments/assets/008b9123-3a03-4ebd-a4ed-e9bbc186e2a9" />



## Cropped Region of Interest (ROI)
<img width="465" height="496" alt="image" src="https://github.com/user-attachments/assets/26a481cb-8831-401e-aec1-56a390a69097" />


## Flipped Horizontally
<img width="636" height="385" alt="image" src="https://github.com/user-attachments/assets/62adc097-e1a8-4c52-a66c-f54eb31ae881" />


## Flipped Vertically
<img width="617" height="382" alt="image" src="https://github.com/user-attachments/assets/595f8002-d2e0-470c-a743-c9275ade3cfd" />



## Result:
Thus, the images were read, displayed, brightness and contrast adjustments were made, and bitwise operations were performed successfully using the Python program.

