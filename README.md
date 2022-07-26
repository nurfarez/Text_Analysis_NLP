# Text_Analysis_NLP
 Analysing Text with sentiment analysis


# About the project
This project is to analyse the text dataset in categorize unseen 
articles into 5 categories namely:
1)Sport
2)Tech
3)Business
4)Entertainment 
5)Politics

# Objective of the project
To develop a LSTM Model using DL approach(sentiment analysis) which can achieve accuracy of more 
than 70% and F1 score of more than 0.7 and only allowed to use TensorFlow library 

# software used:
GOOGLE COLAB
obstacle during model construction is unable to compute module for the textanalysis model due to longer runtime.This maybe due to unstable
connection. 

# Libraries used:
1.RegEx
2.os
3.json
4.pickle
5.Datetime
6.NumPy
7.pandas
8.scikit-learn
9.TensorFlow/tensorboard

# Steps taken in the project
# Data loading
The data been loaded using pd.read_csv as usual using url 
# Data Inspection

Target: Category with 5 types which are 
0)Sport
1)Tech
2)Business
3)Entertainment 
4)Politics

and feature: text

- Duplicated data were found and None Nan values were found in this dataset
# Data Cleaning

Duplicated data were dropped and we changed all the letters into small letters

# Features Selection

no features selection were performed as it is for text analysis

# Data Preprocessing

The preprocessing as below were carried out and the dataset were split train and test :
1.Tokenization
2.padding
3.OHE
4.train-test-split

# Model development

The model were constructed using sequential. Embedding, Bidirectional, LSTM, Dropout, Dense, Input used to improve the model construction.

At the first, the model were running as per above with the epoch of 5 and nodes of 128 with 2 layers and it's lead to overfitting issue where the accuracy/f1 score obtained is at very low.

![Confusion_Matrix before](https://user-images.githubusercontent.com/109565405/180985309-9ebe7fac-3fac-4535-9fdb-5220c4387f9c.PNG)

Then, the model trained back with the epoch of 50, nodes 128, 2 layers and the used of early callback were implemented. The accuracy and f1 score has been increased as per below:


![model1](https://user-images.githubusercontent.com/109565405/180987150-f3a1fe68-f27b-4824-84b3-7b5c3781cc7a.PNG)

![Confusion_Matrix after](https://user-images.githubusercontent.com/109565405/180986743-522d8f58-bac1-4dc5-a039-4606296285cf.PNG)

The model architecture were plotted as per below:
![model_arch](https://user-images.githubusercontent.com/109565405/180986996-5acebc96-6d59-4d97-8f72-a739c3a86516.png)

The epoch acc and loss also displayed in tensorboard:

![epoch_acc](https://user-images.githubusercontent.com/109565405/180987186-321002cd-ca0e-49de-846f-3690add8703e.PNG)

![epoch_loss](https://user-images.githubusercontent.com/109565405/180987219-ad1fffdd-d68b-46dd-99c3-3b076c6ab86e.PNG)



# Discussion

The model achieved 0.41 accuracy at the first training model where all the f1 score is below 0.5 averagely. The model indicated towards overfitting issue.
So, the model is trained back with  the epoch of 50, nodes 128, 2 layers and the used of early callback were implemented. The accuracy has increased to 0.81 and the f1 increased by 0.7 above.

# Dataset Credit 
Thanks to
(https://raw.githubusercontent.com/susanli2016/PyCon-Canada-2019-NLP-Tutorial/master/bbc-text.csv)




















