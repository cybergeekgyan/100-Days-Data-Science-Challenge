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
```


### Step to run application:

```
Step 1:	Create the copy of the project.

Step 2: Open command prompt and change your current path to folder where you can find 'app.py' file.

Step 3: Create environment by command given below-
    conda create -name <environment name>

Step 4: Activate environment by command as follows-
    conda activate <environment name>

Step 5: Use command below to install required dependencies-
    python -m pip install -r requirements.txt

Step 6: Run application by command;
    python app.py

You will get url copy it and paste in browser.

Step 7: You have sample_data folder where you can get images to test.
```
