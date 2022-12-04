# Plant Disease Prediction 

In this project, We will create a Convolutional Neural Network which will be able to predict whether a plant is suffering from a disease. 
- Using Different layers and other hyperparameters for Building, Training, and Testing the classification model.

## Tech Stack

```
TensorFlow
Keras
```

## Objectives

  - HUMAN SOCIETY NEEDS TO INCREASE FOOD PRODUCTION BY AN ESTIMATED 70% BY 2050 TO FEED AN EXPECTED POPULATION SIZE THAT IS PREDICTED TO BE OVER 9 BILLION PEOPLE. 
  - CURRENTLY, INFECTIOUS DISEASES REDUCE THE POTENTIAL YIELD BY AN AVERAGE OF 40% WITH MANY FARMERS IN THE DEVELOPING WORLD EXPERIENCING YIELD LOSSES AS HIGH AS 100%. 
  - THE WIDESPREAD DISTRIBUTION OF SMARTPHONES AMONG CROP GROWERS AROUND THE WORLD WITH AN EXPECTED 5 BILLION SMARTPHONES BY 2020 OFFERS THE POTENTIAL OF TURNING THE SMARTPHONE INTO A VALUABLE TOOL FOR DIVERSE COMMUNITIES GROWING FOOD. 
  - ONE POTENTIAL APPLICATION IS THE DEVELOPMENT OF MOBILE DISEASE DIAGNOSTICS THROUGH MACHINE LEARNING AND BIG DATA.


## Methodology

- Mounting Google Drive on Colab Notebok
- Visualising the Images that we will be working on
- Finding out the mean of the Images and Resizing all Images accordingly.
- Converting the Images into a Numpy array and normalise them.
- Checking Class Imbalance
- Splitting the data and performing One-Hot Encoding
- Creating the Model Architecture, Compiling the model and then fitting it
- Plotting the Accuracy and loss against each Epoch
- Preprocessing the Test Data and Making predictions on it.
- Visualising the Original and Predicted labels for the test Images

## Importing the Libraries

```Python

import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
from matplotlib.image import imread
import cv2
import random
import os
from os import listdir from PIL import Image
from sklearn.preprocessing import label_binarize, LabelBinarizer
from keras.preprocessing import image
from keras.preprocessing. image import img_to_array, array_to_img
from keras.optimizers import Adam
from keras.models import Sequential
from keras. layers import Conv2D, MaxPooling2D
from keras.layers import Activation, Flatten, Dropout, Dense
from sklearn.model_selection import train_test_split
from keras.models import model_from_json
from keras.utils import to_categorical
```

```Python
# Plotting 12 images to check dataset
plt.figure(figsize=(12,12))
path = "/content/drive/My Drive/Plant_images pianalytix/Potato Early blight"
for i in range(1,17):
pit. subplot (4,4,i)
plt.tight_layout ()
rand_img = imread(path +'/*+ random.choice(sorted(os.listdir (path))))
pit.imshow(rand_img)
plt.xlabel(rand_img.shape[1], fontsize = 10)#width of image
pit.ylabel(rand_img.shape[0], fontsize = 10)#height of image


#Converting Images to array
def convert_image_to_array(image_dir):
try:
image = cv2.imread(image_dir)
if image is not None :
image = cv2.resize(image, (256,256))
#image = cv2.cvtColor (image, cv2.COLOR_BGR2GRAY)
return img_to_array(image)
else :
return np.array([])
except Exception as e:
print (f"Error : {e)")
return None


# Visualize the number of classes count
label_counts = pd.DataFrame (label_list).value_counts ()
label_counts. head()


label_list = np.array(label_list)
label_list. shape

# Saving the Model

model.save("/content/drive/My Drive/plant_disease.h5")
# serialize model to json
json_model = model.to_json()
#save the model architecture to JSON file with open(*/content/drive/My Drive/plant model.json', 'w') as json_file:
json_file.write(json_model)
#saving the weights of the model
model. save_weights('/content/drive/My Drive/plant model weights.h5')


#Plot the training history
plt.figure(figsize= (12, 5))
plt.plot(history.history['accuracy'], colors'r')
plt.plot (history.history ['val_accuracy'], color='b')
plt.title('Model Accuracy")
plt.ylabel('Accuracy")
plt.xlabel('Epochs")
plt.legend(['train',
'val'1)
plt.show()


# Plotting the acccuracy of the model for the training history
print("(INFO] Calculating model accuracy")
scores = model.evaluate(x_test, y_test)
print (f"Test Accuracy: {scores [1]*100}")



```
