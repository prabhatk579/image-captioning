Image Captioning
===

Image captioning may can be defined as the process of generation of human redable text which captions an image. For human it's very easy but for machines, it need to know every features of the image and their context to create a caption which is readable by a human being.

Steps for image captioning:

- Feature extraction from images.
- Cleaning and preperation of the description and dataset for caption generation
- Craeting the model
- Model training
- Validation of the model
- Creating a caption of some image (selfie in this case).

1. ### Pre-Calculate Photo Features (Feature extraction)

For feature extraction, we pre-calculate the features from the photos. We do this because we want to use those extracted features for image captioning. Take CNN for example, we first extract features from the images in the feature extraction block which are basically combination of convolution layers and pooling layers. We then use those features to classify the images using classification which are basically fully connected dense layers with activation functions to classify the images. Similarly we use those features to make the machine learn from the images and translate the images.

2. ### Cleaning and prepearation of the description and the dataset for captioning
#### Prepeartion of text
The descriptions are tokenized; this means that each token is comprised of words separated by white space. It also means that punctuation are separated as their own tokens, such as periods (‘.’) and apostrophes for word plurals (’s). 

##### Whole Description Sequence Model

In Whole description sequence model we would use an encoding of the image to generate the output sentence. The image may be encoded using a pre-trained model used for image classification, such as the `VGG` trained on the ImageNet model. The output of the model would be a probability distribution over each word in the vocabulary of the photo descripion in the `descriptions.txt`. The sequence would be as long as the longest photo description.
##### Word-By-Word Model

In word-by-word model, we generate a caption for photographs by generating one word given both the image as input and the last word generated. This model would then have to be called recursively to generate each word in the description with previous predictions as input.