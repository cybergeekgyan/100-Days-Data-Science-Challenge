## Dog Breed Prediction App



## Objective

- Downloading the dataset and creating the model
- This model can be used to predict different breeds of dogs which can be further used by several NGOs working on saving animals 
- Optimizing different Hyperparameters in order to tune the model for Higher accuracy



## Workflow
```
1. Loading the Data from Kaggle
2. Load labels csv for labels that contain Image ID and Breed
3. Checking the breed count
4. One Hot Encoding on Labels Data Prediction Column
5. Load the Images and convert them into an Array and Normalize them
6. Checked the Shape and Size of the X and Y data
7. Building the Model Network Architechture
8. Split the data and fit into the model and create and Accuracy Plot
9. Evaluate the model for Accuracy score
10. Using the model for prediction
```


## Importing the Libraries
```Python

import numpy as np
import pandas as pd
import matplotlib.pyplot as plt

from tqdm import tqdm 
from keras.preprocessing import image
from sklearn.preprocessing import label_binarize
from sklearn.model_selection import train_test_split
from keras.model import Sequential
from keras.layers import Dense, Dropout, Flatten, Conv2D, MaxPool2D
from keras.optimizers import Adam

```



## Steps to run the application
