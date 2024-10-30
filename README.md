# Deepfake Detection Using InceptionV3

## Project Description
This project aims to develop a deep learning model for detecting deepfake images by leveraging the InceptionV3 architecture. The model is trained to classify Images/Videos as either "fake" or "real," utilizing a dataset comprising deepfake and authentic images/Videos.

## Key Features
- **Data Preprocessing**: 
  - Images/frames are preprocessed using the `ImageDataGenerator` to normalize pixel values and augment the dataset, enhancing model robustness.

- **Transfer Learning**: 
  - The model employs transfer learning by initializing InceptionV3 with pretrained weights from ImageNet, allowing the model to leverage existing feature extraction capabilities.

- **Model Architecture**: 
  - The architecture includes several layers:
    - Global Average Pooling
    - Dense layers with batch normalization
    - Dropout layers to prevent overfitting
    - The final output layer uses a sigmoid activation function for binary classification.

- **Training Strategy**: 
  - The model is trained with various callbacks, including:
    - Early stopping
    - Model checkpointing
    - Learning rate reduction
  - This optimizes training efficiency and helps prevent overfitting.

- **Performance Metrics**: 
  - The model's performance is evaluated using metrics such as:
    - Accuracy
    - Precision
    - Recall
    - F1 Score
  - This ensures a comprehensive assessment of its predictive capabilities.

## Results
Upon training, the model achieved a validation accuracy of approximately 81% and an F1 score of around 0.74. The confusion matrix indicates balanced performance, with precision and recall demonstrating the model's capability to effectively distinguish between fake and real images.

## Getting Started

### Prerequisites
- Python 3.x
- TensorFlow/Keras
- NumPy
- Matplotlib
- Other required libraries (as specified in `requirements.txt`)

### Installation
1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd deepfake-detection-inceptionv3
   ```

2. Install the required packages:
   ```bash
   pip install -r requirements.txt
   ```

