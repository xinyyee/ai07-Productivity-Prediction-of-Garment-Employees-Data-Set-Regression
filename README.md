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

The model was trained with a batch size 64 and epochs of 400.Based on Figure 1 to 4 it show that all the model trained with different dataset show a convergence of model training.

![1](https://user-images.githubusercontent.com/109932205/180920130-c7417f0f-9423-4756-9d93-107400b8b1de.png)

*Figure 1.Training using remove columns of wip and date dataset*

![2](https://user-images.githubusercontent.com/109932205/180920172-d9a7c6ea-72c3-4fd7-a67c-a21113ac3200.png)

*Figure 2.Training using remove column of data dataset.*

![3](https://user-images.githubusercontent.com/109932205/180920216-b8a702d8-2b62-4992-8074-6ce226b964ed.png)

*Figrue 3.Training using remove columns of wip and remain date column dataset.*

![4](https://user-images.githubusercontent.com/109932205/180920257-a6c8f547-fded-430c-b1cd-3da4d789e175.png)

*Figure 4.Training using remove columns of wip and date dataset.*



## 4.Result 
The model was tested with the test data.All the evaluation result was shown in the table below.
|Dataset|MAE|MSE|RMSE|AVG|
|:----|:----|:----|:----|:----|
|Remove columns of wip and date |0.09|0.019|0.137|0.082|
|Remove column of date|0.091|0.016|0.127|0.078|
|Remove columns of wip and remain date column|0.093|0.018|0.133|0.081|
|Remain columns of wip and date |0.095|0.017|0.133|0.082|

![1](https://user-images.githubusercontent.com/109932205/180923227-083799e4-b903-4b1b-9492-987e56e919b5.png)

*Figure 5.Predict using remove columns of wip and date dataset*

![2](https://user-images.githubusercontent.com/109932205/180923288-b3c8fc35-264f-428d-a0a4-96852e61e07a.png)

*Figure 6.Predict using remove columns of date dataset*

![3](https://user-images.githubusercontent.com/109932205/180923335-81aa2552-65b2-4067-80e9-bdc077fcff95.png)


*Figure 7.Predict using remove columns of wip and remain date column date dataset*

![4](https://user-images.githubusercontent.com/109932205/180923400-bcaca60a-c5aa-489f-81b7-0ffabe30dc39.png)

*Figure 8.Predict using remain columns of wip and date dataset*


**According to the result, the dataset for remove column of date give a highest prediction compare to other dataset.**




