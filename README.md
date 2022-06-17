# Gesture-Recognition-using-TensorFlow
This set of Notebooks provides a complete set of code to be able to train and leverage your own custom object detection model using the Tensorflow Object Detection API.

## Steps

### Step 1:
Clone this repository: https://github.com/nicknochnack/TFODCourse

### Step 2:
Create a new virtual environment
python -m venv tfod

### Step 3:
Activate your virtual environment
source tfod/bin/activate # Linux
.\tfod\Scripts\activate # Windows 

### Step 4:
Install dependencies and add virtual environment to the Python Kernel
python -m pip install --upgrade pip
pip install ipykernel
python -m ipykernel install --user --name=tfod

### Step 5:
Collect images using the Notebook 1. Image Collection.ipynb - ensure you change the kernel to the virtual environment from Kernel > Change Kernel > tfod

### Step 6
Manually divide collected images into two folders train and test. So now all folders and annotations should be split between the following two folders.
\TFODCourse\Tensorflow\workspace\images\train
\TFODCourse\Tensorflow\workspace\images\test

### Step 7:
Begin training process by opening 2. Training and Detection.ipynb, this notebook will walk you through installing Tensorflow Object Detection, making detections, saving and exporting your model.

### Step 8:
During this process the Notebook will install Tensorflow Object Detection. You should ideally receive a notification indicating that the API has installed successfully at Step 8 with the last line stating OK.
If not, resolve installation errors by referring to the Error Guide.md in this folder.

### Step 9:
Once you get to step 6. Train the model, inside of the notebook, you may choose to train the model from within the notebook. I have noticed however that training inside of a separate terminal on a Windows machine you're able to display live loss metrics.
![Picture1](https://user-images.githubusercontent.com/38144223/174248225-8b7ccb10-b0d4-408f-8a7b-b9f010b31e02.png)

### Step 10:
You can optionally evaluate your model inside of Tensorboard. Once the model has been trained and you have run the evaluation command under Step 7. Navigate to the evaluation folder for your trained model e.g.
cd Tensorlfow/workspace/models/my_ssd_mobnet/eval
and open Tensorboard with the following command
tensorboard --logdir=. 
Tensorboard will be accessible through your browser and you will be able to see metrics including mAP - mean Average Precision, and Recall.

## OUTPUT:
![LiveLong](https://user-images.githubusercontent.com/38144223/174246567-43c9b65e-154b-4261-8f8b-b4315bc35f99.png)
![ThankYou](https://user-images.githubusercontent.com/38144223/174247955-716661e0-08cf-4a46-be9b-4ab9d8274cfb.png)
![ThumbsDown](https://user-images.githubusercontent.com/38144223/174248085-4d91d1fb-4ede-4a4e-b57b-0d5d3e10dafe.png)
![ThumbsUp](https://user-images.githubusercontent.com/38144223/174248102-4ffe843d-6f25-45ba-befe-e6e94e368226.png)

## Statistics:
### Loss Metrics (Time series):
![Picture2](https://user-images.githubusercontent.com/38144223/174248752-e1516a46-57e2-480e-8ae6-2b9d1e1823c1.png)

### Loss Metrics (Scalars):
![Picture3](https://user-images.githubusercontent.com/38144223/174248755-5df276ce-312a-4a31-b135-e99c46350853.png)

### Precision Metrics (Time series):
![Picture4](https://user-images.githubusercontent.com/38144223/174248757-8617cb6e-e503-4e10-84b1-2934db231820.png)

### Precision Metrics (Scalars):
![Picture5](https://user-images.githubusercontent.com/38144223/174248758-6cad2f3a-b52d-4347-b871-11b69ec0b080.png)
