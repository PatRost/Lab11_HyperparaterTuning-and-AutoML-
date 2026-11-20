
# Module 11 Lab – Hyperparameter Tuning and AutoML
## Group 4 – Individual Contribution Journal
**Course:** ITAI 1371 – Introduction to Machine Learning

---

### Member 1: Patrick Rostand Gandjouon Tchassem

**Contribution:**

For this lab, I took responsibility for working through the Google Colab notebook and completing the main coding activities. I started by running the baseline Random Forest model using the Iris dataset and checking the output. The model achieved 100% test accuracy, which gave me a starting point for comparing the other results.

I completed Task 1 using Grid Search to test different values for the number of trees and maximum tree depth. I ran the code and checked the best hyperparameters and cross-validation score. I then completed Task 2 using Random Search, where I tested a larger range of settings and compared its results with Grid Search. Both methods achieved a cross-validation score of 94.29%.

I also worked on the AutoML section using AutoGluon. I installed the required library, ran the training code, and reviewed the leaderboard to understand how different models performed. I checked the selected model and compared the results with the earlier Random Forest experiments.

During the assignment, I worked through coding errors, tested the notebook, and reviewed the outputs to make sure the main activities were completed correctly. I also prepared the Knowledge Check answers based on the actual results.

In addition, I organized the group's documentation by creating separate reflection and contribution Markdown files in GitHub. I prepared individual sections so that each group member could add their own reflection and describe their contribution.

My main contribution was completing the technical notebook, checking the results, preparing the Knowledge Check, and organizing the group documentation.

---

### Member 2: Kenneth Kouokam

My contribution to Lab 11 focuses on interpreting the baseline Random Forest result and explaining
how it differs from the tuning scores. The supplied notebook uses a 70/30 split of the 150 Iris
observations, giving 105 training examples and 45 test examples. Patrick reported 100% baseline
test accuracy, meaning all 45 test flowers were classified correctly. My section explains that this
result describes performance on one held-out test set and does not guarantee perfect predictions on
every future example.

I also explain the reported 94.29% cross-validation score achieved by both Grid Search and Random
Search. These searches evaluate candidate settings using five folds within the training data, rather
than using the 45 test flowers. The lower percentage therefore does not, by itself, mean that tuning
reduced performance. My analysis recommends comparing baseline and tuned models under the
same evaluation conditions, keeping the test set separate from hyperparameter selection. It also
explains that equal search scores do not necessarily mean the selected settings or predictions are
identical.

### Member 3: Saimi Manasiya
My contribution to the group project was reviewing and comparing Grid Search and Random Search. I examined how Grid Search tested 9 combinations, while Random Search sampled 10 combinations from 150 possible combinations. I reviewed the results and identified the best parameters and accuracy scores for both methods. I also learned how five-fold cross-validation evaluates the models and why we should compare their results without assuming that Random Search is always faster. This helped me understand hyperparameter tuning and contribute to the group’s overall learning.


---

### Member 4: [Enter Full Name]

**Contribution:**

---

### Member 5: [Enter Full Name]

**Contribution:**

---
