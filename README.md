<h1>Automatic Garbage Segregation using YOLO-v3</h1>

This project was created using Jupyter Notebooks, Darknet Framework and Labelimg.<br>
We propose a method to segregate garbage into recyclable and non-recyclable by using an image processing algorithm called Tiny-YOLO-v3. <br>
<b>Our result is seen as follows:</b> [a relative link](final_result.png)<br>

In this project we used a robotic arm, controlled by Raspberry pi to make use of these co-ordinates and segregate the waste into its respective bins. <br><br>
<b>Demo and explanation are given in this video:</b> https://youtu.be/s9vpYhOcICE<br>
The implementation of Tiny-YOLO-v3 can be found in the modified darknet framework:
https://github.com/AlexeyAB/darknet 
<br>
If you wish to train your own model using any of the algorithms in the framework, please follow the instructions in the readme file on that link.<br><br>
Our model has been trained to detect 5 classes, namely: Glass, Wood, Plastic, Metal and Paper. After training the model on a dataset of 10k images for 9k iterations using Google Colab, the model was able to achieve a <b> Mean Average Precision of 61.47% </b> <br>
More information can be found in the report pdf file: [a relative link](Report_DT26072020.pdf) , or the paper: [a relative link](Segregation.pdf) 
<br><br>

<h2>To Run The Model:</h2> <br>
Install darknet framework. <br>
Label the dataset using labelimg, https://github.com/tzutalin/labelImg <br>
Split the dataset into test.txt and train.txt using process.py, and copy both txt files into darknet folder<br>
Insert dataset into darknet/data folder <br>
Copy the yolo-tiny-train and yolo-tiny-test cfg files into darknet/cfg folder. <br>
Copy obj_data.data into darknet folder, copy obj.names into darknet folder <br>
Run MultipleObjectDetection.ipynb and change the image names as necessary for testing and training. <br>
The saved weights after training will appear in darknet/backup folder, which can be used for testing. <br>
Finally, IntegratedFinals.py can be used to run the model on a raspberry pi using the final weights file obtained. <br>
Done in Collaboration with github users: @cauvery-a and @akshitha98
