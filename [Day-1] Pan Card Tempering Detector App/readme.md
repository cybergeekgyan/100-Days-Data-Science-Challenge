## Pan Card Tempering Detection

## Objective

- Detection of Tempering of Pan Card using Computer Vision
- This will help the different organization in detecting whether the Pan Card provided by them by their Employees or Customers or Anyone is original or not

## WorkFlow

```
1. Get Images from Users
2. Check for Size and Format of the Image
3. Change Shape and Size of the Image according to the Original Image
4. Converting the Image to Grayscale
5. Finding the Similarity Index of the Images
6. Finding the Threshold of the Image
7. Finding the Contour and Grab those Contours using IMUTILS
8. Draw a Bounding Rectangle using these Contours
9. Plot Difference, Threshold Original and Tampered Image
10. Compare all the Images and Check the Similarity Score to Decide Tempering

```

### Importing the Libraries

```Python

from skimage.metrics import structural_similarity
import imutils
import cv2
from PIL import Image
import requests
