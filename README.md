# DSC232R_DFMProject
This is my project for my UCSD DSC232R course, being done in the Spring 2025 quarter. This project deals with images of skin lesions and attempts to accurately classify which images contain malignant skin lesions (i.e. melanoma) and which images contain benign skin lesions (i.e. nevus, seborrheic keratosis).

## Pre-processing explanation
The exploratory data analysis (EDA) immediately suggested that the images must be normalized. This will be done by resizing the images and normalizing the pixel values as well. Another thing that the EDA made apparent were the disproportionate ways the images were split among the training, testing, and validation sets. I will venture into making each proportion relatively close by virtue of stratified sampling. In addition, among all three sets, nevus is heavily over-represented. This goes hand-in-hand with the aforementioned stratified sampling. However, if the over-representation of nevus images persists, I plan on undersampling the majority to maintain my desired balances.

## Notebook
Here is the link to my Jupyter notebook: [DSC232R_GP.ipynb](./DSC232R_GP.ipynb)
