#REPORT
##Abstract
Wines are a popular choice for many people and a staple drink in restaurants worldwide. Due to this, there is a great demand for high quality wines and wine sellers/makers need to be able to This study explores the application of machine learning algorithms to predict the quality of wines based on their physiochemical properties. Using a dataset consisting of 3109 wine samples, we employed a random forest regression model due to its robustness in handling both linear and non-linear relationships and its efficacy in generalizing from the training data. The model was trained on an 85/15 split of the data, which was preprocessed to remove null values. Feature importance analysis revealed that alcohol content, volatile acidity, and free sulfur dioxide are the most significant predictors of wine quality, whereas fixed acidity, pH, and residual sugar had the least impact. The model achieved a training mean squared error (MSE) of 0.03 and a validation MSE of 0.25, indicating a moderate overfitting which suggests the model's good predictive ability but also highlights an area for further optimization. This analysis provides valuable insights for wine sellers on which features to emphasize or mitigate in their quality enhancement strategies.

##Introduction
Wines are a popular choice of drink for many people and have been a staple of restaurants, social gatherings, and even quiet evenings at home. Known for its variety and complexity, wine pairs beautifully with food, enhances flavors, and often plays a key role in culinary experiences. From reds to whites, rosés to sparkling, each type offers a unique taste and aroma that can suit different moods, meals, and preferences. Each wine has physiochemical properties which make up the properties of wine such as alcohol content, density, fixed acidity etc. The degree to which these properties affect the quality of wines is important information for wine sellers to know. Knowing what specific features of wine affect the quality the most or least can help wine sellers understand which features they need to utilize in order to emphasize positively influential characteristics and mitigate negatively impactful characteristics. Machine learning techniques can be levied to draw conclusions about wine quality by using given data with quantitative values for each feature. In this report, I will discuss the machine learning algorithm used for the wine quality dataset, justify its use, and then discuss the results of the feature importance, showing which qualities are most relevant to adjusting wine quality.

##Methodology
In this project, we are given a Wine quality dataset that consists of two files: the training.csv file and test.csv file. These files are used to train the regression model so that it learns to determine wine quality and test its capabilities with unseen data. Both data files include 3109 entries, each representing a different instance of wines. The regression model is supervised, meaning that the train csv specifically has a quality column that gives the quality for each row. The development process is thus as follows: First, we read the csv files to store the data in variables. Before training, we also preprocess the data by searching for null values in both the training and test sets to prevent skewing of results. Then, we split the dataset into 85% training and 15% testing. Next, we need to decide on a regression model to train and generate predictions. There are a number of different techniques that can be used for this purpose. In our project, however, we opt to use a random forest algorithm. We use a random forest algorithm due to its flexibility because it can handle both linear and non-linear relationships between attributes of wine. Because we are dealing with continuous values, its multiple tree generation method means that it can understand more complex correlations between chemicals and wine quality. Also, predictions for each generated tree reduce the possibility of overfitting, making Random Forest trees a more suitable candidate for generalizing wine quality. Therefore, we write a random forest regression model for our project to generate our predictions.

##Results
Feature Importance results

For feature importance, the top 3 most important factors are:

alcohol (0.24)
volatile.acidity (0.10)
free.sulfur.dioxide (0.10)
The top 3 least important factors are:

fixed.acidity (0.04)
residual sugar (0.06)
pH (0.06)
MSE and Cross Validation results

Training MSE : 0.03 Validation scores: 0.25 MSE scores for each fold: [0.22112217 0.30412225 0.26695389 0.31039208 0.33939777] Average MSE: 0.29

##Conclusion
In this report, we developed and trained a random forest regression model to predict wine quality from physiochemical properties and their values. The model has demonstrated promising results, reflecting the capability to effectively capture and interpret the complex relationships within the data. Our analysis identified alcohol content, volatile acidity, and free sulfur dioxide as the most influential factors affecting wine quality. It provides a clear direction for winemakers and sellers on which characteristics to focus their quality improvement efforts. While the model exhibited some degree of overfitting, as indicated by the disparity between the training and validation MSE, the relatively close values suggest that it can generalize reasonably well to new data.
