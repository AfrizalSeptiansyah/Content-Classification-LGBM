# Project Title

Content Classification with LGBM

## Description

In this project, I will classify content into 5 categories: football, news, business, technology and automotive (imbalanced case). Using LGBM with word vector (fasttext) as features extraxtion.

## Step By Step Solve Problem 
### 1. Label Distribution 
It seems that this is an imbalanced case so I use the metrics f1 score. I use class weight to fix it. 

![label](https://github.com/AfrizalSeptiansyah/Content-Classification-LGBM/blob/main/asset/label.png?raw=true)

### 2. Create Stopwords 
I use the bag of words to get the words that occur most often. I choose the 500 most frequently occurring words and then I selected the most frequently occurring words and not keywords.

### 3. Cleansing  
At this stage I tokenize, change all words to lowercase, take words that are more than 1 letter and remove stopwords and punctuation. 

### 4. Training FastText 

I am using word vector (fasttext) as feature extraction with 1 word represented by 50 vectors. I also use UMAP for visualization of training results with fasttext.

![umap_1](https://github.com/AfrizalSeptiansyah/Content-Classification-LGBM/blob/main/asset/umap_1.PNG?raw=true)

![umap_2](https://github.com/AfrizalSeptiansyah/Content-Classification-LGBM/blob/main/asset/umap_2.PNG?raw=true)


### 5. Modeling 

I use LGBM algorithm then use RandomSearchCV with 5 cross-validations to find optimal hyperparameters.


### 6. Evaluation 

#### Classification Report
![classification_report](https://github.com/AfrizalSeptiansyah/Content-Classification-LGBM/blob/main/asset/classification_report.PNG?raw=true)

#### Confusion Matrix 
![confusion_matrix](https://github.com/AfrizalSeptiansyah/Content-Classification-LGBM/blob/main/asset/confusion_matrix.png?raw=true)


## Sanity Check 

The model successfully predicts new data which is a minority class.

![sanity_check](https://github.com/AfrizalSeptiansyah/Content-Classification-LGBM/blob/main/asset/sanity_check.PNG?raw=true)


# Conclusion 
After doing a long modeling process, we managed to get an f1 score of 0.90 using LGBM and word vectors (fasttext). In the minority class (automotive), we also get sufficient precision and recall and the sanity check also successfully predicts new data from the minority class correctly.

Thank you for reading :)
