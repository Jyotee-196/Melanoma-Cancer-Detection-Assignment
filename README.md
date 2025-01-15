Melanoma Skin Cancer Detection


Abstract
Cancer manifests in over 200 different types, with melanoma being the most lethal form of skin cancer. Diagnosing melanoma involves a series of steps, beginning with clinical evaluation, followed by dermoscopy and histopathological assessment. If detected early, melanoma is highly treatable. The initial phase of diagnosing melanoma includes a visual inspection of the skin, where dermatologists capture dermatoscopic images of skin lesions using high-resolution cameras. While standalone dermatoscopy offers accuracy in the range of 65-80%, further analysis by specialists can boost the accuracy of melanoma diagnosis to 75-84%. This project seeks to create an automated classification system using image processing methods to classify skin cancer based on lesion images.

Problem Statement
Currently, diagnosing skin cancer through biopsy involves taking a sample of the skin lesion for microscopic examination, a process that can take a week or longer. This project aims to expedite this procedure to just a couple of days through a predictive model. The model uses a Convolutional Neural Network (CNN) to classify various types of skin cancer based on lesion images, helping reduce the waiting period and potentially benefiting millions.

Motivation
The primary motivation behind this project is to contribute to the reduction of skin cancer-related mortality. Leveraging state-of-the-art image classification technology, the project aims to improve early diagnosis for better patient outcomes. Advances in computer vision, particularly in machine learning and deep learning, have shown promise in addressing complex problems across multiple domains.

Dataset
The dataset used consists of 2,357 images of malignant and benign skin lesions, provided by the International Skin Imaging Collaboration (ISIC). These images have been categorized according to ISIC classification, with a balanced distribution across the categories.

To combat class imbalance, the Augmentor Python library was employed to augment the dataset and ensure that each class has an adequate number of samples.

Sample Image from the Dataset

https://github.com/Jyotee-196/Melanoma-Cancer-Detection-Assignment/blob/c5c49d51b335c8eeaf8d623c34dcfc4ad8ba38af/Samleimagefromdataset.png


CNN Architecture Design
The goal is to design a CNN-based model capable of classifying skin lesions. To improve classification accuracy, a custom CNN model was developed that includes several layers and techniques to enhance learning and generalization:

Rescaling Layer: This layer normalizes the input data, transforming pixel values from the range [0, 255] to [0, 1].
Convolutional Layer: These layers apply convolutions to the input data, transforming pixel information within their receptive fields into a single value. This operation reduces the image size and consolidates the pixel information.
Pooling Layer: Pooling layers help reduce the dimensions of the feature maps, which decreases the number of parameters and computational effort required during training.
Dropout Layer: To prevent overfitting, this layer randomly sets some input units to zero during training.
Flatten Layer: This converts multi-dimensional data into a one-dimensional vector for input into the fully-connected layer.
Dense Layer: These layers consist of fully connected neurons, where each neuron is connected to every neuron in the previous layer.
ReLU Activation: The Rectified Linear Unit (ReLU) activation function outputs the input directly if it’s positive and zero otherwise, helping to address the vanishing gradient problem.
Softmax Activation: The Softmax function is used in the output layer to predict a multinomial probability distribution, ensuring the sum of probabilities across all classes equals 1.

Model Architecture
https://github.com/Jyotee-196/Melanoma-Cancer-Detection-Assignment/blob/ce479302b51d8fba23482f4542c7796b84aec240/ModelLayer.png

Model Evaluation
https://github.com/Jyotee-196/Melanoma-Cancer-Detection-Assignment/blob/3579c5529e993b9d897d3183471452c56ea29348/ModelEvaluation.png
