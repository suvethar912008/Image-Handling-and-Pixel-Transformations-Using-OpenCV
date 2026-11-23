# Image-Handling-and-Pixel-Transformations-Using-OpenCV
# Name : Suvetha R
# Register Number: 212225220113
# Experiment: Image Handling and Pixel Transformations Using OpenCV

# AIM

To perform image handling and pixel transformations using Python and OpenCV, including reading and displaying images, drawing shapes, adding text, color space conversion, pixel manipulation, image resizing, cropping, flipping, and saving the modified image.

# SOFTWARE REQUIRED

• Python 
• OpenCV 
• Matplotlib 
• Jupyter Notebook 
• Anaconda (optional)

# INSTALLATION

Install the required libraries using the following command:

pip install opencv-contrib-python-headless matplotlib

# ALGORITHM
# Step 1: Read and Display an Image
   Import OpenCV and Matplotlib libraries. Read an image from the local directory using cv2.imread().          Convert the image from BGR to RGB. Display the original image using Matplotlib.

# Step 2: Draw Shapes and Add Text
  Draw a line from the top-left to the bottom-right of the image. Draw a circle at the center of the          image. Draw a rectangle around the image. Add the text "OpenCV Drawing" at the top-left corner.

# Step 3: Color Space Conversion
Convert the RGB image to HSV and display it. Convert the RGB image to grayscale and display it. Convert the RGB image to YCrCb and display it. Convert the HSV image back to RGB and display it.

# Step 4: Pixel Manipulation
Access and print the pixel value at coordinates (100, 100). Change the pixel at coordinates (200, 200) to white. Modify a 300 × 300 region of the image to white. Display the modified image.

# Step 5: Image Resizing
Read the original image. Resize the image to half its original width and height. Display the resized image.

# Step 6: Image Cropping
Read the original image. Extract a 300 × 300 region of interest starting at (50, 50). Display the cropped image.

# Step 7: Image Flipping
Flip the original image horizontally. Flip the original image vertically. Display both flipped images.

# Step 8: Save the Final Modified Image
Save the modified image in the local directory using cv2.imwrite(). Verify that the image has been saved successfully.

# PROGRAM
# Step 1: Read and Display an Image
```
import cv2
import matplotlib.pyplot as plt

# Read the image using OpenCV

img = cv2.imread('fish.jpeg', cv2.IMREAD_COLOR)


# Convert BGR (OpenCV's default) to RGB (Matplotlib's expected color order)

img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)

# Display the image using Matplotlib
plt.imshow(img_rgb, cmap='viridis')  # You can change 'viridis' to another cmap or use None for RGB images
plt.title("Original Image")
plt.axis('off')  # Removes axis ticks and labels
plt.show()
```

# Step 2: Draw Shapes and Add Text

# 2.1 Draw a Line
```
# Load the image
image = cv2.imread('fish.jpeg') 

# Convert BGR (OpenCV's default) to RGB (Matplotlib's expected color order)
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
img_rgb.shape

# Draw a line from top-left to bottom-right
line_img = cv2.line(img_rgb, (0, 0), (768, 600), (255, 0, 0), 2) # cv2.line(image, start_point, end_point, color, thickness)

# Display the image
plt.imshow(line_img, cmap='viridis')  
plt.title("Image with Line")
plt.axis('off')  
plt.show()

```
# 2.2 Draw a Circle
```
# Load the image
image = cv2.imread('fish.jpeg') 

# Convert BGR (OpenCV's default) to RGB (Matplotlib's expected color order)
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)

img_rgb.shape

circle_img = cv2.circle(img_rgb,(400,300),150,(255,0,0),10) # cv2.circle(image, center, radius, color, thickness)

# Display the image
plt.imshow(circle_img, cmap='viridis')  
plt.title("Image with Circle")
plt.axis('off')  
plt.show()
```
# 2.3 Draw a Rectangle
```
# Load the image
image = cv2.imread('Qno. 1.jpg') 

# Convert BGR (OpenCV's default) to RGB (Matplotlib's expected color order)
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)

img.shape

# Draw a rectangle around the Whole image
rectangle_img = cv2.rectangle(img_rgb, (0, 0), (768, 600), (0, 0, 255), 10)  # cv2.rectangle(image, start_point, end_point, color, thickness)

# Display the image
plt.imshow(rectangle_img, cmap='viridis')  
plt.title("Image with Rectangle")
plt.axis('off')  
plt.show()
```

# 2.4 Add Text to the Image
```
# Load the image
image = cv2.imread('Qno. 1.jpg') 

# Convert BGR (OpenCV's default) to RGB (Matplotlib's expected color order)
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)

# Add text to the image
text_img = cv2.putText(img_rgb, "OpenCV Drawing", (10, 30), cv2.FONT_HERSHEY_SIMPLEX, 1, (255, 255, 255), 10)  ## cv2.putText(image, text, position, font, font_scale, color, thickness)


# Display the image
plt.imshow(text_img, cmap='viridis')  
plt.title("Image with Text")
plt.axis('off')  
plt.show()
Step 3: Color Space Conversion
# Load the image
image = cv2.imread('fish.jpeg') 

image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)

# Original RGB Image
plt.imshow(image_rgb)
plt.title("Original RGB Image")
plt.axis("off")

# Convert RGB to HSV
image_hsv = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2HSV)

# HSV Image
plt.imshow(image_hsv)
plt.title("HSV Image")
plt.axis("off")

# Convert RGB to GRAY
image_gray = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2GRAY)

# Grayscale Image
plt.imshow(image_gray, cmap='gray')
plt.title("Grayscale Image")
plt.axis("off")

# Convert RGB to YCrCb
image_ycrcb = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2YCrCb)

# YCrCb Image
plt.imshow(image_ycrcb)
plt.title("YCrCb Image")
plt.axis("off")

# Convert HSV back to RGB
image_hsv_to_rgb = cv2.cvtColor(image_hsv, cv2.COLOR_HSV2RGB)

plt.imshow(image_hsv_to_rgb)
plt.title("HSV to RGB Image")
plt.axis("off")
```

