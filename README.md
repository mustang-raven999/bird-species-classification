
# Bird Classification Project

This repository contains the implementation of a bird classification project using deep learning techniques, particularly focusing on transfer learning models. The dataset used for this project is the CUB-200-2011 bird image dataset.

## Project Overview
The aim of this project is to classify bird species using a pre-trained deep learning model and to fine-tune the model for optimal performance.

## Dataset
- **Source**: CUB-200-2011 bird dataset.
- **Data Processing**: The dataset was divided into training and testing sets using the provided `images.txt`, `train_test_split.txt`, and `image_class_labels.txt` files.
- **Input Shape**: [224, 224, 3] was used for the images.

## Methods
### Data Augmentation
An `ImageDataGenerator` was employed to apply data augmentation techniques, with a validation split to prevent overfitting.

### Model
Various pre-trained models were evaluated using transfer learning:
- **InceptionV3**
- **Xception**
- **ResNet**

The models were fine-tuned by adjusting the trainable layers and employing different hyperparameters.

### Hyperparameters
- **Optimizer**: Adam optimizer with a learning rate of 0.0001 was found to work best.
- **Activation Function**: ReLU was used due to its efficiency and simplicity.
- **Learning Rate Scheduling**: A self-adjusting learning rate was employed using `LearningRateScheduler`.
- **Batch Size**: A batch size of 32 was selected for optimal memory usage and feature learning.
- **Other Optimizers**: RMSprop, Adam, and SGD were tested, with Adam providing the best results.

### Results
- **Accuracy**: 0.637
- **F1 Score**: 0.636
- **Precision**: 0.673
- **Recall**: 0.637

## Files
- **Bird_Classification_script.ipynb**: Jupyter notebook with the implementation of the model and analysis.
- **Bird_Classification.pdf**: Report detailing the project's methods, results, and analysis.
- **Images**: Train and test image sets for the classification task.

## How to Run
1. Clone the repository.
2. Ensure you have the necessary dependencies installed (TensorFlow, Keras, etc.).

NOTE: Running the whole project might take an extended period of time. Training time also depends on your system's computation capabilities.

i.  Download the project by unzipping the folder provided. Also download the image dataset seperately and upload it in your drive in the following paths:
	drive_zip_file = "/content/drive/My Drive/bird_classification/bird_CUB_200_2011.zip"

ii. In case you just want to see how the model is working, the model is provided along with the code file. Load the model and go to the "Model Evaluation" section of the notebook and run the cells under that section.

iii. Before running the code you might want to comment out the models{Incase of multiple models applied} containing the command model.fit


3. Review the findings and results in the `Bird_Classification.pdf` file.

## Libraries Used
- TensorFlow
- Keras
- NumPy
- Matplotlib
- Pandas
