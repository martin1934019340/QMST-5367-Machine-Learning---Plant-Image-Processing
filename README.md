# QMST 5367 Machine Learning - Plant Image Processing

## TEAM 5 GROUP MEMBERS:
### Chi Bao, Christian Martin, Taja Castilleja, Shainan Agrawal


##### Project Description:
###### The goal of the project was to use machine learning to identify 5 different types of plants: potato, tomato, raspberry, poison ivy, and bell peppers. We used datasets of plant leaf images to train our model, which is a supervised model since the user will know the correct type of a plant. Training an algorithm to identify types of plants removes the effort and time to research plant information and type online. For this project, we used convolutional neural networks to build our model and trained our model to classify the images accurately. We found that as more images are added to the training dataset, the more accurate the model becomes. 

##### Case Description: 
###### We are a start-up company that is developing an app where users take pictures of plants and the app will identify the plants using machine learning. We have premium and free services, where the premium service includes expanded plant image recognition. Some of our target customers are Boy Scout or Girl Scout groups, avid hikers, forest rangers and other personnel that work in parks, forests, and other national settings, and even hobbyist foragers who want to improve their leisure activity experience.

##### Useful features from the data and description of the features:
###### We created a customized dataset of plant images that includes images of plants classified into 5 categories. We chose the image based on the following:

######   ·  	Image Quality: The images we chose for our model have good quality with low memory. Using high quality photos helps improve feature extraction and optimization to properly train our model.
######   ·  	Single Leaf and Grouped Leaves: We chose a combination of images in our dataset such that there were single leaves in some of the images and multiple leaves of the same type grouped together. This helped us train our model better.
######   ·  	Grey images: We also converted images to grayscale and ran our model with this revised dataset. This offered a different way to extract features from the images.


###### Example of the plant leaf images:
![image](https://user-images.githubusercontent.com/70920238/116769219-20af1880-aa00-11eb-8ca0-61a88cb0b217.png)

###### Colored images converted into grayscale:
![image](https://user-images.githubusercontent.com/70920238/116769235-302e6180-aa00-11eb-95eb-3a165e9678a1.png)

##### Data Sources and links used to retrieve data:
###### https://www.kaggle.com/emmarex/plantdisease and https://github.com/bazilione/poison_ivy/blob/master/data_all.zip


### Description of Revised Models:
##### Model 1: VGG-16 architecture
###### VGG stands for Visual Geometry Group and this method was founded in 2016. It is a convolutional neural network that is 16 layers deep and adapts to arbitrary input sizes and weights.
###### Number of layers: 16
###### Activation Function: ReLU
###### Learning Rate: 0.005
###### Optimizer: Adam
###### Accuracy Rate: 47%
![image](https://user-images.githubusercontent.com/70920238/116769272-6bc92b80-aa00-11eb-96b3-49dd831dcba2.png)


##### Model 2: RMSProp optimizer method
###### RMSProp stands for Random Means Squared Propagation. This optimization method takes a moving average of the squared gradient for each weight and adjusts the weights by dividing the gradient by the root of said average. 

###### Layers: 16
###### Activation Function: ReLU
###### Learning rate: 0.001
###### Optimizer: RMSProp
###### Accuracy: 66%
![image](https://user-images.githubusercontent.com/70920238/116769392-64565200-aa01-11eb-8a6b-8822b119eb87.png)


##### Model 3: Variants of Adam Optimization
###### Adam stands for Adaptive Moment Estimation. This optimization technique uses a replacement optimization algorithm to leverage adaptive learning rates to find individual learning rates for parameters.

###### Number of layers: 16
###### Activation Function: ReLU
###### Learning Rate: 0.001
###### Optimizer 1: Adamax
###### Optimizer 2: Namax
###### Accuracy Rate 1: 83%
###### Accuracy Rate 2: 95%
![image](https://user-images.githubusercontent.com/70920238/116769415-88199800-aa01-11eb-9f87-6ed316f1c8e0.png)


##### Final Model Evaluation:
###### Activation Function: ReLU
###### Optimizer: Nadam
###### Learning Rate: 0.001
###### Accuracy: 95%

###### The final model that we used for plant image recognition is shown below:
![image](https://user-images.githubusercontent.com/70920238/116769430-b4351900-aa01-11eb-8207-085d9a3f021c.png)

##### Conclusion:
###### We improved our model over the course of this semester to better predict the classification of a plant using a picture of its leaf. We tried different optimization algorithms, transformations, and added new plant images to improve the accuracy. Our best model to classify images was our final one using the Nadam optimizer which can classify the leaf accurately 95% of the time. The model generated above-average results for predicting images, however, there is room for improvement. With more data and changes made to the model, we can account for more variations and the diversity in plants. Also, adding more images and testing the model using different methods can improve the overall prediction and performance.


