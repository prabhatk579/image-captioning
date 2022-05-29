# image-captioning

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