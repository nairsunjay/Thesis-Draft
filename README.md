Validating and verifying address data comes with unique sets of challenges. The chal-
lenges arise due to varying reasons starting from lack of international address standard

to diverse addressing systems around the world. To tackle the address data problem,
many commercial and open-source validation services are available. However, these have
similar limitations making the usage of such services less useful among organizations. So
to explore and tackle the address problem, address data from GLEIF was taken.

GLEIF data has address representations from most parts of the world, making it a rep-
resentative dataset of diverse addresses. GLEIF, like any other organization, has to

manually validate addresses, which leads to wasted time and effort. To address this
problem we propose to follow the CRISP-DM process in order to implement an outliers
prediction model. The address data features are then explored.

Next, the data is sampled and transformed into suitable vector space for the outlier analy-
sis. The Term Frequency-Inverse Document Frequency (TF-IDF) vectorization (free text

fields) and One hot encoding (categorical field) are used for data transformation based
on the type of the features. The algorithms to perform anomaly detection are surveyed.

Based on the performance metrics and suitability to the data set two unsupervised learn-
ing methods, namely isolation forest and autoencoders are implemented.

The proposed pipeline is an anomaly detection prediction model. The task at hand is
to use the current ”challenge” information to detect potential quality defects in address
data. The results of the and predictive analysis is visually plotted and summarized using
PCA plot. To compare the performance of the implemented outlier detection model,
the Area Under the Receiver Operating Characteristic Curve (AUC) and Area under the

Precision-Recall Curve (AUCPR) are plotted. Based on the evaluation results, it is ob-
served that both prediction models have similar performance on the dataset, but Isolation

forest prediction model performs marginally better than Autoencoder implementation.
The data pipeline not only provides a framework for GLIEF to classify their address data
but also a generic framework that can be used for outlier detection analysis by extending
the framework. The goal is to keep the framework modular enough to plug in a new
outlier detection model or data transformation method and extendable to new datasets.
