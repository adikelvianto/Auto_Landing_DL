# Development of Auto Landing Deep Learning Model for Boeing 747 Aircraft

## Executive Summary
This project aim to create **auto landing deep learning model** using TensorFlow by utilizing **"Flight Data Recorcder"** data. 
* First process done is **preprocessing the FDR data** which have a big size each flight and consisting a lot of noise, until we have dataset for training, validation, and testing. The steps done on this process can be seen from [Preprocessing Step.ipynb](https://github.com/adikelvianto/Auto_Landing_DL/blob/main/Preprocessing%20Step.ipynb) 
* Process of developing **elevator** model can be seen here [Build Model - Elevator.ipynb](https://github.com/adikelvianto/Auto_Landing_DL/blob/main/Build%20Model%20-%20Elevator.ipynb)
* Process of developing **throttle** model by set **power lever angle** as targets can be seen here [Build Model - Throttle.ipynb](https://github.com/adikelvianto/Auto_Landing_DL/blob/main/Build%20Model%20-%20Throttle.ipynb)
* The next development of this project is to deploy it to MATLAB/Simulink and X-Plane to see wether this models can do their job as an auto landing control system.

## Dataset
* The dataset that will be processed is **FDR** data containing **300** csv files, where each file consist of nearly **200** variables, when an aircraft depart from certain airport and landing to specific airport which is **Memphis International Airport (MEM), TN, USA**. The aircraft is also limited to **4** engines aircraft (Boeing 747). 

* **Explanation of each variables** can be found in [flight_data_parameter.csv](https://github.com/adikelvianto/Auto_Landing_DL/blob/main/flight_data_parameter.csv)

* **FDR Raw CSV sample files**, consisting **100** flight data can be downloaded through this [link](https://drive.google.com/uc?export=download&id=1qKVe8d0EvFNNv_uxn2vJUbdAbhuTkcG0)

## Result

* [Elevator model](https://github.com/adikelvianto/Auto_Landing_DL/blob/main/model/elevator_model.h5) work **really well** in predicting elevator deflection on landing phase. The predicted and actual trend is very similar, eventhough some of graphs shown the predicted value have **offset** value, but it **never exceed 4 degrees**. Hence, this model could be said well performed. This picture below shown sample of predicted value vs actual test set value for the elevator deflection. 

<p align="center">
<img width="1307" alt="Elevator Comparison" src="https://user-images.githubusercontent.com/92104520/196446972-d92fe034-d835-4562-9993-a1ab18730c35.png">
</p>

* [Throttle model](https://github.com/adikelvianto/Auto_Landing_DL/blob/main/model/throttle_model.h5) also work well in terms of following pilot behavior in deflecting 4 units of power lever angle (Since the aircraft have 4 engines). The problem for this model is the prediction value tends to fluctuate rather than having constant value to create step input graph. The comparison between model prediction and actual power lever angle value can be seen from this picture below. 

<p align="center">
<img width="897" alt="PLA Comparison" src="https://user-images.githubusercontent.com/92104520/196449142-dda478d9-03d1-4ad6-8ee5-dfe12e6aea59.png">
</p>
