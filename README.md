# Color Classification Model

This repository contains a Python project that builds a color classification model using a neural network. The model takes red, green, and blue color values as input and predicts the color category. It is trained on a dataset of labeled color samples.

## Project Structure

- `source_code.ipynb`: Jupyter Notebook file containing the complete source code.
- `Result\Result.csv`: CSV file containing the results of the model's predictions.
- `Model\model_weights.h5`: Saved model weights.
- `Verification_source_code.ipynb`: Jupyter Notebook file for verifying the model on custom data.

## Code Explanation

The code can be summarized as follows:

### 1. Importing Libraries

The code begins by importing various Python libraries for data manipulation, visualization, and machine learning. Notable libraries include pandas for data handling, TensorFlow for building and training a neural network, and various other utilities like NumPy, Seaborn, Matplotlib, and Plotly.

### 2. Data Loading and Preprocessing

A dataset named 'data.csv' is loaded using Pandas. This dataset contains information about colors represented by 'red', 'green', and 'blue' values along with their corresponding color categories in the 'label' column. The 'label' column is encoded into numerical data using Label Encoding and One-Hot Encoding. The dataset is split into training and testing sets in an 80:20 ratio.

### 3. Building a Neural Network Model

A Sequential neural network model is created using TensorFlow's Keras API. This model has two dense layers, batch normalization, and activation functions (LeakyReLU and softmax). The LeakyReLU activation function introduces a small gradient for negative inputs, which helps mitigate the vanishing gradient problem. The model is compiled with a categorical cross-entropy loss function, Adam optimizer, and custom evaluation metrics (accuracy, F1 score, precision, and recall).

### 4. Training the Model

The model is trained on the training data using the `model.fit` function. Training continues for 300 epochs.

### 5. Model Evaluation

The code includes custom evaluation metrics functions for precision, recall, and F1 score, which are used to evaluate the model's performance on the test data. The results (accuracy, loss, precision, recall, F1 score) are printed and saved.

### 6. Model Weights Saving

The model weights are saved to a file named 'model_weights.h5' for future use.

### 7. Visualization

The code includes Matplotlib-based visualization of training history, showing accuracy, loss, precision, and recall over epochs.

### 8. Making Predictions

The model makes predictions on the test data, and the results are saved in a DataFrame. The predictions are converted back to categorical labels and compared to the actual labels. The resulting DataFrame is saved to 'Result\Result.csv'.

## Verification

To verify the model with custom data, follow these steps:

1. Create a CSV file named 'verification.csv'.
2. Add raw data to this file.
3. Run the 'Verification_source_code.ipynb' Jupyter Notebook.
4. View the results in the 'verification.csv' file.

## Results

The results of the model's predictions can be found in 'Result\Result.csv'.

## Usage

Feel free to use this code and model for your color classification tasks. You can train it on your own dataset or make predictions with new color data.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
