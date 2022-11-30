# Module12Challenge
The task is to create a Jupyter notebook that contains the data preparation, analysis, and visualizations for all the time series data that the company(MercadoLibre) needs to understand.

# Technologies
- python 3.9.13
- JupyterLab
- libraries: pandas, pathlib, numpy, sklearn, imblearn
- MacOs
# Installation
If you want to run the program yourself and/or enter different data, do the following:
1. To install the project files, go to the GitHub page for the workshop, click on the green Code button, then download the repository as a ZIP file. 
<img width="1209" alt="image" src="https://user-images.githubusercontent.com/111472420/204692640-96810a35-6c02-44d2-ab44-6c9ec7e2252d.png">
</br>
2. Unpack a zip file into the directory you can operate from in JupyterLab. 
<img width="844" alt="image" src="https://user-images.githubusercontent.com/111472420/204692829-3ac067d2-a75f-4f3e-a08e-ec8e577a53ef.png">

3. Install all the libraries via Terminal, open credit_risk_resampling.ipynb and Run the code!
<img width="844" alt="image" src="https://user-images.githubusercontent.com/111472420/204692969-da42c943-4d3c-4551-ac1c-87c8878652ef.png">

## Overview of the Analysis

* Credit risk poses a classification problem that’s inherently imbalanced. The task was to build a model that can identify the creditworthiness of borrowers.
* We used a dataset of historical lending activity from a peer-to-peer lending services company. </br>
<img width="862" alt="image" src="https://user-images.githubusercontent.com/111472420/204694069-d492cf15-914b-4edd-afbe-1c309e7e5a69.png"> </br>
We used the logistic regression model, that predicts both the `0` (healthy loan) and `1` (high-risk loan) classes.
* Variables we were trying to predict. </br>
<img width="558" alt="image" src="https://user-images.githubusercontent.com/111472420/204698449-1bda2096-d79b-4189-b421-4ca776da7038.png">
<img width="674" alt="image" src="https://user-images.githubusercontent.com/111472420/204698538-6ca55586-6b1b-4615-9e38-384de0943872.png"> </br>


* The stages of the machine learning process we went through as part of this analysis:
 1. Read the data

 2. Visualize the data

 3. Split the data into training and testing sets

 4. Oversample the data

 5. Fit a logistic regression model

 6. Make predictions

 7. Evaluate the model
* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).
<img width="651" alt="image" src="https://user-images.githubusercontent.com/111472420/204700606-e1545e7b-b0c0-4179-97d3-32e6351b6773.png">


## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * <b>balanced_accuracy_score</b> = 0.9520479254722232 </br> The accuracy score is high (95%).
  * <b>precision (0)</b> = 1.00 </br> All the predictions the model predicted to be 0 are actually a 0. </br> <b>precision (1)</b> = 0.85 </br> 15% of predictions the model predicted to be 1 are actually 0.
  * <b>recall (0)</b> = 0.99 </br> The model predicted 99% of total 0-labeled (healthy) loans. That's almost perfect. </br><b>recall (1)</b> = 0.91 </br>The model predicted 91% of total 1-labeled (high-risk) loans.



* Machine Learning Model 2:
  * <b>balanced_accuracy_score</b> = 0.9936781215845847 </br> The accuracy score is high (99%).
  * <b>precision (0)</b> = 1.00 </br> All the predictions the model predicted to be 0 are actually a 0. </br> <b>precision (1)</b> = 0.84 </br> 16% of predictions the model predicted to be 1 are actually 0.
  * <b>recall (0)</b> = 0.99 </br> The model predicted 99% of total 0-labeled (healthy) loans. That's almost perfect. </br><b>recall (1)</b> = 0.99 </br>The model predicted 99% of total 1-labeled (high-risk) loans.
## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* The balanced accuracy score of oversampled dataset is higher. The precision is almost the same. The recall on oversampled dataset is 99% accurate, which is a better score then when performed on original dataset. 
* The accuracy level is extremely high for both datasets. "Perfect" might be worse. I'd personally go with the first model, because the precision for the minority class is a bit higher and the recall with the second model is probably so high because the model went through testing data several times (by randomly multiplying the minority class data).
