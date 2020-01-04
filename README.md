# Dog_Breed_Classifier_CNN

Dog Breed Classification Project which uses CNN's to classify real world dog images and predict their breed out of 133 breeds/classes.
If supplied an image of a human face, the code will identify the resembling dog breed.  Achieved an accuracy of 81% (with just one epoch!!!) using VGG-16 and Transfer learning.

I learned how to build a pipeline that can be used within a web or mobile app to process real-world, user-supplied images.
Transfer learning was also used to use already trained models (VGG-16 in this case) which perform well.These models take weeks to train on high-end GPU's and hence it's not feasible to train them on PC.

## Project Information

### Contents


- Intro
- Step 0: Import Datasets
- Step 1: Detect Humans                                                           Accuracy-98%
- Step 2: Detect Dog                                                              Accuracy-98%
- Step 3: Create a CNN to Classify Dog Breeds (from Scratch)                      Accuracy-16%
- Step 4: Create a CNN to Classify Dog Breeds (using Transfer Learning)           Accuracy-81% 
- Step 5: Writing Own Algorithm
- Step 6: Testing Own Algorithm

### Main CNN Model

![Model Architecture](model_architecture.PNG)

I used this architecture in the step 3 


and I used VGG-16 for the transfer learning in step 4. Here is the architecture of VGG-16:

![VGG16 Architecture](vgg16_architecture.png)


 ## Final Prediction
 
 
![Prediction](prediction.PNG)


## Future tasks to make my project stand out

### 1 AUGMENT THE TRAINING DATA
Augmenting the training and/or validation set might help improve model performance. 
### (DONE NOW)

### 2 TURN YOUR ALGORITHM INTO A WEB APP
Turning the code into a web app using Flask! . Planning to deploy on aws cloud.

### 3 OVERLAY DOG EARS ON DETECTED HUMAN HEADS
Overlay a Snapchat-like filter with dog ears on detected human heads. can determine where to place the ears through the use of the OpenCV face detector, which returns a bounding box for the face. would also like to overlay a dog nose filter, some nice tutorials for facial keypoints detection exist [here](https://www.kaggle.com/c/facial-keypoints-detection/details/deep-learning-tutorial) .

### 4 ADD FUNCTIONALITY FOR DOG MUTTS
Currently, if a dog appears 51% German Shephard and 49% poodle, only the German Shephard breed is returned. The algorithm is currently guaranteed to fail for every mixed breed dog. Of course, if a dog is predicted as 99.5% Labrador, it is still worthwhile to round this to 100% and return a single breed; so, need to find a nice balance.

### 5 EXPERIMENT WITH MULTIPLE DOG/HUMAN DETECTORS
Perform a systematic evaluation of various methods for detecting humans and dogs in images & Provide improved methodology for the face_detector and dog_detector functions.




### Libraries

The list below represents main libraries and its objects for the project.
- [PyTorch](https://pytorch.org/) (Convolutional Neural Network)
- [OpenCV](https://opencv.org/) (Human Face Detection)
- [Matplotlib](https://matplotlib.org/) (Plot Images)
- [Numpy](http://www.numpy.org/) 

### Dataset
* Download the [dog dataset](https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/dogImages.zip)
* Download the [human_dataset](https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/lfw.zip)

### Accelerating the Training Proecess

In the training step in the Step 3 and 4, it will take too long to run so you will need to either reduce the complexity of the VGG-16 architecture or switch to running the code on a GPU or use Google Colab.

#### Amazon Web Services

I Used Amazon Web Services to launch a GPU instance. (This costs money!)
