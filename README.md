# 📝 Fruit Image Classification using MobileNetV2

## 🔍 Summary
This project focuses on building an image classification model using the MobileNetV2 architecture to identify five types of fruits: Apple, Banana, Grape, Mango, and Strawberry. The dataset, sourced from Kaggle, is split into training, validation, and test sets. Extensive preprocessing, data visualization, and hyperparameter tuning techniques have been applied to optimize model performance.

## 📌 1. Introduction
The dataset is designed for fruit image classification and is organized into separate folders for training, validation, and testing.

Class names are extracted from the training directory.

The dataset includes five fruit categories and has real-world applicability.

Reproducibility is ensured with fixed random seeds in TensorFlow and NumPy.

## 📂 2. Loading the Dataset
A custom function reads image files and decodes JPEG/PNG formats using TensorFlow.

Images are standardized and converted to float32.

A second function loads all datasets and applies shuffling, labeling, and optional size trimming.

Data is split into x_train, y_train, x_valid, y_valid, x_test, and y_test.

## 📊 3. Data Distribution
The dataset is well-balanced across all five fruit categories.

A pie chart is used to visually confirm the equal distribution.

## 🖼️ 4. Data Visualization
A function show_images displays sample images and labels.

If a model is passed, it also displays predicted labels for the images.

Helps assess model performance visually and understand the dataset structure.

## 🔧 5. MobileNetV2 Hypertuning
MobileNetV2 is loaded with pre-trained ImageNet weights.

The model is extended with:

Global average pooling layer

Dropout layer (50%)

Dense layer with softmax activation for classification

Compiled using:

categorical_crossentropy loss

Adam optimizer with custom learning rate

Accuracy as a performance metric

Trained using:

EarlyStopping (patience = 3)

ModelCheckpoint (best model saved as .h5)

20 epochs, custom BATCH_SIZE

## 📈 6. Accuracy
Training Accuracy: 84%

Validation Accuracy: 87%

Test Accuracy: 92%
→ Shows the model generalizes well to unseen data.

## 🤖 7. Prediction
The model successfully predicts the class of random fruit images.

Visual results are shown with both original and predicted labels.

## 🧠 8. Conclusion
The MobileNetV2 model performed well with a simple architecture.

High test accuracy suggests strong generalization.

Future improvements could involve testing deeper or more complex models using Keras Tuner for optimal hyperparameters.
