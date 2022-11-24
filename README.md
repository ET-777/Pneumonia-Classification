Pneumonia Classification with VGG16
-----------------------

Predict whether a patient has pneumonia or not. A dataset of X-Ray chest images containing healthy patients and patients with pneumoinia is used to train a classification model with VGG16. Dataset is [here](https://data.mendeley.com/datasets/rscbjbr9sj/2).

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