# MS285_Final_Project
##Project Title

#-Object Detection Using YOLO and its application for identifying and quantifying Rockfish seen in RUV recording

##Motivation (3-5 sentences)

#-I am interested in using machine learning to help humans annotate video. Humans spend tons of time watching video recorded by ROVs, BRUVs, and landers to indentify and enumerate species of interest. Personally, I am interested in Rockfish species because that is primarily what we see in the CCFRP catch data. For my thesis, I will be recording video from above a lure and enumerating fish interactions with a lure. I hope to be able to use machine learning to identify Rockfish species and enumerate them in video frames to calculate MaxN of rockfish species.

##Data (3-5 sentences)

#-Jake Todd, a recent graduate from MMLML, used mini-landers (metal frame with stereo gopro video) to record fish species in different habitat types in order to draw conclusions on how habitat and wave energy regimes affect the makeup of fish assemblages. The video he collected includes a limited view of the benthos and records fish as they swim by. Each video is an hour long and he recorded hundreds of videos. I will annotate a few of his videos to create a training dataset of labeled images with classes; Fish, Rockfish, and other. The fish will be labeled when it is a fish but cannot be identified as a Rockfish and the Rockfish label will be used when it can be positively identified as a Rockfish.

##Model (4-6 sentences)

#-I am planning to use a YOLO model from Ultralytics. This model is appropriate to use on my dataset because I want to identify multiple objects per image and train the model on the labeled objects instead of the whole frame. YOLO is the best and easiest model to train using this type of data. I will train the model using the training dataset I manually annotated. The loss function used by YOLO models is different for each of the model iterations, but the YOLOv8 model I am planning on using uses both Box Loss (CIoU Loss and Distribution Focal Loss) and Classification Loss (Binary Cross-Entropy)

##Analysis (3-5 sentences)

#-First, I will train the model on the training dataset and use another smaller set of labeled images to validate and test the models performance. Based on this validation/test dataset, the model will provide a performance which will hopefully decrease over time.

#Next, I will use the trained model to indentify and enumerate the fish in a new video and I will extract the number of fish and Rockfish the model identified in each video frame. I will then review the results of the models performance and make any corrections. I will also compare this to the species MaxN calculated by Jake Todd. The differences of the model and Jake's MaxN will tell me how the model does.

#Other Pertinent Info (as necessary)
#How to access training data images and labels:
# Follow this link for training dataset in YOLO format: https://drive.google.com/drive/folders/10QfcUQJNyWHKnvAh13qAz6hr34aXPx2J?usp=sharing
# See files for YOLO model - 'best.pt' for training weights from this dataset. 
# MS285_Final_Project
