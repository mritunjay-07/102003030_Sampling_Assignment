# SAMPLING ASSIGNMENT 
**By: MRITUNJAY DUBEY (102003030)**
## OVERVIEW
* **Sampling is a method that allows us to get information about the population based on the statistics from a subset of the population (sample), without having to investigate every individual**.
* **Sampling is done to draw conclusions about populations from samples, and it enables us to determine a population’s characteristics by directly observing only a portion (or sample) of the population**. 
  * Selecting a sample requires less time than selecting every item in a population.
  * Sample selection is a cost-efficient method.
  * Analysis of the sample is less cumbersome and more practical than an analysis of the entire population.
## TASK
* In this sampling assignment, the task is to generate five samples using five different sample techniques and predict the accuracy using five differnt models.
* The steps used for achieving this task are as follows: 
  * **Step-1: Obtaining the dataset.**
  * **Step-2: Balancing the dataset.** 
  * **Step-3: Using different sampling techniques, to create five different samples.**
  * **Step-4: Applying five different models.**
  * **Step-5: Obtaining the accuracy table.**
## **STEP-1: OBTAINING THE DATASET**
* This assignment is using a credit card fraud detection dataset.
* The dataset consists of **773 rows and 31 columns**. The dataset can be downloaded from the given link: [Credit_Card_Dataset](https://github.com/mritunjay-07/102003030_Sampling_Assignment/blob/main/Creditcard_data.csv)
* From the dataset, it is clear that the given problem is of binary classification. You can clearly see that there is a huge difference between the data set. **9000 non-fraudulent transactions and 492 fraudulent**.
## **STEP-2: BALANCING THE DATASET**
* As it is observed that fraudulent transaction is around 400 when compared with non-fraudulent transaction around 90000, the given data set is imbalance.
* When a dataset is imbalanced, the majority class tends to dominate and predicting it would lead to a high accuracy. However, this approach would neglect the minority class, which is often the main focus of the model. **The imbalanced nature of the dataset can cause the model to perform poorly in capturing the patterns and nuances of the minority class, leading to poor overall performance**.
* Therefore, it is important to restructure the modeling approach to address the class imbalance issue. This can be achieved by using techniques such as resampling the dataset to balance the classes, applying cost-sensitive learning, or using algorithms that are specifically designed to handle imbalanced data. By doing so, the model can effectively capture the patterns in both the majority and minority classes, resulting in a more robust and accurate model.
* For this assignment, I have used **SMOTE Sampling** technique to balance the dataset.
  * **SMOTE (Synthetic Minority Over-sampling Technique)** is a widely used technique in machine learning for dealing with imbalanced datasets. In imbalanced datasets, the number of examples in one class is significantly lower than the number of examples in another class. This can lead to poor performance of machine learning models, as they tend to be biased towards the majority class.
  * **SMOTE** addresses this problem by creating synthetic examples of the minority class. It works by selecting a minority class example and finding its k nearest neighbors. A synthetic example is then created by interpolating between the selected example and one of its neighbors. This process is repeated until the desired number of synthetic examples is generated.
* After balancing, now our dataset contains both majority and minority classes equally.
## **STEP-3: CREATION OF FIVE DIFFERENT SAMPLES USING DIFFERENT SAMPLING TECHNIQUES**
* **For obtaining five different samples, I have used five different techniques. These are:**
  1. **For Sample 1->Stratified Sampling**
     * Stratified sampling is a sampling method in which the population is divided into homogeneous subgroups, called strata, and a random sample is taken from each stratum to ensure proportional representation of each subgroup in the sample.  
  2. **For Sample 2->Systematic Sampling**
     * Systematic sampling is a statistical sampling method in which every k-th item in the population is selected for the sample, where k is a fixed interval calculated by dividing the population size by the desired sample size.
  3. **For Sample 3->Convenience Sampling**
     * Convenience sampling is a non-probability sampling technique in which participants are selected based on their availability and willingness to participate, rather than through a random or systematic selection process, leading to a non-representative sample.
  4. **For Sample 4->Cluster Sampling**
     * Cluster sampling is a sampling technique in which the population is divided into clusters, and a random sample of clusters is selected for inclusion in the sample, with all members of the selected clusters included in the sample, which can save time and cost in data collection.
  5. **For Sample 5->Simple Random Sampling**
     * Simple random sampling is a statistical sampling method in which each member of the population has an equal chance of being selected for the sample, and each sample of the same size has an equal chance of being selected, ensuring representativeness and reducing bias.
## **STEP-4: APPLYING FIVE DIFFERENT MODELS**
* **The five different models used for predicting results are:**
  1. **M1->Logistic Regression**
     * Logistic regression is a statistical model used to analyze the relationship between a binary dependent variable and one or more independent variables, by estimating the probability of the dependent variable based on the values of the independent variables, making it a popular method for classification problems.
  2. **M2->Support Vector Machine**
     * Support Vector Machine (SVM) is a popular machine learning algorithm used for both classification and regression, that aims to find the hyperplane that maximizes the margin between the two classes, and can work well with non-linearly separable data by using kernel functions.
  3. **M3->Decision Tree Classifier**
     * Decision tree classifier is a machine learning model that builds a tree-like structure to predict the class label of a given input by recursively splitting the input space based on the most informative features, which is easy to interpret and visualize, but can suffer from overfitting.
  4. **M4->Gaussian Naive Bayes**
     * Gaussian Naive Bayes is a probabilistic machine learning algorithm based on Bayes' theorem that assumes independence among the features and uses a Gaussian distribution to model continuous features, making it fast, simple, and effective for classification tasks, particularly when the input variables are continuous.
  5. **M5->KNeighbors**
     * K-Nearest Neighbors (KNN) is a machine learning algorithm that can be used for both classification and regression, which predicts the label or value of a new observation by finding the k-nearest neighbors in the training set and taking a weighted average of their values, making it easy to understand and interpret, but computationally expensive for large datasets.
## **STEP-5: ACCURACY TABLE**
**Results Obtained After Applying Five Different Models on Five Different Samples** 
 ||Sample 1|Sample 2|Sample 3|Sample 4|Sample 5|
  | :----: |:--------------------:|:------------:|:------------:|:---------------:|:---------------:|
  | M1 | 0.95 | 0.86 | 0.66 | 0.90 | 0.90 |
  | M2 | 0.92 | 0.86  | 0.66 | 0.91 | 0.95 |
  | M3 | 0.92 | 0.90 | 0.94 | 0.97 | 0.80 |
  | M4 | 0.87 | 0.86  | 0.59 | 0.74 | 0.80 | 
  | M5 | 0.87 | 0.67 | 0.88 | 0.86 | 0.80 | 
  
**NOTE: It can be observed that Decision Tree Classifier gives the maximum accuracy score.**
