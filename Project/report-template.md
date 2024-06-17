# Report: Predict Bike Sharing Demand with AutoGluon Solution
#### Madhawie Shashikala

## Initial Training
### What did you realize when you tried to submit your predictions? What changes were needed to the output of the predictor to submit your results?
Upon attempting to submit my predictions, I encountered syntax errors and inconsistencies in data formatting. I needed to refine the output format to align with the competition's submission requirements. Additionally, moving my tasks to SageMaker studio significantly streamlined the process and allowed for more efficient debugging and testing.

### What was the top ranked model that performed?
The best-performing model was achieved without tuning hyperparameters, but rather by incorporating additional features in the second run. This model achieved a notable Kaggle score of 0.46870, demonstrating a significant improvement from earlier scores above 1.3.

## Exploratory data analysis and feature creation
### What did the exploratory analysis find and how did you add additional features?
Exploratory analysis revealed normally distributed temperature categories. Crucial improvements came from refining the datetime feature into year, month, day, and hour components. Additional analysis indicated distinct patterns across seasons and various weather conditions, which helped in tailoring the features more effectively.

### How much better did your model preform after adding additional features and why do you think that is?
The introduction of refined datetime components (year, month, day, hour) led to a 66% improvement in model performance. This significant enhancement is likely due to the model's increased ability to capture temporal dynamics affecting bike demand.

## Hyper parameter tuning
### How much better did your model preform after trying different hyper parameters?
While the model improved compared to the initial version, it slightly underperformed relative to the version enhanced merely with additional features. Although I adhered to AutoGluon's recommendations for tabular data, the fine-tuning of hyperparameters could benefit from a deeper understanding of the model's intricacies.

### If you were given more time with this dataset, where do you think you would spend more time?
With more time, I would focus on further feature engineering, particularly exploring one-hot encoding and adjustments related to seasonal variations and work hours, which seem to have substantial impacts on bike demand.

### Create a table with the models you ran, the hyperparameters modified, and the kaggle score.
|model|score|
"initial"|1.39373
"add_features"|0.46870
"hpo"|0.49696


### Create a line plot showing the top model score for the three (or more) training runs during the project.



![model_train_score.png](img/model_train_score.png)

### Create a line plot showing the top kaggle score for the three (or more) prediction submissions during the project.



![model_test_score.png](img/model_test_score.png)

## Summary
The most substantial gains were observed through feature engineering, underscoring the value of a thorough exploratory data analysis. Moving forward, enhancing the model with nuanced insights into operational timings and seasonal impacts could further optimize performance, aiming for even lower Kaggle scores.
