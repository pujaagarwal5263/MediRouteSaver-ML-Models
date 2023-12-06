# Mental-Health-Prediction
> Route and Vehicle Prediction with Machine-Learning.

# How to run the app?
Setup your virtual environment and run the following command:
```
python app.py
```

# What is the payload to be sent?
```
{
    "features": [[1,1087],[56,789]]
}
```
<hr/>

# Feature Description for Route Prediction
```
{
    "features": [[stop_id,time],[stop_id,time]]
}
```
<small>The stop IDs are unique list of postalCodes from 1-78 and time is formatted as 17:35 -> 1035 using simple calculations.</small>

<p>Output will be 0,1,2,3 signifying RTE01, RTE02,...</p>

# URL to be hit on for route Prediction
Once the app is up and running the hit this endpoint with above payload: <strong>http://127.0.0.1:5000/predict-route</strong>

<hr/>

# Feature Description for Vehicle Prediction
```
{
    "features": [[task_id,stop_id],[task_id,stop_id]]
}
```
<small>The task IDs are unique list of tasks from 0-14 and stop_id is list of PostalCodes from 1-78.</small>

<p>Output will be 0,1,2 signifying Veh_01, Veh_02,...</p>

# URL to be hit on for vehicle Prediction
Once the app is up and running the hit this endpoint with above payload: <strong>http://127.0.0.1:5000/predict-vehicle</strong>
