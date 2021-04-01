# Health Insurance Lead Prediction - Kaggle Competition
## Job-A-Thon - Analytics Vidhya, Health Insurance

* **Author**: Miguel Santana

Thank you for reviewing this repository. The author's contact info, blog post, sources and social media profiles are listed below under **further information.**

### Project Methodology
FinMan Company is looking to leverage their client base by cross selling insurance products to existing customers. Insurance policies are offered to prospective and existing clients based on website landing and consumer election to fill out additional information forms. FinMan company would like to leverage their acquired information to classify positive leads for outreach programs using machine learning classifiers. 

### Data and Analytical Structure
The project dataset is provided by Analytics Vidhya via Kaggle. Data includes demographic features, policy features (for current customers) and example positive classifications for ML model validation and interpretation. The source can be found [here.](https://www.kaggle.com/imsparsh/jobathon-analytics-vidhya?select=sample_submission.csv) The project analysis followed the OSEMN framework: Obtain, Scrub, Explore, Model and Interpret.

![!](/images/OSEMN.png)

### Data Processing and Modeling

Once data processing (filling nulls, feature engineering, etc) was completed, a single column was dropped in order to combat multicollinearity. Categorical variables were encoded using a helper function which groups the category by a target variable, sorts the target values and enumerates the labels (treating them as ordinal values). This allowed the features to be converted and representative of the appropriate scale in a single step. This method is credited to Dr. Soledad Galli. 

## Pycaret Modeling

#### Target Imbalance

![!](/images/pycaretimbalance.png)

#### Balanced Target | SMOTE

![!](/images/pycaretsmote.png)

## Scikit-learn Modeling

GridSearchCV using Gradient Boosting Classifier was performed. 

### Model Validation

**Scores**

![!](/images/validation.png)

## Interpreting Results | Feature Importance

![!](/images/featureimportance.jpg)

### Reco Policy Category

![!](/images/policycategoryxresponse.jpg)

![!](/images/top5categoryxresponse.jpg)

### Reco Policy Premium

![!](/images/premiumbin.jpg)

![!](/images/top5premiumbin.jpg)

### City Code

![!](/images/citycode.jpg)

![!](/images/top11citycode.jpg)

## Recommendations
The model's top 3 features were Reco Policy Category, Reco Policy Premium and City Code. Within those three categories, subcategories yielded the highest positive to total response ratios. It is recommended to focus on clients in/with:

City Codes: C1, C2, C13, C23

Reco Policy Categories: 15, 22

Reco Policy Premiums between: 15,000 & 19,999.

#### Limitations
The project was limited by the anonymity of the data. Specifically the geographic data that could have been used for additional feature engineering leading to higher scores.

#### Future Work
Future models can be created using more complicated feature engineering and analysis such as clustering of the geographic features. For the purposes of this project, doing so would have complicated the output and made it difficult to implement within a real workplace.

### Further Information
Please review the narrative of our analysis in [our jupyter notebook](./Jupyter_notebook.ipynb) or review our [presentation](./presentation.pdf)

For any additional questions, please reach out via email at santana2.miguel@gmail.com, on [LinkedIn](https://www.linkedin.com/in/miguel-angel-santana-ii-mba-51467276/) or on [Twitter.](https://twitter.com/msantana_ds)

##### Repository Structure:

```

├── README.md               <- The top-level README for reviewers of this project.
├── jupyter_notebook.ipynb     <- narrative documentation of analysis in jupyter notebook
├── presentation.pdf        <- pdf version of project presentation

```

