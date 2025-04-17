🚨 Cyberbullying Detection: A Data Mining Approach
📘 Project Overview

This project explores how advanced data mining and machine learning techniques can be used to detect and categorize various forms of cyberbullying on social media platforms. With cyberbullying becoming increasingly pervasive across online communities, there is a critical need for automated systems that can understand and moderate such harmful interactions effectively. We utilized publicly available datasets to build models that classify cyberbullying based on factors like age, gender, ethnicity, religion, and more, aiming to uncover patterns that can guide better detection mechanisms and foster safer online environments.
❗ Problem Definition

Cyberbullying is a form of online harassment that can lead to severe emotional, psychological, and social consequences. It often goes unnoticed or underreported due to the anonymous and persistent nature of digital communication. Traditional moderation techniques are frequently ineffective in identifying evolving and context-specific abusive behavior. The core objective of this project is to develop an automated, scalable system that leverages data mining and natural language processing techniques to identify, classify, and analyze cyberbullying content. By doing so, we aim to enhance digital safety and contribute towards early detection and prevention of online abuse.
📊 Dataset

We used two primary datasets sourced from Kaggle. The first is the Fine-Grained Balanced Cyberbullying Dataset, which contains over 47,000 tweets labeled into categories including Age, Gender, Religion, Ethnicity, Sexism, and a general “Other cyberbullying” category. Each category uses binary labeling to denote the presence or absence of cyberbullying. The second dataset, Twitter Sexism Parsed Dataset, focuses specifically on detecting sexist language on Twitter and is part of a broader dataset that includes data from platforms like YouTube and Wikipedia Talk pages.
🧰 Techniques and Tools Used

We began with extensive text preprocessing, which involved converting text to lowercase, removing punctuation and common stopwords (including custom ones relevant to tweets), and applying stemming to reduce words to their root forms.

For classification, we trained and evaluated three models:

    Logistic Regression (using a multinomial approach)

    Random Forest

    Support Vector Machine (SVM)

To uncover latent patterns and relationships, we applied unsupervised techniques like K-Means Clustering with dimensionality reduction using PCA (Principal Component Analysis) and identified the optimal number of clusters using the Elbow Method. The textual data was vectorized using TF-IDF to convert tweets into numerical features.

Furthermore, we performed Association Rule Mining using the Apriori algorithm to discover strong co-occurrence patterns in the dataset, evaluated using metrics such as support, confidence, lift, and conviction.
🔍 Key Findings

Our classification experiments revealed that the Random Forest model provided the best overall accuracy (77.34%), especially in detecting cyberbullying related to age and ethnicity. However, all models struggled with underrepresented categories such as "Sexism", largely due to dataset imbalance.

In clustering, we identified four distinct thematic clusters in the data, highlighting patterns such as religious/political discussions, school-related bullying, offensive ethnic language, and jokes involving sexual orientation. The Elbow Method supported the choice of four clusters, although 3D visualizations revealed overlapping group boundaries.

Association rule mining surfaced several interesting patterns, including relationships between specific offensive terms and cyberbullying types. These rules not only validated known trends but also provided new insights into language patterns across different abuse categories.
📈 Results

    Random Forest showed strong classification metrics with recall scores nearing 98% in categories like Age and Ethnicity.

    SVM and Logistic Regression models also performed reasonably well but struggled similarly with the "Sexism" and "Other" categories.

    Clustering via K-Means identified four main topic areas, though the clustering quality (measured via silhouette score) was moderate.

    Association rules revealed meaningful linguistic connections, indicating potential for rule-based augmentation of detection systems.

🚀 Future Scope

While our models yielded valuable insights, there’s room for improvement. One of the major limitations was the class imbalance in the dataset, particularly in categories like "Sexism," which significantly impacted model performance. Future work will focus on collecting a more balanced dataset, exploring hierarchical clustering for more nuanced groupings, and integrating sentiment analysis for better context understanding. Additionally, implementing deep learning models and leveraging distributed computing could improve scalability and accuracy for real-world applications.
