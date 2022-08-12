# Poseidon's Eye
* Ship Detection and Recognition Utilizing Web Camera Streams 
* Roboflow Custom Data Set (will download as zip): https://app.roboflow.com/ds/5qoAPGIHWQ?key=JRywu8UTxX

# Objectives
The objective of this project where to:
* Source images that can be used to create a data set
* Annotate sourced images to create a computer vision data set
* Train a model utilizing YOLOv5 in order to create weights to use for image recognition
* Feed videos into Computer Vision Program (CVP) to test the weights created 
* Refine weights and CVP
* Feed CVP live streams to detect ships 

# Approach
* Utilizing Roboflow, a dataset was created by webscraping shipspotting.com. Roughly 3000 images were scraped. Raw pictures will be included in the repository
* Roboflow Annotate was used to annotate the images. 
* When generating the dataset, preprocessing and augmentation steps were added. For preprocessing, auto-orient, isolate objects, and resize to 600x416 were used. For augmentation, a horizontal flip and blur of up to 3.75px were used. This resulted in a model with 7.4k images being used for training, 692 images for validation, and 387 images for testing. 
* The classifications used are: Bulkers, Car Carriers, Conatiner Ships, Cruise Ships, Recreational, Sailboats, and Tugs.
* Weights were calcualted utilizing YOLOv5 train.py for 100 epochs, this number needs to be increased. These weights can be found in best.pt
* YouTube videos were then fed into both SAHI and YOLOv5 detect.py image recognition. These downloaded videos can be found in the download folder. 

# Products
