# **Traffic Sign Recognition** 

## Project Writeup
### By:   Omer Waseem
### Date: 2017-08-21

---

[//]: # (Image References)

[image1]: ./writeup_images/sample_image_09.jpeg "Sample image (no passing)"
[image2]: ./writeup_images/hist.jpeg "Histogram of training data"
[image3]: ./writeup_images/hist.jpeg "Histogram of training data"
[image4]: ./writeup_images/hist.jpeg "Histogram of training data"
[image5]: ./writeup_images/hist.jpeg "Histogram of training data"
[image6]: ./writeup_images/hist.jpeg "Histogram of training data"
[image7]: ./writeup_images/hist.jpeg "Histogram of training data"
[image8]: ./writeup_images/hist.jpeg "Histogram of training data"

## Description
#### This project uses a CNN with 7 weighted layers (4 convolutional and 3 fully connected) to classify the [German Traffic Sign Dataset](http://benchmark.ini.rub.de/?section=gtsrb&subsection=dataset) with 99.5% validation accuracy and 97.9% test accuracy.

---

### Files Submitted

#### 1. [Project Writeup (this file)](https://github.com/omerwase/SDC_P2_Traffic_Sign_Classifier/blob/master/README.md)
#### 2. [Traffic_Sign_Classifier.ipynb Notebook](https://github.com/omerwase/SDC_P2_Traffic_Sign_Classifier/blob/master/Traffic_Sign_Classifier.ipynb)
#### 3. [IPython Notebook Report](https://github.com/omerwase/SDC_P2_Traffic_Sign_Classifier/blob/master/report.html)
#### 4. [New German Traffic Sign Images](https://github.com/omerwase/SDC_P2_Traffic_Sign_Classifier/tree/master/new_traffic_signs/)
  
  
### Data Set Summary & Exploration

#### 1. Dataset Summary

The following stats about the dataset were calculated using numpy methods and attributes:

* The size of training set is **34799** images
* The size of the validation set is **4410** images
* The size of test set is **12630** images
* The shape of a traffic sign image is **(32, 32, 3)**
* The number of unique classes/labels in the data set is **43**

#### 2. Exploratory Visualization

Below is an example image from the dataset corresponding to a **No Passing** sign (label 9):  
![alt text][image1]

The historgram below shows the number of images for each class in the training dataset:  
![alt text][image2]

There is a large discrepancy between certian classes. For example label 0 has 180 examples (lowest) and label 2 has 2010 (highest). One possible enhancement to the training data would be to gather more images of traffic signs with few examples. **Note:** additional data was not generated for this project. Validation accuracy of **99.5%** and test accuracy of **97.9%** was achieved using only the dataset pictured above.

### Design and Test a Model Architecture

#### 1. Describe how you preprocessed the image data. What techniques were chosen and why did you choose these techniques? Consider including images showing the output of each preprocessing technique. Pre-processing refers to techniques such as converting to grayscale, normalization, etc. (OPTIONAL: As described in the "Stand Out Suggestions" part of the rubric, if you generated additional data for training, describe why you decided to generate additional data, how you generated the data, and provide example images of the additional data. Then describe the characteristics of the augmented training set like number of images in the set, number of images for each class, etc.)

As a first step, I decided to convert the images to grayscale because ...

Here is an example of a traffic sign image before and after grayscaling.

![alt text][image2]

As a last step, I normalized the image data because ...

I decided to generate additional data because ... 

To add more data to the the data set, I used the following techniques because ... 

Here is an example of an original image and an augmented image:

![alt text][image3]

The difference between the original data set and the augmented data set is the following ... 


#### 2. Describe what your final model architecture looks like including model type, layers, layer sizes, connectivity, etc.) Consider including a diagram and/or table describing the final model.

My final model consisted of the following layers:

| Layer         		|     Description	        					| 
|:---------------------:|:---------------------------------------------:| 
| Input         		| 32x32x3 RGB image   							| 
| Convolution 3x3     	| 1x1 stride, same padding, outputs 32x32x64 	|
| RELU					|												|
| Max pooling	      	| 2x2 stride,  outputs 16x16x64					|
| Convolution 3x3	    | etc.      									|
| Fully connected		| etc.        									|
| Softmax				| etc.        									|
|						|												|
|						|												|
 


#### 3. Describe how you trained your model. The discussion can include the type of optimizer, the batch size, number of epochs and any hyperparameters such as learning rate.

To train the model, I used an ....

#### 4. Describe the approach taken for finding a solution and getting the validation set accuracy to be at least 0.93. Include in the discussion the results on the training, validation and test sets and where in the code these were calculated. Your approach may have been an iterative process, in which case, outline the steps you took to get to the final solution and why you chose those steps. Perhaps your solution involved an already well known implementation or architecture. In this case, discuss why you think the architecture is suitable for the current problem.

My final model results were:
* training set accuracy of ?
* validation set accuracy of ? 
* test set accuracy of ?

If an iterative approach was chosen:
* What was the first architecture that was tried and why was it chosen?
* What were some problems with the initial architecture?
* How was the architecture adjusted and why was it adjusted? Typical adjustments could include choosing a different model architecture, adding or taking away layers (pooling, dropout, convolution, etc), using an activation function or changing the activation function. One common justification for adjusting an architecture would be due to overfitting or underfitting. A high accuracy on the training set but low accuracy on the validation set indicates over fitting; a low accuracy on both sets indicates under fitting.
* Which parameters were tuned? How were they adjusted and why?
* What are some of the important design choices and why were they chosen? For example, why might a convolution layer work well with this problem? How might a dropout layer help with creating a successful model?

If a well known architecture was chosen:
* What architecture was chosen?
* Why did you believe it would be relevant to the traffic sign application?
* How does the final model's accuracy on the training, validation and test set provide evidence that the model is working well?
 

### Test a Model on New Images

#### 1. Choose five German traffic signs found on the web and provide them in the report. For each image, discuss what quality or qualities might be difficult to classify.

Here are five German traffic signs that I found on the web:

![alt text][image4] ![alt text][image5] ![alt text][image6] 
![alt text][image7] ![alt text][image8]

The first image might be difficult to classify because ...

#### 2. Discuss the model's predictions on these new traffic signs and compare the results to predicting on the test set. At a minimum, discuss what the predictions were, the accuracy on these new predictions, and compare the accuracy to the accuracy on the test set (OPTIONAL: Discuss the results in more detail as described in the "Stand Out Suggestions" part of the rubric).

Here are the results of the prediction:

| Image			              |     Prediction	        	                  				| 
|:---------------------:|:---------------------------------------------:| 
| Stop Sign      	     	| Stop sign   						                         			| 
| U-turn     			        | U-turn 										                             |
| Yield					            | Yield											                              |
| 100 km/h	           		| Bumpy Road					 			                          	|
| Slippery Road	      		| Slippery Road      						                    	|


The model was able to correctly guess 4 of the 5 traffic signs, which gives an accuracy of 80%. This compares favorably to the accuracy on the test set of ...

#### 3. Describe how certain the model is when predicting on each of the five new images by looking at the softmax probabilities for each prediction. Provide the top 5 softmax probabilities for each image along with the sign type of each probability. (OPTIONAL: as described in the "Stand Out Suggestions" part of the rubric, visualizations can also be provided such as bar charts)

The code for making predictions on my final model is located in the 11th cell of the Ipython notebook.

For the first image, the model is relatively sure that this is a stop sign (probability of 0.6), and the image does contain a stop sign. The top five soft max probabilities were

| Probability         	|     Prediction	        					| 
|:---------------------:|:---------------------------------------------:| 
| .60         			| Stop sign   									| 
| .20     				| U-turn 										|
| .05					| Yield											|
| .04	      			| Bumpy Road					 				|
| .01				    | Slippery Road      							|


For the second image ... 
