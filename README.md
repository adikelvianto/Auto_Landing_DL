# Development of Auto Landing Deep Learning Model for Boeing 747 Aircraft

## Executive Summary
This project aim to create **auto landing deep learning model** using TensorFlow by utilizing **"Flight Data Recorcder"** data. 
* First process done is **preprocessing the FDR data** which have a big size each flight and consisting a lot of noise, until we have dataset for training, validation, and testing. The steps done on this process can be seen from [Preprocessing Step.ipynb](https://github.com/adikelvianto/Auto_Landing_DL/blob/main/Preprocessing%20Step.ipynb) 
* Process of developing **elevator** model can be seen here [Build Model - Elevator.ipynb](https://github.com/adikelvianto/Auto_Landing_DL/blob/main/Build%20Model%20-%20Elevator.ipynb)
* Process of developing **throttle** model by set **power lever angle** as targets can be seen here [Build Model - Throttle.ipynb](https://github.com/adikelvianto/Auto_Landing_DL/blob/main/Build%20Model%20-%20Throttle.ipynb)

## Dataset
* The dataset that will be processed is **FDR** data containing **300** csv files, where each file consist of nearly **200** variables, when an aircraft depart from certain airport and landing to specific airport which is **Memphis International Airport (MEM), TN, USA**. The aircraft is also limited to **4** engines aircraft (Boeing 747). 

* **Explanation of each variables** can be found in [flight_data_parameter.csv](https://github.com/adikelvianto/Auto_Landing_DL/blob/main/flight_data_parameter.csv)

* **FDR Raw CSV sample files**, consisting **100** flight data can be downloaded through this [link](https://drive.google.com/uc?export=download&id=1qKVe8d0EvFNNv_uxn2vJUbdAbhuTkcG0)
