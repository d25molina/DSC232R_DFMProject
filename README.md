# DSC232R_DFMProject
This is my project for my UCSD DSC232R course, being done in the Spring 2025 quarter. This project deals with images of skin lesions and attempts to accurately classify which images contain malignant skin lesions (i.e. melanoma) and which images contain benign skin lesions (i.e. nevus, seborrheic keratosis).

## Pre-processing explanation
The exploratory data analysis (EDA) immediately suggested that the images must be normalized. This will be done by resizing the images and normalizing the pixel values as well. Another thing that the EDA made apparent were the disproportionate ways the images were split among the training, testing, and validation sets. I will venture into making each proportion relatively close by virtue of stratified sampling. In addition, among all three sets, nevus is heavily over-represented. This goes hand-in-hand with the aforementioned stratified sampling. However, if the over-representation of nevus images persists, I plan on undersampling the majority to maintain my desired balances.

## Notebook (Milestone2)
Here is the link to my Jupyter notebook for the second milestone: [DSC232R_GP.ipynb](./DSC232R_GP.ipynb)

## Pre-processing
As you will see from the notebook for Milestone3, the pre-processing that was done included making the sizes of each image 64 x 64 and applying a stratified sample to make a new 70/15/15 split to make a new train/valid/test data split. I fit the data into a logistic regression model and analyzed the performance of the model in a markdown section of the notebook, which is attached below the conclusion.

### Conclusion
The logistic regression model on raw pixels is probably more useful as a simple debugging baseline. Since we are dealing with images that are textured, of high variance, and of not much discriminative structure, high accuracy was never going to be accomplished for test accuracy. The way in which I was able to fit the dermatoscopic images into the model was by setting my universal image size to 64 x 64, which most likely removes the color cues. Whenever I set my image size to something larger (i.e. 128 x 128), the executor memory would not be enough to train the logistic regression model. To possibly improve my model, I could explore alternative ways to resize my images to where I can maintain the integrity and structure of those textures and color cues from the images and perhaps venture into the application of PCA onto my dataset, in order to process my images through the models without taking up that memory.

## Notebook (Milestone3)
Here is the link to my Jupyter notebook for the third milestone: [DSC232R_M3.ipynb](./DSC232R_M3.ipynb)
