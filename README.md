# St-Gerogie-Detection

# Problem Statement:

Build a model that can detect the presence of st Gerogie in an image data.

## Summarization :

* As we have received huge almost 2000 image datets of st Geore, so We only collected 91 images of St. George and mannualy annotated bounding boxes with coordinates, width and height with the help of Roboflow. (Because its not possible to annotated 2k images mannualy alone with limited time).

*  Make a seperate folder 'classes' on Google drive and put all annotated datasets of train(50 images), validation(25 images) and test(16 images) along with data.yaml file( it contains train, val data image path and number of classes and names) and mount it on google colab.

*   Install yoloV8 for detection of St Georgie in the image from ultralytics.YoloV8 is the latest version of yolo. And it is the fastest among all the version available for the object detection. It has very few parameters compared to other yolo version available.

*  keep all image sizes 224x224, run yolov8s (it has mape = 44.9, param = 11.2,speed = 128.4 ms) on train images for detecting St georgie with 35 epochs.During training YoloV8 perform some data augmentation technique inside.

*  Save the best weight of the trained model along with Precision , Recall, F1 , PR curve inside the run folder in G drive.

*   Run the save best weight trained model to the validation 25 images.
*  Run the save best weight trained model to the test 16 images with 25% confidence score. And it can successfully predict all the images.Keep confidence score low just because it can successfully predict more images.

* Last we write a code where we can put any image url or image path to predict 
where it can detect presence of St  George or not. Like We experimented one image of non St George and it can predict it successfully.


## *Metrics*
*  After trained the yoloV8s model on the train images, we got very good Accuracy as we can see that frm the confusion matrix above of St Georgie TP = 80% and precision recall both around 80 % from all train images . And for validation images Precision and recall tends to 100%.

*  From the result images above we can see that Loss is getting reduced for all epochs proceed further. If we run near around 300 - 400 epochs for model training and if we train more than 1.5k annotated images, we can eventually get a excellent accuracy for this particular project, for time constraints here we are taking limite images as well as epochs.(possible improvements).


