Pneumonia X-Ray Classification with VGG16
-----------------------

Deep network to predict whether a patient has pneumonia or not from x-ray images. A dataset of x-ray chest images containing over 5 thousand images of healthy patients and patients with pneumoinia is used to train a classification model with VGG16, a bidirectional LSTM model. Dataset is [here](https://data.mendeley.com/datasets/rscbjbr9sj/2). You can see the data processing, model, code, and full explanations in the `PneumoniaClassification.ipynb` notebook above.

Quick Overview
----------------------

<p align="center">
<br />
Normal X-Rays
<br />
<img src="https://github.com/ET-777/Pneumonia-Classification/blob/master/images/normal.png"/>
<br />
<br />
<br />
Pneumonia X-Rays
<br />
<img src="https://github.com/ET-777/Pneumonia-Classification/blob/master/images/pneumonia.png"/>
<br />
<br />
<br />
</p>

The datasets were converted into tensors for the tensorflow model. A functional model was constructed, with the VGG16 model without its output layers and adding the the output layer for this data. Only the output layer has trainable parameters.

<p align="center">
<br />
VGG16 without output layers
<br />
<br />
<img src="https://github.com/ET-777/Pneumonia-Classification/blob/master/images/vgg16.jpg" height="50%" width="50%"/>
<br />
<br />
<br />
Functional Model
<br />
<br />
<img src="https://github.com/ET-777/Pneumonia-Classification/blob/master/images/model.jpg"/>
<br />
<br />
<br />
</p>


Results
----------------------

The model was trained for 3 epochs with a sigmoid activation and a BinaryCrossEntropy loss function.

<br />

 Data | Loss | Accuracy
------------ | ------------- | -------------
Training | 0.0908 | 0.97
Testing | 0.4349 | 0.84
Validation | 0.2796 | 0.88

<br />
The loss scores are not bad but do vary between the sets, training data was quick and probably with some overfitting. The accuracy, however, performs well enough on both test and validation sets and indicates a decent model for prediction. Other models might be tried for better results.

<br /><br />

Installation
----------------------

### Download the data

* Clone this repo to your computer.
* Create a `Data` folder in the project directory.
* Download the data files from Mendeley Data into the `Data` folder.  
    * You can find the data [here](https://data.mendeley.com/datasets/rscbjbr9sj/2).
* Extract the `.zip` file you downloaded into the `Data` folder.
    * Move the `test` and 'train' folders within the `chest_xray` folder to the parent `Data` folder.
    * Create a `val` folder for validation data and move some of the test images into it.

### Install the requirements
 
* Install the requirements with `anaconda` or with pip using `pip install -r requirements.txt`.
    * Make sure you use Python 3.
    * You may want to use a virtual environment for this.

Usage
-----------------------

* Open `PneumoniaClassification.ipynb` with `Jupyter Notebook`.
* Run the notebook
    * Make sure you are using running `tensorflow` with a `GPU`.
