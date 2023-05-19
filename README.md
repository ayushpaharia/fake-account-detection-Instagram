# Anomalous User Profile Detection on Instagram using ML Techniques

The objective of this endeavor is to construct and educate a complex neural network model with the purpose of identifying fraudulent or unsolicited Instagram profiles.

---

### Understanding the problem

- A deep neural network model is being developed to detect fake or spam Instagram accounts.
- Spam accounts are a significant problem on Instagram, and they are often created to give users the appearance of having a larger following.
- Some spam accounts are also used to sell fake products or impersonate other users.
- These impersonations can be harmful, leading to influencing, criticizing, and damaging reputations and emotions.
- The neural network model uses advanced algorithms to identify patterns and behaviors that indicate spam accounts.
- The hope is that the model will reduce the number of spam accounts on Instagram and improve the user experience on the platform.

<!-- ABOUT THE PROJECT -->

## 👨‍💻 About The Project

**Anomalous User Profile Detection**'s objective is to recognize fake Instagram accounts using classification algorithms and two datasets: one with 11 features for private accounts and another with 14 features for public accounts.

The projects has 2 dataset: the first with 11 feature is used for the recognition of private accounts, which due to their privacy have a limited amount of informations to share, the second with 14 features is used with the public accounts, which thanks to their privacy have more informations to work with, such as the date of the post published, which gave the algorithms some informations about the index of activity of the account.

Every account's feature has been scraped using an Instagram Web Scraper.

Then the two dataset have been subject to a _Preprocessing Phase_. This phase consists of the _standardization_ and the _normalization_ of the two datasets. In this have been done the [_Feature Importance Forest of Trees_] and the [_Feature Selection_] analysis. In the Feature Selection has been used four algorithms:

- L1 Based
- Tree Based
- Removing Features with Low Variance
- Univariate Select Best (K = 4)

The features, now preprocessed, are taken and given to this [_Machine Learning Classifier Algorithms_]:

- AdaBoost
- Decision tree
- K-Nearest Neighbours (KNN)
- Logistic Regression
- Multi-Layer Perceptron
- Random Forest
- Stochastic Gradient Descent (SGD)
- Stochastic Gradient Descent (SGD)
- Support Vector Machine (SVM)

For every algorithm, in addition to the trainining and the testing phase, has been calculated:

- Cross Validation
- Confusion Matrix
- Receiver Operating Characteristic / ROC Curve
- Classification Report

<!-- GETTING STARTED -->

## 🔨 Getting Started

### Installation

You can just clone this repository and install the requirements by running:

```
$ pip install igramscraper
```

```
$ pip install sklearn
```

Then start the notebook files in the relative folders to see the results.

### Features Description

- **Profile Pic** _boolean value_. 0 if the user doesnt'have the profile pic, 1 otherwise.
- **Nums / Length Username** _double value_. How many special characters of numeric characters the username has on its full length.
- **Full Name Words** _numeric value_. How many words in the full name.
- **Bio Length** _numeric value_. How many characters in the biography of the account.
- **External URL** _boolean value_. 0 if the user doesnt'have the an external URL in the biography, 1 otherwise.
- **Is Private** _boolean value_. 0 if the user doesnt'have a private account, 1 otherwise.
- **Is Verified** _boolean value_. 0 if the user doesnt'have the verified badge , 1 otherwise.
- **Is Business** _boolean value_. 0 if the user doesnt'have a business account, 1 otherwise.
- **# Post** _numeric value_. The number of the post published by the account.
- **# Followers** _numeric value_. The number of the followers of the account.
- **# Following** _numeric value_. The number of the following of the account.
- **Last Post Recent** _boolean value_. 0 if the user doesnt'have a post publisched withing 6 months, 1 otherwise.
- **% Post Single Day** _double value_. How many post has been published in the same same day on the total number of the posts.
- **Index of Activity** _double value_. How many post in average the account publishes every month.
- **Average of Likes** _double value_. Average of the likes of a post of the account.

   <!-- CLASSIFICATION REPORT -->

  ## 📊 CLASSIFICATION REPORT

  ### Report for Private Accounts

   <center>

  |        _Algorithm_         | _Accuracy_ | _Precision_ | _Recall_ | _F-Score_ |
  | :------------------------: | :--------: | :---------: | :------: | :-------: |
  |        **AdaBoost**        |    96%     |     96%     |   96%    |    96%    |
  |     **Decision Tree**      |    96%     |     96%     |   96%    |    96%    |
  |       KNN Classifier       |    95%     |     96%     |   95%    |    95%    |
  |    Logistic Regression     |    94%     |     94%     |   94%    |    94%    |
  | **Multi-Layer Perceptron** |    96%     |     96%     |   96%    |    96%    |
  |       Random Forest        |    94%     |     94%     |   94%    |    94%    |
  |       SGD Classifier       |    95%     |     95%     |   95%    |    95%    |
  |       SVM Classifier       |    94%     |     94%     |   94%    |    94%    |

   </center>

  ### Report for Public Accounts

   <center>

  |      _Algorithm_       | _Accuracy_ | _Precision_ | _Recall_ | _F-Score_ |
  | :--------------------: | :--------: | :---------: | :------: | :-------: |
  |        AdaBoost        |    97%     |     97%     |   97%    |    97%    |
  |     Decision Tree      |    97%     |     97%     |   97%    |    97%    |
  |     KNN Classifier     |    95%     |     95%     |   95%    |    95%    |
  |  Logistic Regression   |    95%     |     95%     |   95%    |    95%    |
  | Multi-Layer Perceptron |    97%     |     97%     |   97%    |    97%    |
  |   **Random Forest**    |    98%     |     99%     |   98%    |    98%    |
  |     SGD Classifier     |    95%     |     95%     |   95%    |    95%    |
  |     SVM Classifier     |    95%     |     95%     |   95%    |    95%    |

   </center>
