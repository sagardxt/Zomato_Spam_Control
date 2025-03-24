1. Problem Statement
Overview of the issue:
In recent years, the importance of reviews on platforms like Zomato has significantly increased. Restaurant ratings play a major role in attracting customers. However, there has been a rise in fake or spam reviews planted by restaurant owners or competitors, which can mislead potential customers and unfairly impact a restaurant's reputation.

Why it matters:

Fake reviews distort the true customer experience.

They undermine the credibility of the platform, making it unreliable for users.

Spam reviews can harm restaurants' credibility and skew ratings.

Current challenges:

Zomato's existing spam detection system is primarily based on pattern matching and behavior tracking but is not perfect.

Smart spam tactics have become increasingly difficult to detect using basic filters.

2. Objective
The goal is to build a robust spam detection system that can classify reviews as either spam or non-spam, improving the overall trustworthiness of the platform.

Implement a system that can detect both overt and subtle spam reviews to maintain neutrality and protect the integrity of the platform.

3. Approach and Methodology
Data Collection & Exploration:

Dataset: We are using the Zomato review dataset, which contains key features like review_text, rating, user_activity, and more.

EDA (Exploratory Data Analysis):

Analyzed the distribution of spam reviews using visualizations (e.g., countplot).

Created word clouds to understand the common words in spam vs non-spam reviews.

Feature Engineering:

Derived new features like review_length (length of the review) and word_count (number of words in the review).

Encoded categorical features like review_sentiment using LabelEncoder.

Model Development:

Logistic Regression: Started with a basic Logistic Regression model for initial experimentation.

Random Forest Classifier: A more powerful ensemble method to handle both linear and non-linear patterns.

XGBoost: A boosting algorithm that can help in handling complex data and has shown success in many machine learning competitions.

Model Evaluation:

Accuracy, Precision, Recall, and F1-Score were used to evaluate each model.

We also visualized confusion matrices to better understand false positives and false negatives.

Results Comparison:

Compare the performance of Logistic Regression, Random Forest, and XGBoost.

Based on the results, we'll decide which model provides the best balance of performance and efficiency.

4. Results and Insights
Logistic Regression: Provided a baseline, but did not perform as well in detecting subtle spam patterns.

Random Forest: Showed strong performance by capturing complex relationships in the data. It is able to handle a mix of numerical and categorical data effectively.

XGBoost: Outperformed other models in many metrics, especially in handling imbalanced data and complex patterns. It provided high recall, ensuring that fewer spam reviews were missed.

Confusion Matrix: Helps visualize the number of true positives, false positives, true negatives, and false negatives, showing how well the model is performing on both classes (spam vs non-spam).
