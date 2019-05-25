
Architectural Basics:--

•	Image Normalization
		
    Normalization of image for example the images to have similar lighting conditions have to be done before we decide on any architecture.
		
    Needs to check the data or images before deciding what type of normalization needs to be applied.

•	Receptive Field
		
    The target receptive field helps to decide number of layers of convolution that is needed in the architecture.

•	3x3 Convolutions
		
    Preferring 3X3 kernels as other kernels of any dimension can be created using this.
		

•	How many layers:
		
    Receptive field and image dimension decides the number of layers that has to be applied .

•	Kernels and how do we decide the number of kernels?
		
    Feature Extractors are kernels. The number of kernels are directly proportional to the size of the channels 
		

•	1x1 Convolutions
		
    Reduces the number of channels after convolution in the best possible way as it combines the information of all the different 
    
    channels and therefore retains most of the information.

•	MaxPooling
		
    Reduces the image size in order to reduce the size of parameters and computation in the network.

•	Position of MaxPooling,
		
    Should not be applied very soon as it may cause loss of important information. 
		
    Also should not be applied too close to the prediction layer which can also cause loss of important information before the prediction

•	The distance of MaxPooling from Prediction
		
    Should not be applied too close to the prediction layer which can also cause loss of important information before the prediction.
		
    Atleast 2 a difference of two layers should be maintained.

•	Concept of Transition Layers
		
    The combination of 1x1 convolution and max pooling is transition layer. Here we are playing with the channels involved and the image 
    
    size which causes a transition in the model.

•	Position of Transition Layer
		
    Transition layer should be applied just before the prediction layer.

•	When do we stop convolutions and go ahead with a larger kernel or some other alternative (which we have not yet covered)
		
    It depends on the image size. For instance for an image size 100x100, if we stop convolving at an image size of 3x3, not much can be 
		
    interpreted from a such a small size of image. We decide to stop at 11x11 which will be the patterns level which can be used to 
    
    decide the part of objects which will help in deciding the objects which will go to objects and then image.

•	Batch Normalization
		
    Solves the problem of "Internal Covariate shift". It is normalization of the channels.
		
    The input for example is changed to x' which is the difference from mean divided by standard deviation which normalizes the input.
		
    Output of the layer is obtained using the trainable parameters alpha and beta. this is the precautionary step.

•	The distance of Batch Normalization from Prediction
		
    It should not be just before the prediction layer.

•	DropOut
		
    A regularization Technique where random selected neurons are dropped during training. This helps in increasing the accuracy.
		

•	When do we introduce DropOut, or when do we know we have some overfitting
		
    To reduce overfitting of the model which helps the network to prevent coadapting too much.
		
    I think we need ovrfitting or not depends on the type of training and validation data set that are getting used.
		

•	SoftMax
		
    Applied at the very last layer which turns the output of the convolution to a probabilty like number.

•	When to add validation checks
		
    To check the training of the model at every epoch with the validation data.

•	How do we know our network is not going well, comparatively, very early
		
    We can detect this by comparing the first two epoch validation checks if no change has been done in the network like
		
    batch normalizatio or drop out.

•	Number of Epochs and when to increase them
		
    Its the number of time the training data is passed to the model for training. This is similar to iterations in optimization. 
		
    We increase this on the basis of training accuracy that we get for each epoch. Increasing this allows the network to learn more on 
    
    the training data.

•	Learning Rate
		
    A hyperparameter that decides at what rate the network will be learning on the training data. 

•	LR schedule and concept behind it
		
    We should me maintaining a sweet spot between very high and very low learning rates. Very low learning rate as performance issues 
    
    along with high chances of overfitting. Very high learning rate has chances of missing the local minima and thus reduces the 
    
    accuracy.

•	Batch Size, and effects of batch size
		
    The number of training images used in one iteration. One of the major effect seen is in the performance. With higher batch size the 
    
    time taken for one epoch is reduced. This helps in increasing the accuracy as the model gets to see more images every iteration 
    
    which gives a chance to learn better.

•	Adam vs SGD
		
    Not sure of the optimizer concepts and different type of optimizers used.
