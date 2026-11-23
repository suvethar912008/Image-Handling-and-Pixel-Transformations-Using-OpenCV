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


# Step 2: Draw Shapes and Add Text
# 2.1 Draw a Line

# 2.2 Draw a Circle
# 2.3 Draw a Rectangle

# 2.4 Add Text to the Image

# Step 4: Pixel Manipulation

# Step 5: Image Resizing

# Step 6: Image Cropping

# Step 7: Image Flipping

# OUTPUT

# The following outputs are obtained:

# 1. Original image displayed using OpenCV and Matplotlib.

# 2. Image with a line drawn from the top-left to the bottom-right.

# 3. Image with a circle at the center.
# 4. Image with a rectangle around its boundary.

# 5. Image with the text "OpenCV Drawing".

# 6. HSV, grayscale, and YCrCb color space conversions.

# 7. Image converted from HSV back to RGB.

# 8. Pixel value displayed and a white region added to the image.

# 9. Image resized to half its original dimensions.

#10. Cropped region of interest displayed.

#RESULT 
Thus, image handling and pixel transformations were performed using Python, OpenCV, and Matplotlib. The experiment demonstrated image reading, shape drawing, text insertion, color space conversion, pixel manipulation, image resizing, cropping, flipping, and saving.
