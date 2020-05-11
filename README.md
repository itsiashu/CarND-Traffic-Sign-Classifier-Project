## Project: Build a Traffic Sign Recognition Program
[![Udacity - Self-Driving Car NanoDegree](https://s3.amazonaws.com/udacity-sdc/github/shield-carnd.svg)](http://www.udacity.com/drive)

Traffic Sign Classifier

Overview
---
In this project, you will use what you've learned about deep neural networks and convolutional neural networks to classify traffic signs. You will train and validate a model so it can classify traffic sign images using the [German Traffic Sign Dataset](http://benchmark.ini.rub.de/?section=gtsrb&subsection=dataset). After the model is trained, you will then try out your model on images of German traffic signs that you find on the web.


### Build a Traffic Sign Classifier Project ###

### Project Steps ###
	-load data set 
	-visualize data
	-build, train and test a neural network model
	-let model do predictions on test images
	-analyze soft-max probabilities of test images
	-summarize results with a detailed report

### Dependencies ###
This lab requires:

* [CarND Term1 Starter Kit](https://github.com/udacity/CarND-Term1-Starter-Kit)

The lab environment can be created with CarND Term1 Starter Kit. Click [here](https://github.com/udacity/CarND-Term1-Starter-Kit/blob/master/README.md) for the details.

### Dataset and Repository
	No of train examples = 34799
	No of validation examples = 4410
	No of test examples = 12630
	Image shape = 32x32
	No of classes = 43

### Exploratory visualization of the dataset ###
Please refer dataset visualization done in project 


### Design and Test a Model Architecture ###
 - shuffle training data
 - normalize image data for less costly train


### Final model consists of below layers ###
	Layer			Description
	input			32x32x3 normalize RGB image
	convolution 5x5		1x1 stride, valid padding and output 28x28x12
	relu	
	max pooling		2x2 stride, output 14x14x12
	convolution 5x5		1x1 stride, valid padding, outputs 10x10x16
	relu	
	max pooling		2x2 stride, output 5x5x16
	flatten			input 5x5x16, output 400
	fully connected		input 400, output 120
	relu	
	fully connected		input 120, output 84
	relu	
	fully connected		input 84, output 43
	soft-max layer	


### Train Model ###
	- batch size used is 128
	- epochs is 20
	- learning rate varied from 0.01 to 0.0001 

	rate = 0.001
	batch_size = 128
	train_epochs = 20

	final model results:
	train-set accuracy of 0.996
	validation-set accuracy 0.971
	test-set accuracy 0.876

### Test Model on New Images ###
	- Model is tested on 5 random images picked from web
	- Check html doc with this
