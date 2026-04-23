# ABE deep learning project: fruit detection

## Repository Description
The following section provides an overview of the repository. 

We are using a slightly overcomplicted repository stucture. It is important to read carefully, as the code will not run unless the structure is kept. 

Since the project runs on Colab, the working directory is set to the Drive mount point. On Google drive, we uploaded a folder named "Deep Learning" (also uploaded to brightspace), which contains a version of our repository with only the training images, weights, and object_detection_utils file. When the notebooks run in Colab, they load all required files (such as detector and classifier weights, object_detection_utils, training images, etc) from this Drive location. However, this version of the repository on Google Drive does not contain the notebooks. 

Therefore, if one wants to update the weigths or training data, they must do it in the Deep Learning folder found on Google Drive. 

The local version of the repository contains the notebooks. Although it also contains the training images and object_detection_utils file, the notebooks always use the version of these files from the mounted Drive, not the local versions. 

When we work in a temporary cloud environment, we need to clone the repository with the notebooks into that session to access it: !git clone https://git.wur.nl/abe-datasets/education/fruit-detection-challenge.git

The rest of the repository is fairly straight forward. There are two folders single-step, and two-step. The single step folder contains the basic single-step model. The two-step folder contains the classification file using ResNet50, as wel as three different detection files:
- ObjectDetection: The basic object detection model. (used in TSB)
- ObjectDetectionPhoto: The object detection model with dropout and photometric augmentation (used in TSPA)
- ObjectDetectionAugmentation: The object detection model with dropout, geometric and photometric augmentation (used in TSPGA)

The object detection and classification files generate weights files, which should be placed in the weights folder in the Drive (one for detection, one for classification). Once this is done, the TwoStep file can be run, which merges the object detector and classifier. 




