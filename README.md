**Ensemble_Learning_Methods_Chapter7_Lab**

**Overview**


The lab covers three main ensemble learning approaches:

**Majority Voting Classifier** - Combines multiple classifiers through majority voting

**Bagging** - Bootstrap aggregating with Decision Trees

**Boosting** - Adaptive boosting (AdaBoost) with Decision Tree stumps

Datasets Used
Iris Dataset (Versicolor vs Virginica classes only)

Wine Dataset (Classes 2 and 3 only)

Implementation Details
1. **Majority Vote Classifier**
Custom implementation of MajorityVoteClassifier

Combines Logistic Regression, Decision Tree, and KNN classifiers

Supports both class label voting and probability-based voting

2. **Bagging Classifier**
Uses BaggingClassifier from scikit-learn

Compares performance of single Decision Tree vs Bagged Decision Trees

Visualizes decision boundaries

3. **AdaBoost Classifier**
Uses AdaBoostClassifier from scikit-learn

Implements adaptive boosting with Decision Tree stumps

Analyzes error convergence over iterations

Includes hyperparameter tuning with GridSearchCV

Key Findings
Performance Comparison
The comprehensive comparison of classifiers on the Iris dataset showed:

Classifier	Mean Accuracy	Std Accuracy
KNN	0.951818	0.048285


Logistic Regression	0.941818 	0.047621


Voting Classifier	0.940909 	0.065839


Bagging	0.940909 	0.065839


Random Forest	0.931818 	0.063278


Decision Tree	0.922727	 0.059231


AdaBoost	0.922727	 0.071841


Hyperparameter Tuning Results


AdaBoost: Best parameters were {'estimator__max_depth': 1, 'learning_rate': 0.1, 'n_estimators': 50} with score 0.971

Bagging: Best parameters were {'max_features': 0.8, 'max_samples': 0.5, 'n_estimators': 200} with score 0.952

**Key Insights**
Ensemble Methods Advantages
Majority Voting: Aggregates multiple perspectives, smoothing out individual classifier mistakes

Bagging: Reduces variance by averaging multiple bootstrap samples

AdaBoost: Adaptively focuses on difficult samples, creating a strong classifier from weak learners

When Ensembles Work Best


When individual classifiers are diverse and uncorrelated

When dealing with high-variance models

When you want to reduce overfitting

Potential Limitations
Ensemble methods can perform worse if all base classifiers are weak or highly correlated

Increased computational complexity

Potential overfitting with too many iterations (especially in boosting)

**Dependencies**

numpy

pandas

scikit-learn

matplotlib

**Usage**

Run the notebook cells sequentially to:

Implement ensemble classifiers

Compare their performance

Visualize results and decision boundaries

Tune hyperparameters for optimal performance

The notebook provides practical examples of how ensemble methods can improve prediction accuracy and model robustness compared to individual classifiers.

