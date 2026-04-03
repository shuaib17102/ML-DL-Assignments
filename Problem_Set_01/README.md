Project Title: Automated Detection of Pneumonia from Chest X-Ray Images using Deep Learning

Objective:

The objective of this project is to develop a Convolutional Neural Network (CNN) model capable of classifying pediatric chest X-ray images into two categories: Pneumonia and Normal. This helps demonstrate how deep learning can assist in medical image analysis.

Dataset:

- Total Images: 5,863
- Categories: Pneumonia, Normal
- Dataset Structure: train, test, val folders provided
- Source: Pediatric chest X-ray dataset(https://drive.google.com/file/d/1219EeGE1XTJVXYaulynJSa3BXGsbNCLx/view?usp=sharing)

---

Approach and Methodology:

1. Data Preparation:

- All images were resized to 150x150 pixels for uniform input
- Pixel values were normalized by scaling to the range [0,1]
- Data augmentation was applied to increase dataset variability, including:
  - Rotation
  - Zoom
  - Shearing
  - Horizontal flipping

2. Validation Strategy:

- A validation subset was created from the training data using an internal split
- This ensures that validation samples are drawn from the same distribution as training data
- The test dataset was kept completely separate and unseen for final evaluation

3. Model Architecture:

- A Convolutional Neural Network (CNN) was implemented with multiple feature extraction layers
- The architecture includes:
  - Three convolutional blocks with increasing filter sizes (32, 64, 128)
  - Batch Normalization layers to stabilize and speed up training
  - MaxPooling layers for dimensionality reduction
  - A fully connected Dense layer with ReLU activation
  - Dropout layer to reduce overfitting
  - Output layer with Sigmoid activation for binary classification

4. Training Configuration:

- Optimizer: Adam (with a reduced learning rate for stable convergence)
- Loss Function: Binary Crossentropy
- Evaluation Metric: Accuracy
- Early Stopping was used to prevent overtraining by monitoring validation loss

5. Evaluation Method:

- Model performance was evaluated on a completely unseen test dataset
- Accuracy and loss curves were plotted to analyze training behavior

---

Results and Findings:

- The model achieved high accuracy on the test dataset (~88–90%)
- Data augmentation significantly improved generalization capability
- Regularization techniques such as Dropout and Batch Normalization reduced overfitting
- The model demonstrates strong capability in distinguishing between Pneumonia and Normal X-rays

---

Conclusion:

This project highlights the effectiveness of CNNs in medical image classification tasks. Proper preprocessing, regularization, and validation strategies play a crucial role in achieving reliable and generalizable results.

---

How to Run:

1. Open the notebook in Google Colab
2. Download the dataset using the provided link
3. Run all cells sequentially
4. Observe training progress and evaluation outputs

---

Additional Notes:

- Binary classification was used due to the two-class nature of the problem
- Sigmoid activation with binary crossentropy ensures efficient optimization
- The model design balances performance and computational efficiency
