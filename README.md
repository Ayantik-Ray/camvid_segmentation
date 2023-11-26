
Semantic Segmentation with U-Net on CamVid Dataset

Introduction Semantic segmentation is a computer vision task aimed at classifying each pixel in an image into predefined classes. Leveraging the U-Net architecture for this task has become popular due to its prowess in capturing intricate details and spatial relationships. This document explores the application of semantic segmentation on the CamVid dataset using the U-Net model.

Dataset Insight The CamVid dataset comprises images captured from a vehicle-mounted camera and is widely utilized for semantic segmentation tasks. It provides pixel-wise labeled masks corresponding to the images, encompassing 32 distinct classes such as road, sidewalk, building, and sky.

U-Net Architecture The U-Net architecture is characterized by a contracting path, a bottleneck, and an expansive path. The contracting path focuses on context and spatial information through convolutional and pooling layers, while the expansive path facilitates precise localization using transposed convolutions. Crucial spatial information is preserved through skip connections linking corresponding layers in the contracting and expansive paths.

Key Components of the Architecture:

Contracting Path: Comprising convolutional blocks with batch normalization and ReLU activation, each followed by max-pooling to reduce spatial dimensions.

Bottleneck: A double convolution block retaining critical information in a compressed form.

Expansive Path: Consists of transposed convolutions and concatenation with corresponding feature maps from the contracting path. Each block includes convolutional layers with batch normalization and ReLU activation.

Output Layer: Utilizes a 1x1 convolution for generating the segmentation map with pixel-wise class predictions.

Data Preprocessing CamVid dataset images and masks undergo standard transformations, including resizing and normalization. Masks are converted to one-hot encoded tensors to align with the model's output format.

Loss Function and Optimization Focal Loss, a modification of cross-entropy, serves as the loss function. Stochastic Gradient Descent (SGD) with momentum is employed for optimization.

Training The model undergoes training across multiple epochs, monitoring training loss and Intersection over Union (IoU). IoU measures the overlap between predicted and ground truth masks.

Results and Visualization Training progress is visualized through plots of training and validation loss curves. Sample images, original masks, and predicted masks are showcased for performance assessment.

Conclusion Semantic segmentation of the CamVid dataset using the U-Net architecture showcases the model's accuracy in classifying pixels. Further experimentation with hyperparameters, data augmentation, or model architecture fine-tuning may enhance performance. This document provides a guide for implementing semantic segmentation tasks on similar datasets using the U-Net model.
