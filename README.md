<H3>NAME</H3> Nandhana.R
<H3> REGISTER NO.</H3>212223040124
<H3>EX. NO.1</H3>
<H3>DATE</H3>
<H1 ALIGN =CENTER> Introduction to Kaggle and Data preprocessing</H1>

## AIM:

To perform Data preprocessing in a data set downloaded from Kaggle

## EQUIPMENTS REQUIRED:
Hardware – PCs
Anaconda – Python 3.7 Installation / Google Colab /Jupiter Notebook

## RELATED THEORETICAL CONCEPT:

**Kaggle :**
Kaggle, a subsidiary of Google LLC, is an online community of data scientists and machine learning practitioners. Kaggle allows users to find and publish data sets, explore and build models in a web-based data-science environment, work with other data scientists and machine learning engineers, and enter competitions to solve data science challenges.

**Data Preprocessing:**

Pre-processing refers to the transformations applied to our data before feeding it to the algorithm. Data Preprocessing is a technique that is used to convert the raw data into a clean data set. In other words, whenever the data is gathered from different sources it is collected in raw format which is not feasible for the analysis.
Data Preprocessing is the process of making data suitable for use while training a machine learning model. The dataset initially provided for training might not be in a ready-to-use state, for e.g. it might not be formatted properly, or may contain missing or null values.Solving all these problems using various methods is called Data Preprocessing, using a properly processed dataset while training will not only make life easier for you but also increase the efficiency and accuracy of your model.

**Need of Data Preprocessing :**

For achieving better results from the applied model in Machine Learning projects the format of the data has to be in a proper manner. Some specified Machine Learning model needs information in a specified format, for example, Random Forest algorithm does not support null values, therefore to execute random forest algorithm null values have to be managed from the original raw data set.
Another aspect is that the data set should be formatted in such a way that more than one Machine Learning and Deep Learning algorithm are executed in one data set, and best out of them is chosen.


## ALGORITHM:
STEP 1:Importing the libraries<BR>
STEP 2:Importing the dataset<BR>
STEP 3:Taking care of missing data<BR>
STEP 4:Encoding categorical data<BR>
STEP 5:Normalizing the data<BR>
STEP 6:Splitting the data into test and train<BR>

##  PROGRAM:
TYPE YOUR CODE HERE
import pandas as pd
import io
from sklearn.preprocessing import StandardScaler
from sklearn.preprocessing import MinMaxScaler
from sklearn.model_selection import train_test_split

data = pd.read_csv("Churn_Modelling.csv")
data
data.head()

X=data.iloc[:,:-1].values
X

y=data.iloc[:,-1].values
y

data.isnull().sum()

data.duplicated()

data.describe()

data = data.drop(['Surname', 'Geography','Gender'], axis=1)
data.head()

scaler=MinMaxScaler()
df1=pd.DataFrame(scaler.fit_transform(data))
print(df1)

X_train ,X_test ,y_train,y_test=train_test_split(X,y,test_size=0.2)

X_train

X_test

print("Lenght of X_test ",len(X_test))


## OUTPUT:
SHOW YOUR OUTPUT HERE
![image](https://github.com/user-attachments/assets/04eec952-e0de-4fa1-9ade-137a9c3e7fd7)

X VALUES:
![image](https://github.com/user-attachments/assets/51914183-2d03-4f4b-8960-abf93a4b0568)

Y VALUES:
![image](https://github.com/user-attachments/assets/dd7af305-0ffe-4923-ae09-381252984808)

NULL VALUES:
![image](https://github.com/user-attachments/assets/3c861555-c19d-43fa-8fbd-1ad12d881449)

DUPLICATED VALUES:
![image](https://github.com/user-attachments/assets/6f1f058f-60d4-4f03-ab23-8d395423dc86)

DESCRIPTION:

![image](https://github.com/user-attachments/assets/dd58f16b-0215-404e-b8b3-70632d87ab4b)

NORMALIZESD DATASET:
![image](https://github.com/user-attachments/assets/89a8b057-12ba-4043-a3ad-88a1351c2412)

TRAINNING DATA:
![image](https://github.com/user-attachments/assets/f728fb4a-92c0-442f-a9c6-c1c564fcf641)

TESTING DATA:
![image](https://github.com/user-attachments/assets/c55cf764-c3ee-46c2-8b45-20ba4c6f23e7)













## RESULT:
Thus, Implementation of Data Preprocessing is done in python  using a data set downloaded from Kaggle.


