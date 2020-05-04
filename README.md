# SEPTA On-Time-Performance(OTP) Prediction

This project intends to locate the elements that cause train delays. The goal is to build a model which takes in train number, date, and station, and gives the predicted arrival time of the train. 

Potential models include decision tree, k-nearest-neighbor, or neural network. As for feature selection, besides the [given dataset](https://www.kaggle.com/septa/on-time-performance), weather data will also be collected via an API as weather could be a significant factor in OTP. When giving predictions, if the selected date is within 7 days, a weather forecast would also be pulled to be considered. Otherwise, weather would be excluded from the model. 

This project is particularly of interest to people who commutes daily from central Philadelphia to the suburban area. The predictions could also be useful for train schedulers and dispatchers to help them understand the bottleneck of the rail network.

One obvious challenge is to connect the delays of previous trains into a feature of the current instance. The dataset is given in a way that all trains are separately stored, so a link must be established for consecutive trains. To make things more complex, in the segment between 30th Station and Jefferson Station, all trains share the same rail. Therefore, there perhaps will be a reorganization of train sequence (for instance, an Airport Line train is inserted between two previously connected Newark Line trains). Another challenge would be the huge class imbalance. On time trains could far exceed late trains in number, and this must be taken into account. 

This is the final project of CIS 545 Big Data Analytics at University of Pennsylvania in Spring 2020.
