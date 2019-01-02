### face-emotion-detection

#### install the correct dependencies by runing below python user defined function

```python
def lib():
    !pip install numpy==1.15.4
    import numpy as np
    print("congratulations you are now using {} numpy version".format(np.__version__))
    !pip install tensorflow==1.12.0
    import tensorflow as tf
    print("congratulations you are now using {} tensorflow version".format(tf.__version__))
    !pip install keras==2.2.4
    import keras
    print("congratulations you are now using {} keras version".format(keras.__version__))
    !pip install opencv-python==3.4.3
    import cv2
    print("congratulations you are now using {} open cv version".format(cv2.__version__))
    print()
    print("You have what is takes to run this project, you are good to go"\
         " but you might need to install scipy library which is being used in utils/preprocessors.py file")
    
lib()

```

### Data-set

First thing first, let's see which data was used and what was inside it. 
The data consists of 48x48 pixel grayscale images of faces. The faces have been automatically registered so that the face is more or less centered and occupies about the same amount of space in each image. The task is to categorize each face based on the emotion shown in the facial expression in to one of seven categories 

label   |    category
------|----------------
0|Angry
1|Disgust
2|Fear
3|Happy
4|Sad
5|Surprise
6|Neutral

***
Here is what training data look like: 
![title](https://github.com/nirajdevpandey/face-emotion-detection/blob/master/data-set/training_data.PNG)

***
Here is what test data look like: 
![title](https://github.com/nirajdevpandey/face-emotion-detection/blob/master/data-set/test_data.PNG)

***
train.csv contains two columns, "emotion" and "pixels". The "emotion" column contains a numeric code ranging from 0 to 6, inclusive, for the emotion that is present in the image. The "pixels" column contains a string surrounded in quotes for each image. The contents of this string a space-separated pixel values in row major order. test.csv contains only the "pixels" column and your task is to predict the emotion column.

The training set consists of `28,709` examples. The public test set used for the leaderboard consists of `3,589` examples.

> This dataset was prepared by `Pierre-Luc Carrier` and `Aaron Courville`, as part of an ongoing research project. 

Trained model can be found in the repository itself. Special thanks to `B-IT-BOTS` robotics team for such a wonderful resources and the pretrained models. https://mas-group.inf.h-brs.de/?page_id=622

The credit goes to `B-IT-Bots graoup`. 

Please stay tuned, i'll upadte the readme very soon. Thanks 
***
