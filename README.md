# breast-cancer-detection
A breast cancer dataset is loaded using the Pandas library, and an exploratory data analysis is conducted. The dataset contains various features related to breast cancer tumors, and the 'diagnosis' column is the target variable, indicating whether a tumor is malignant (M) or benign (B).

The initial data preprocessing involves dropping unnecessary columns ('id' and 'Unnamed: 32'). The 'diagnosis' column is then mapped to binary values (1 for malignant and 0 for benign) to facilitate classification tasks.

Exploratory data analysis includes generating histograms to visualize the distribution of diagnoses and subplots to compare mean values of different features between malignant and benign tumors. This provides insights into potential patterns and differences in feature distributions.

A train-test split is performed to prepare for model training and evaluation. The code then defines a generic function for creating and evaluating classification models. Logistic Regression, Decision Tree, and Random Forest classifiers are instantiated and evaluated using various subsets of features.

The Logistic Regression model achieves an accuracy of approximately 89.7%, with cross-validation scores around 89.97%. The Decision Tree classifier achieves 100% accuracy on the training set, but the mean cross-validation score is around 91.2%. The Random Forest classifier, using all features, achieves an accuracy of 95.2% on the training set, with a mean cross-validation score of 91.97%.

Feature importances are extracted from the Random Forest model, and the top features, including 'concave points_mean', 'radius_mean', 'perimeter_mean', 'area_mean', and 'concavity_mean', are used to train another Random Forest model, yielding an accuracy of 93.97% on the training set and a mean cross-validation score of 90.71%.

Subsequently, the models are evaluated on the test set, with the Random Forest classifier achieving an accuracy of 96.49% and a mean cross-validation score of 93.56%. The results indicate that the models perform well on both the training and test data, showcasing their ability to generalize to new data.
