# Deepfake Image Detector

A deep neural network based project to detect deep fake image generator

## Data set

We are using the dataset from the Kaggle challenge [here](https://www.kaggle.com/xhlulu/140k-real-and-fake-faces)

## How to run

We suggest you to use [Google Colab](https://colab.research.google.com/). 

To Download dataset directly from kaggle to googe drive you can use following code snippet.

Train the model or use the saved respective (.h5) model.

```python
"""
Step 1: Upload the API key file provided by kaggle to a location in google drive
Step 2: Set the config file as the environemnt variable
Step 5: Change working directory
Step 3: Get kaggle download link from kaggle 
"""

import os

# set kaggle config file directory
os.environ['KAGGLE_CONFIG_DIR'] = "/content/drive/MyDrive/Kaggle"

%cd /content/drive/MyDrive/Kaggle/

!kaggle datasets download -d xhlulu/140k-real-and-fake-faces --unzip
```

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License
[MIT](https://choosealicense.com/licenses/mit/)