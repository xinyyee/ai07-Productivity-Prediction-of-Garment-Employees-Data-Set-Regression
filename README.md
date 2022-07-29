# ai07-Productivity-Prediction-of-Garment-Employees-Data-Set
## 1.Objective
The objective is to predict the productivity performance of the working team in Garment Inudstry.Since Germant Industry had a huge global demand products it is important to track, analysis and predict the productivity of the working teams in their factories.

[Dataset Download Link](https://archive.ics.uci.edu/ml/datasets/Productivity+Prediction+of+Garment+Employees#)

## 2.IDE and Framework
Google Colab was implemented integrated development environment.Besides,the main frameworks used in this project were Pandas,Numpy,Scikit-Learn and TensorFlow Keras.
 
## 3.Methodology 
# 3.1 Data Pipeline 
Data was loaded and the data was preprocessed such that typographical error in department column such as "finishing " will be replaced to "finishing".Besides,categorical features such as day,department and quarter columns were converted to numeric form.In addition, the undefined wip(product work in progress) value will be assigned to zero.Subsequently the dataset will be splitted into 4 different group dataset with ratio of 75:25 train-test dataset by applying k-fold cross-validation.Besides, train dataset will be standardized.


 # 3.2 Model Pipeline
 A functional API model was created to solve the regression problem.The architecture of the model and number of nodes of each layer was shown as figure below.All the hidden layers consists of exponential linear unit(ELU) activation function except the outptut layer it consists of linear activation function.
 
 ![Architecture of model](https://user-images.githubusercontent.com/109932205/181765662-c14af61e-d604-4b9c-a00d-b5b47d12b63c.png)



The model was trained with a batch size 700 and epochs of 40 with 4 k-fold cross-validation dataset.The result of the traning and validation was shown in the table below.Next, the training process graph was shown in the figure below.It can observed a convergence sign for the training process.
|             | Training | Validation |
| ----------- | -------- | ---------- |
| Loss        | 0.0168   | 0.0174     |
| mae         | 0.0902   | 0.886      |

![image](https://user-images.githubusercontent.com/109932205/181766466-fbd0609a-8062-49b0-8c81-c26e534c4f19.png)


## 4.Result 
The model was tested with the random data obtained from the dataset.The figure below show some predictions result of training result. 


![image](https://user-images.githubusercontent.com/109932205/181768195-c2f111cd-14dd-47f4-99a5-992f9af3fb34.png)

*Figure 1 Arruracy and loss of Prediction Data*

![image](https://user-images.githubusercontent.com/109932205/181768232-b8f3c22d-49ba-4ae5-a823-5b2e0dd18f37.png)

*Figure 2 Result of Predictions of Trained Model(left=prediction,right=label)*

![image](https://user-images.githubusercontent.com/109932205/181768325-85b265c7-a4b1-41f0-ab82-79aaa94b6859.png)

*Figure 3 Graph of Predicted Y vs Label*

![image](https://user-images.githubusercontent.com/109932205/181768386-aa04d788-29ce-4da8-a74f-05a35a217cc3.png)

*Figure 4 Metrics of Regression*


