
<h1>ActiveOD</h1>


<p>A graphical Semi-automatic annotation tool based on <a  href="https://github.com/tzutalin/labelImg">labelImg</a> and <a  href="https://github.com/ultralytics/yolov5">YOLOv5</a></p>

<p>Active learning Tool for semi-automatic data annoation for object detection</p>

  

## Demonstration of semi-automatic labeling function
This tool is used to reduce the time of the labeling for object detection using a pretrained Yolo model.
All you have to do is train the model on few annotated data, run the tool and ask for autolabel proposals from the models weights, correct what needs to be fixed and fine tune the model on the fixed annotation that way the model will learn from your feedback.

  

## Attention

<p>If there is a problem, please put it forward in the issue</p>

<p>Please put classes.txt under the marked dataset folder in advance</p>

<p>The annotation file is saved in the same location as the picture folder</p>

<p>Recommended version of python: python 3.8</p>

<p>Recommended for conda environments</p>

<p>Note: This project only supports Version 5 of YOLOv5 for the time being.</p>

  
  

## Installation and use



<p>1.Fetching Yolov5 project</p>

  

```bash

git clone https://github.com/ultralytics/yolov5

```
<p>2.Put the annotated data into path/data and put your images and labels, train and test </p>
<p>3.Create your training configuration in a yamlfile (number of classes, classes names ordered by index, train path...)</p>
<p>4.train your model using:</p>
  

```bash

python train.py --data yourconfigfile.yaml

```

<p>5.Fetching ActiveLearningLabeler Project</p>

  

```bash

git clone https://github.com/MoetezKd/ActiveOD/

```
<p>6.Copy all your yolo project to the yolov5 folder of the ActiveLearningLabeler Project</p>
<p>7. put the images you want to label in the images folder and modify the classes.txt the same as the trained yolov5 order</p>
<p>8.Switching the operating directory to the project directory</p>

  

```bash

cd ActiveOD

```

  

<p>9.Installation environment</p>

  

```bash

pip install -r requirements.txt

```

  

<p>10.Modify the contents of the /data/predefined_classes.txt file in the directory to your own category</p>

  

<p>11.Launching applications</p>

  

```bash

python ActiveLearningLabeler.py

```

  


  

<p>12. Click on the "Auto Annotate" button to confirm that the information is correct and then select the trained yolov5 pytorch model weights from path/yolov5/runs/ to complete the auto annotation</p>

  

<p>13. Adjust the automatic annotation results according to the actual requirements and save them</p>
<p>14. Click on Retrain Model to finetune the model on the fixed annotations and obtain a better performance using active learning</p>
<p>15. Now you can use the fintuned model to annotate other images</p>
