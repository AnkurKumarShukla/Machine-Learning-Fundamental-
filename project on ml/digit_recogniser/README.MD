                                     A TWIST with MNIST

 
The MNIST dataset has handwritten digits from 0 to 9. This is one of the best datasets to use for starting with image recognition using deep learning, and has been explored thoroughly for years by research scientists for various purposes. This challenge brings a twist to the MNIST dataset by adding handwritten values from 10 to 19 instead of 0 to 9. Every image in the dataset has values from 10 to 19 along with the corresponding label. 
The task for this challenge is to create a model which can accurately identify the value from the images. We will be evaluating submissions based on the accuracy of the predicted labels against the true labels. 
The dataset has 3 files, train.csv, test.csv and submission_format.csv. 
The train.csv has 1401 columns, where the first 1400 columns are flattened images of the handwritten values. Each image has a dimension of 28x50. The last column is "label" which is the corresponding label for every image. 
In test.csv, there are 1401 columns. The first column is "image_id" which is an ID corresponding to every image. The next 1400 columns are flattened images of the handwritten values. Each image has a dimension of 28x50. The "image_id" is to be retained as it is part of the submission. You have to use the images in the test.csv file to predict the labels. 
The submission format is given with the dataset (submission_format.csv). Every image in the test dataset has an "image_id" column which is the index of the submission format. The second column is "label" which is the predicted label for every image, corresponding to the "image_id". You have to upload the submission file to the competition to get the accuracy and appear on the leaderboard. 
Files
1.	 train.csv - the training set
2.	test.csv - the test set
3.	submission_format.csv - a sample submission file in the correct format


Language – python (ipynb)
Solution on my Kaggle id – Here
LINK = https://www.kaggle.com/code/ankurkumarshukla/digit-recog

Libraries 
Numpy , pandas =  to deal with array image data 
Matplotlib = to visualise the image data 
Sklearn = to pre- process  the data , and split data for making validation set 
Tensorflow = to use keras module to make model , create input and hidden layers , use optimiser 


Approach = Problem is solved using simple neural network 

First I split the train data for validation . Then created 2 function named – ankmagic  and changer . Those function transform 1d image data to 28 x 50 2d array  for visualisation

After this normalisation occur . Neural networks process inputs using small weight values, and inputs with large integer values can disrupt or slow down the learning process. As such it is good practice to normalize the pixel values so that each pixel value has a value between 0 and 1.

Next I started with making of neural network . I used relu activation function and softmax for output layer . ReLU in hidden layer to avoid vanishing gradient problem and better computation performance , and Softmax function use in last output layer . I tried SGD and adam optimiser . Adam works better. 

After changing multiple combination I used one of the model and created submission report 

Full code - https://www.kaggle.com/code/ankurkumarshukla/digit-recog















Result 
 
This model predict the result with the accuracy of 99% , validation accuracy = 96.13%


