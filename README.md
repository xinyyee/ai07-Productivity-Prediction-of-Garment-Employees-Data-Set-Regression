# ai07-Productivity-Prediction-of-Garment-Employees-Data-Set
## 1.Objective
The objective is to predict the productivity performance of the working team in Garment Inudstry.Since Germant Industry had a huge global demand products it is important to track, analysis and predict the productivity of the working teams in their factories.

[Dataset Download Link](https://archive.ics.uci.edu/ml/datasets/Productivity+Prediction+of+Garment+Employees#)

 ## 2.IDE and Framework
Google Colab was implemented integrated development environment.Besides,the main frameworks used in this project were Pandas,Numpy,Scikit-Learn and TensorFlow Keras
 
 ## 3.Methodology 
 # 3.1 Data Pipeline 
Data was loaded and it used several preprocessed data method to generate several datasets show in the table below.Next,the typographical error in department column such as "finishing " will be replaced to "finishing".Besides,categorical features such as day,department and quarter columns were converted to numeric form.In addition, the undefined wip(product work in progress) value will be assigned to zero if the wip column remain.Subsequently the data will be splitted into train-validation-test sets with a ratio of 70:20:10.
|Dataset|
|:----|
|Remove columns of wip and date|
|Remove column of date|
|Remove columns of wip and remain date column|
|Remain columns of wip and date|

 # 3.2 Model Pipeline
 A functional API model was created to solve the regression problem.The architecture of the model and number of nodes of each layer was shown as figure below.Moreover,the model consists of one input layer, five hidden layers each hidden layers was implemented exponential linear unit(ELU) and one output layer with linear activation function.
 
 ![Architecture of model](https://user-images.githubusercontent.com/109932205/180914544-b257bfc4-0a67-4dcf-b0f1-74e4e5fea57d.png)

The model was trained with a batch size 64 and epochs of 400.





## 4.Result 
The model was tested with the test data.All the evaluation result was shown in the table below.
|Dataset|MAE|MSE|RMSE|AVG|
|:----|:----|:----|:----|:----|
|Remove columns of wip and date |0.09|0.019|0.137|0.082|
|Remove column of date|0.091|0.016|0.127|0.078|
|Remove columns of wip and remain date column|0.093|0.018|0.133|0.081|
|Remain columns of wip and date |0.095|0.017|0.133|0.082|









