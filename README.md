# Resume Classifier Evaluation Report

## Dataset
Our dataset comprises 2171 resume images from Kickresume and 2000 non-resume images sourced from various internet platforms. To ensure a robust dataset, we applied augmentation and preprocessing techniques, enhancing diversity and standardizing images for effective model training.

## Data Processing
For streamlined dataset management and processing, we utilized Fastai's DataBlock structure. ImageBlock managed image data, while CategoryBlock handled categorical labels. Leveraging functions like get_image_files and parent_label facilitated efficient retrieval and labeling of images. A random splitter divided the dataset into distinct training (80%) and validation (20%) sets. Image preprocessing included resizing images to 460 pixels, and batch-level augmentations such as rotations and flips were applied to enhance model generalization.

## Model Selection and Performance
Our approach involved using the fastai library and the cnn_learner interface to create a CNN with the resnet34 architecture. The learning rate finder determined an optimal learning rate, and subsequent fine-tuning for two epochs adapted the pre-trained model to our specific dataset, focusing on visual characteristics for resume classification.

## Model Evaluation Results
After training and validation, the model exhibited exceptional performance on the validation set:
- **Validation Loss:** 0.0254
- **Validation Accuracy:** 99.06%

### Confusion Matrix:
