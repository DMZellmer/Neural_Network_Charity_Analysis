# Neural_Network_Charity_Analysis


# Overview
The purpose of this analysis was to use machine learning on a dataset of 34,000 organizations that have received funding from the foundation, Alphabet Soup, to predict whether applicants will be successful if funded. Before implementing machine learning models, however, the data required preprocessing.



# Results 


## Data Preprocessing

![image](https://user-images.githubusercontent.com/86337475/141716491-a0092de1-d4d8-4f40-9d6b-39a51153b413.png)


* Target variable = IS_SUCCESSFUL column values



* Variable features (all other columns besides IS_SUCCESSFUL =
 
  APPLICATION_TYPE
  
  AFFILIATION                 
  CLASSIFICATION              
  USE_CASE                     
  ORGANIZATION                 
  STATUS                       
  INCOME_AMT                   
  SPECIAL_CONSIDERATIONS       
  ASK_AMT  



![image](https://user-images.githubusercontent.com/86337475/141716559-643d3b38-d434-4909-8897-899cc5ae09c6.png)


* Variables EIN and NAME were removed from the input data because they did not contain meaningful values.



## Compiling, Training, and Evaluating the Model


![image](https://user-images.githubusercontent.com/86337475/141717129-6f987ccd-7af2-4ea8-90fd-e82ce166e63f.png)


Given that there were 9 input features, we chose to populate our two hidden layers with 27 neurons each, as (input)x3 is considered a good rule of thumb to start with when training machine learning models. Rectified Linear Unit (Relu) was selected as the initial activation function because it is the most common activation used in machine learning.


Unfortunately, we were not able to achieve target model perfomance of 75% accuracy. To do so, we doubled the number of epochs- from 100 to 200, added a third hidden layer with 27 neurons, and finally used the Random Forest Classifier to predict the data. The first two attempts both achieved an accuracy of 72.4%, which when rounded to the tenth of a percent, is the same accuracy of the initial attempt. The Random Forest Classifier was even less accurate at 70.6%.

![image](https://user-images.githubusercontent.com/86337475/141719253-667f4b86-606f-4123-9b89-bec7264b090b.png)


## Summary

In summary, the results of our attempt to optimize the model to achieve the target perfomance of 75% accuracy was a disapointing failure. However, we are confident that with more time to optimize and tweak the parameters of the model, we would reach the threshold of 75% predictive accuracy. Sigmoid activation functions were called on the hidden layers, but this did not improve model performance (data not shown). Perhaps the tanh activation function would perform better with this dataset, although it is a similar function to sigmoid activation function. After closer analysis, the data preprocessing step transformed the X_train features into a larger length set of values than initially thought (see image below).

![image](https://user-images.githubusercontent.com/86337475/141719949-5552c457-1e0a-494a-a421-cb37199fc31b.png)

Therefore, using the (input)x3 general rule of thumb, we should have added 123 neurons (41 x 3) to our hidden layers. This number initially seemed too high, which was why it wasn't used. Future analysis would most definitely test the accuracy of a model containing 123 neurons per hidden layer, although this would require additional time and computational power. 
