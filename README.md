#Automatic Garbage Segregation using YOLO-v3

This project was created using Jupyter Notebooks, Darknet Framework and Labelimg.<br>
We propose a method to segregate garbage into recyclable and non-recyclable by using an image processing algorithm called Tiny-YOLO-v3. <br>
Our result is seen as follows: [a relative link](final_result.jpg)

In this project we used a robotic arm, controlled by Raspberry pi to make use of these co-ordinates and segregate the waste into its respective bins. 
Demo and explanation are given in this video: https://youtu.be/s9vpYhOcICE
The implementation of Tiny-YOLO-v3 can be found in the modified darknet framework:
https://github.com/AlexeyAB/darknet
If you wish to train your own model using any of the algorithms in the framework, please follow the instructions in the readme file on that link. 
Our model has been trained to detect 5 classes, namely: Glass, Wood, Plastic, Metal and Paper. After training the model on a dataset of 10k images for 9k iterations using Google Colab, the model was able to achieve a Mean Average Precision of 61.47%
More information can be found in the report pdf file, or the paper: [a relative link](GarbageSegregation.pdf)

#To Run The Model: 
Install darknet framework. 
Label the dataset using labelimg, https://github.com/tzutalin/labelImg
Split the dataset into test.txt and train.txt using process.py, and copy both txt files into darknet folder
Insert dataset into darknet/data folder 
Copy the yolo-tiny-train and yolo-tiny-test cfg files into darknet/cfg folder. 
Copy obj_data.data into darknet folder, copy obj.names into darknet folder 
Run MultipleObjectDetection.ipynb and change the image names as necessary for testing and training. 
The saved weights after training will appear in darknet/backup folder, which can be used for testing. 
Finally, IntegratedFinals.py can be used to run the model on a raspberry pi using the final weights file obtained. 
