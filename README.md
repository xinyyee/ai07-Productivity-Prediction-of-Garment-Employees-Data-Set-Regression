# Productivity Prediction of Garment Employees Data Set(Regression)
## 1.Objective

<p align="justify"> 
The objective is to predict the productivity performance of the working team in Garment Inudstry.Since Germant Industry had a huge global demand products it is important to track, analysis and predict the productivity of the working teams in their factories.</p>

[Dataset Download Link](https://archive.ics.uci.edu/ml/datasets/Productivity+Prediction+of+Garment+Employees#)

## 2.IDE and Framework
Google Colab was implemented as integrated development environment.Besides,the main frameworks used in this project were Pandas,Numpy,Scikit-Learn and TensorFlow Keras.
 
## 3.Methodology 
### 3.1 Data Pipeline 
<p align="justify"> 
Data was loaded and the data was preprocessed such that typographical error in department column such as "finishing " will be replaced to "finishing".Besides,categorical features such as day,department and quarter columns were converted to numeric form.In addition, the undefined wip value (product work in progress) will be assigned to zero.Next, the date column was converted to more columns such as year,month,day of year, week, week of year,day of week and weekday.Moreover, the value of actual productivity column which exceed one will be replaced to one.Subsequently the dataset will be splitted into 5 different group dataset with ratio of 80:20 train-test dataset by applying k-fold cross-validation.Besides, train dataset will be standardized.</p>


### 3.2 Model Pipeline
 <p align="justify"> 
 A functional API model was created to solve the regression problem.The architecture of the model and number of nodes of each layer was shown as figure below.All the hidden layers consists of exponential linear unit(ELU) activation function and the outptut layer it consists of linear activation function.</p>

![download](https://user-images.githubusercontent.com/109932205/182021644-13f22f4a-8e49-4d92-9fd9-6216b31bbdbd.png)


 

 <p align="justify"> 
The model was trained with 5 k-fold cross-validation dataset ,the optimizers of adam learning rate was set as 0.00001 and the batch size was set as 200.The epochs value for each k-fold cross validation and result of the traning and validation was shown in the table below.</p>

| K-fold Cross Validation | 1      | 2      | 3      | 4      | 5      |
| ----------------------- | ------ | ------ | ------ | ------ | ------ |
| Epochs                  | 200    | 100    | 100    | 50     | 50     |
| Training Loss           | 0.0225 | 0.0172 | 0.0151 | 0.0139 | 0.0138 |
| Training MAE            | 0.1131 | 0.0968 | 0.0882 | 0.0838 | 0.0819 |
| Validation Loss         | 0.0231 | 0.0180 | 0.0162 | 0.0149 | 0.0139 |
| Validation MAE          | 0.1043 | 0.0929 | 0.0839 | 0.0828 | 0.0781 |



## 4.Result 
The model was tested with the random data obtained from the dataset.The figure below show some predictions result of training result. 

![image](https://user-images.githubusercontent.com/109932205/182021773-f12f034d-61ad-4c41-bc1e-6a3a104c537a.png)

*Figure 1 Result of Predictions of Trained Model(left=prediction,right=label)*

![image](https://user-images.githubusercontent.com/109932205/182021802-9930d247-761e-404c-aae7-e8caf15d5617.png)

*Figure 2 Graph of Predicted Y vs Label*

![image](https://user-images.githubusercontent.com/109932205/182021831-ed8e36e9-691c-4ea2-bc15-8884a903c115.png)

*Figure 3 Metrics of Regression*


