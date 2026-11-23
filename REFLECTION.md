
# Module 11 Lab – Hyperparameter Tuning and AutoML
## Group 4 – Reflection Journal
**Course:** ITAI 1371 – Introduction to Machine Learning

---

### Member 1: Patrick Rostand Gandjouon Tchassem

**Reflection:**

This lab helped me understand why hyperparameter tuning is important in machine learning. Before working on this assignment, I thought that once a model was trained and gave a good accuracy score, there was not much else to do. After completing the lab, I realized that we can adjust different settings to see how they affect the model's performance.

One part I found interesting was comparing Grid Search and Random Search. Grid Search tested every combination we provided, while Random Search selected combinations from a larger range. In our results, both methods achieved 94.29% cross-validation accuracy, even though they selected different hyperparameters. This helped me understand that there can be more than one good combination of settings for the same dataset.

I also learned something important from the baseline model. It achieved 100% accuracy on the test data, but the tuning methods gave lower cross-validation scores. At first, that seemed confusing. I learned that these scores come from different evaluation methods, so they should not be compared as if they measured exactly the same thing.

Another interesting part was using AutoGluon. Instead of manually selecting and tuning one algorithm, AutoGluon trained and compared several models automatically. Seeing the leaderboard helped me understand how AutoML can save time and make the machine-learning workflow easier to manage. I also noticed that the model selected using validation results was not necessarily the one with the highest test accuracy.

Overall, this lab improved my understanding of hyperparameters, model evaluation, and automation. It also helped me become more comfortable running Python code in Google Colab, troubleshooting errors, and reviewing the results instead of just focusing on whether the code runs.

---

### Member 2: Kenneth Kouokam

For Module 11, my role is interpreting the baseline and evaluation results. The two reported
percentages raise an interesting question: why would a baseline model score 100% while the tuning
methods report 94.29%? Looking only at the numbers could suggest that tuning made the model
worse. Understanding where each score comes from gives me a different explanation. The scores
describe different evaluations, so I need to examine the data used for each before drawing a
conclusion.

The baseline uses 105 Iris examples for training and 45 for testing. Its reported 100% test accuracy
means that it correctly classified those 45 flowers. That is a useful result, but it is still based on a
small set of observations. A single mistake would reduce the score to about 97.8%. This connects to
the earlier ensemble lab: a perfect score on one split does not settle which model will be more reliable
when the examples change.

The tuning scores come from five-fold cross-validation within the 105 training examples. For each
candidate setting, the process repeatedly trains on four folds and evaluates on the remaining fold. In
this setup, each fit uses 84 examples and validates on 21. This is different from fitting the baseline on
all 105 training examples and evaluating on the separate test set. The average validation score helps
compare candidate settings, but it should not be treated as the same measurement as the baseline
test accuracy.

The matching 94.29% scores from Grid Search and Random Search also need careful interpretation.
They tell me that the best reported average scores were equal at the displayed precision. They do not
establish that both searches selected identical settings or made the same predictions. To understand
the comparison more fully, I would want to examine the best parameters and the scores across the
individual folds. Those details would help explain a tie instead of assuming that the two search
methods behaved identically.

My main takeaway is that a score only becomes useful when I understand how it was produced.
Hyperparameter selection should use training and validation data, while the test set should remain
separate for final evaluation. Repeatedly changing settings after inspecting test results would weaken
that separation. For a fair comparison, I would evaluate the baseline and selected tuned models
under matching conditions and explain both the results and their limits. This role helps me connect
the idea of tuning to the practical question of whether a comparison actually supports the conclusion
being made.

### Member 3:saimi manasiya

In this lab, I learned the difference between Grid Search and Random Search and how they help improve machine learning models. I understood that Grid Search tests every combination of the selected hyperparameters, while Random Search selects a limited number of combinations from a larger search space. I also learned how five-fold cross-validation helps evaluate model performance more reliably. Both methods achieved the same cross-validation accuracy of 94.29%, but they found different best hyperparameter settings. This activity helped me better understand how different tuning methods work and how they can be used to optimize machine learning models.

---

### Member 4: Anavictoria Cavazos

After working on module 11, I learned the difference between model parameters and hyperparameters and how they work in machine learning. 
I understood more how the hyperparameters control complexity. For instance, increasing the estimators stabilizes predictions without 
overfitting, and  max_depth as well as min_samples_split help trees not memorize training noise.

Also, this lab helped me understand the difference between a single test split and cross-validation, and see how they impact the 
results, and what may appear to be a good accuracy of the model can actually just be showing a certain percentage of the model. The 5-
fold cross-validation gave an accuracy of 94.29% compared to the 100% given by the single test split, but the 5-fold is better because it 
shows the performance through different folds. This just reinforces the concept of splitting data multiple times to see how good the 
model really is. 

Aside from this, what I enjoyed learning from this module was the AutoML because it shows a much faster way of writing the preprocessing, 
tuning hyperparameters, and all the other parts that were used for the coding, written in a much simpler way in a few lines. This is very 
crucial to know and use in future coding, as it can decrease the time used in coding or programming. Overall, this lab helped me compare 
certain aspects of machine learning that are new and that are known, and seeing how they differ and apply with the iris dataset, which 
shows me ways of seeing and handling future datasets. 


---

### Member 5: Hashim Sayed Hoosini

Going into this lab, I felt pretty comfortable with the basics, but this was the first time I got to see how tuning actually behaves under the hood. Setting up the grid of hyperparameters for the Random Forest model and watching the search process run was a huge eye-opener. It made me realize how much of machine learning is about finding that sweet spot in model configurations before you even start the final training run.

When we started running the experiments, I wasn't entirely sure how much of a difference the search methods would actually make in practice. But comparing Grid Search and Random Search directly turned out to be super interesting. Grid Search felt really systematic since it checks every single combination, but it also felt like a lot of heavy lifting. It was satisfying to watch the progress bar finish, though it made me realize how slow this would get on a larger dataset.

Random Search was the part that surprised me the most because of how efficient it was. Even though it just samples combinations randomly from a distribution, it managed to find equally strong hyperparameters (getting us that same 94.29% validation accuracy) in a fraction of the computation time. It showed me that you don't always need to test every single option to get a solid, optimized setup, which is a great trick to keep in mind for future projects.

Using AutoGluon at the end of the lab was wild. Seeing how it ran multiple algorithms like XGBoost, LightGBM, and neural networks, and then stacked them into an ensemble automatically, made me realize how much manual work can be streamlined. It definitely showed me how valuable AutoML tools are for prototyping quickly when you don't have hours to manually tune separate models.

Overall, this lab helped bridge the gap between theory and code for me. Moving from a simple baseline model to systematic searches, and finally to automated pipelines, gave me a clear picture of the tuning process. It makes me feel much more confident about setting up my own modeling pipelines in the future without just relying on default settings.
