# rock-paper-scissor
This repo is used to build your own robo.

#GETTING OUR DATA
The basics of any machine learning is its data. So here GET DATA is used for generation of own data.

```
python getData label startIndex endIndex
```

This will essential to make a folder of name label and store (endIndex-startIndex+1) images 

#TRAIN OUR DATA
Next we move to training our model. Here we have used the DenseNet model available from keras.applications as a base model to work upon. It is followed by a MaxPooling Layer which is Flattened and finally run through a Dense Layer with 3 Output Neurons and SoftMax Activation to predict our output from 3 Classes Rock, Paper and Scissor.
Here we have train.py which is run like this <br>

```
python train.py pathToImages
```
This will iterate over the files produced by getData.py and train our Model. Once trained the Model architecture is stored in a json file and the weights are stored in .h5 file.
Due to lack of computational power I had to train the model using Google Colab by setting Hardware Accelration to GPU.

#Let's play
Now we load our Model Architecture and weights and finally play the game. 
Make sure model.h & model.json are in same folder in which play.py

```
python play.py
```
#Requirements
keras
Tensorflow 
opencv

It is good to use anaconda for package management.
