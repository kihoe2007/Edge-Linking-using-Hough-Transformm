# Edge-Linking-using-Hough-Transformm
## Aim:
To write a Python program to detect the lines using Hough Transform.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:

Import all the necessary modules for the program.
### Step2:

Load a image using imread() from cv2 module.
### Step3:

Convert the image to grayscale.
### Step4:

Using Canny operator from cv2,detect the edges of the image.
### Step5:

Using the HoughLinesP(),detect line co-ordinates for every points in the images.Using For loop,draw the lines on the found co-ordinates.Display the image.
## Output

### Input image and grayscale image
```
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert image to RGB for displaying
plt.title("Input Image")
plt.axis('off')
```
<img width="770" height="570" alt="image" src="https://github.com/user-attachments/assets/78e3e2e5-3afa-4454-bcf5-02d313153f34" />

### Canny Edge detector output

```
plt.imshow(gray_image, cmap='gray')
plt.title("Grayscale Image")
plt.axis('off')
```
<img width="1329" height="687" alt="image" src="https://github.com/user-attachments/assets/8e11e552-5eae-46ea-ac6b-971f7047eadc" />
```
# Canny Edge Detector output
plt.imshow(edges, cmap='gray')
plt.title("Canny Edge Detector")
plt.axis('off')
```


<img width="724" height="561" alt="image" src="https://github.com/user-attachments/assets/103f4f9a-b50f-4a04-8ae7-a379e2957e46" />


### Display the result of Hough transform
```
lines = cv2.HoughLinesP(edges, 1, np.pi / 180, 100, minLineLength=50, maxLineGap=10)
for line in lines:
    x1, y1, x2, y2 = line[0]  # Unpacking the line coordinates
    cv2.line(image, (x1, y1), (x2, y2), (0, 255, 0), 2)  # Draw green lines with thickness of 2
# Display the result of Hough Transform (Image with lines)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Image with lines drawn
plt.title("Result of Hough Transform")
plt.axis('off')
```

<img width="747" height="569" alt="image" src="https://github.com/user-attachments/assets/749513d9-b521-41cb-b9d4-2491c875a5d9" />