# Step 4: Pixel Manipulation
```
# Modify a block of pixels (300x300) to white, starting from (200, 200)
image[200:500, 200:500] = [255, 255, 255]  # Rows: 200-499, Columns: 200-499

# Convert BGR to RGB for displaying with Matplotlib
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)

# Display the modified image
plt.imshow(image_rgb)
plt.title("Image with 300x300 White Block")
plt.axis("off")
plt.show()
```

# Step 5: Image Resizing
```
image = cv2.imread('fish.jpeg') 
image.shape

# Resize the image to half its size
resized_image = cv2.resize(image, (768 // 2, 600 // 2))  # (new_width, new_height)

# Convert BGR to RGB for displaying with Matplotlib
resized_image_rgb = cv2.cvtColor(resized_image, cv2.COLOR_BGR2RGB)

resized_image_rgb.shape

# Display the resized image
plt.imshow(resized_image_rgb)
plt.title("Resized Image (Half Size)")
plt.axis("off")
plt.show()

```
# Step 6: Image Cropping
```
# Load the image
image = cv2.imread('fish.jpeg')

image.shape

# Crop a 300x300 region starting from (50, 50)
roi = image[50:350, 50:350]  # Rows: 50-349, Columns: 50-349

# Convert BGR to RGB for displaying with Matplotlib
roi_rgb = cv2.cvtColor(roi, cv2.COLOR_BGR2RGB)

# Display the cropped region (ROI)
plt.imshow(roi_rgb)
plt.title("Cropped Region of Interest (ROI)")
plt.axis("off")
plt.show()
```

# Step 7: Image Flipping
```
# Load the image
image = cv2.imread('fish.jpeg')

# Flip the image horizontally (left-right)
flipped_horizontally = cv2.flip(image, 1)

# Convert BGR to RGB for displaying with Matplotlib
flipped_horizontally_rgb = cv2.cvtColor(flipped_horizontally, cv2.COLOR_BGR2RGB)

# Horizontal flip
plt.imshow(flipped_horizontally_rgb)
plt.title("Flipped Horizontally")
plt.axis("off")

# Flip the image vertically (up-down)
flipped_vertically = cv2.flip(image, 0)

# Convert BGR to RGB for displaying with Matplotlib
flipped_vertically_rgb = cv2.cvtColor(flipped_vertically, cv2.COLOR_BGR2RGB)

# Vertical flip
plt.imshow(flipped_vertically_rgb)
plt.title("Flipped Vertically")
plt.axis("off")
```

# OUTPUT

# The following outputs are obtained:

# 1. Original image displayed using OpenCV and Matplotlib.


<img width="417" height="410" alt="image" src="https://github.com/user-attachments/assets/aca2604b-0b65-4892-aa7f-4df877ca4722" />


# 2. Image with a line drawn from the top-left to the bottom-right.


<img width="377" height="407" alt="image" src="https://github.com/user-attachments/assets/9f413b43-4c09-4f70-a2b0-495592b91955" />


# 3. Image with a circle at the center.

<img width="410" height="412" alt="image" src="https://github.com/user-attachments/assets/825b2e07-0481-4a1a-8713-fb238fb76635" />


# 4. Image with a rectangle around its boundary.

<img width="382" height="390" alt="image" src="https://github.com/user-attachments/assets/e548845d-2592-4bf1-9953-c07074e3a356" />


# 5. Image with the text "OpenCV Drawing".

<img width="382" height="402" alt="image" src="https://github.com/user-attachments/assets/9e4806ca-4d34-4ffa-90be-042e7ffc4bbc" />


# 6. HSV, grayscale, and YCrCb color space conversions.


<img width="380" height="386" alt="image" src="https://github.com/user-attachments/assets/f59df828-c9b6-4a7c-8127-526013a197d3" />


<img width="365" height="392" alt="image" src="https://github.com/user-attachments/assets/bf26c9f0-0422-451a-9ca2-6227428af0e7" />


<img width="382" height="398" alt="image" src="https://github.com/user-attachments/assets/39c31819-c78a-4fb4-8261-3aaea672f550" />

# 7. Image converted from HSV back to RGB.


<img width="387" height="415" alt="image" src="https://github.com/user-attachments/assets/cc281aef-5afa-46d1-85ec-b7809b46678c" />

# 8. Pixel value displayed and a white region added to the image.

<img width="372" height="392" alt="image" src="https://github.com/user-attachments/assets/ef89b9c8-e6fd-4bef-b080-6ef0e55f3939" />


# 9. Image resized to half its original dimensions.


<img width="475" height="395" alt="image" src="https://github.com/user-attachments/assets/8635d3cc-31ab-4333-8c6e-219c724b4129" />


#10. Cropped region of interest displayed.


<img width="377" height="391" alt="image" src="https://github.com/user-attachments/assets/86754484-e37f-41fa-972b-4a222f3a5a87" />

#11. Horizontally flipped image displayed.

<img width="367" height="396" alt="image" src="https://github.com/user-attachments/assets/4929270c-e3f8-4619-985d-f830befc74eb" />



# RESULT 
Thus, image handling and pixel transformations were performed using Python, OpenCV, and Matplotlib. The experiment demonstrated image reading, shape drawing, text insertion, color space conversion, pixel manipulation, image resizing, cropping, flipping, and saving.
