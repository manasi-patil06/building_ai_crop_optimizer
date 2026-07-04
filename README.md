<img width="1408" height="768" alt="system_flowchart" src="https://github.com/user-attachments/assets/872d8f90-4ac1-47b3-a7e2-75ba3508621d" />
<img width="1408" height="768" alt="system_flowchart" src="https://github.com/user-attachments/assets/61ac7cea-c5b8-49ab-827d-b1fb6d3ef5e8" />
<img width="1408" height="768" alt="system_flowchart" src="https://github.com/user-attachments/assets/3509875d-b7cb-4e3d-9a06-9b62f7aecf2b" />
<img width="1408" height="768" alt="system_flowchart" src="https://github.com/user-attachments/assets/c64c15f8-8fdd-4013-b670-65c049344329" />
<img width="1408" height="768" alt="system_flowchart" src="https://github.com/user-attachments/assets/6cb63c21-af97-4df6-89c3-e0933f3ac39b" />
<img width="1408" height="768" alt="system_flowchart" src="https://github.com/user-attachments/assets/5bf26f0e-a628-40cb-8457-7a7ada834823" />
<img width="1408" height="768" alt="9fa120ce-d5be-43dc-a6e2-8ffa73e98697" src="https://github.com/user-attachments/assets/be6b7204-9dac-46f9-b25e-7fd26a973df5" />
# AI Crop Optimizer

This is my final project for the Building AI course!| Created by Manasi Patil.


## Summary
The AI Crop Optimizer is a practical tool designed to help farmers get the best possible crop yields while saving money on resources. Instead of just guessing, the system looks at local environmental data—like soil pH, nutrient levels (NPK), moisture, temperature, and local weather forecasts—to figure out exactly which crop fits the land best and layout a smart schedule for watering and fertilizing.

## Background

* **Wasted Resources:** A lot of farmers end up over-watering or over-fertilizing simply because they don't have exact data. It’s expensive and ends up ruining the soil over time.
  
* **Crop Failures:** Picking the wrong crop for a specific season or soil type can wipe out an entire harvest, which is devastating for smaller farms.
  
* **Unpredictable Weather:** With climate change, old-school farming rules of thumb aren't working like they used to.
  
* **My Motivation:** I wanted to build something that gives mid-to-small-scale farmers easy access to data-driven insights so they can grow sustainably and protect their livelihoods.

## How is it used?
The idea is to have this run as a simple mobile app or web dashboard that a farmer can check before planting season, and then keep using throughout the year.

1. **Inputting Data:** The user inputs their location or syncs the app up with cheap, off-the-shelf IoT soil sensors.
2. **The Crunching:** The system compares these live readings against historical regional data.
3. **The Output:** The farmer gets a clear recommendation on what to plant, plus ongoing alerts on exactly when to irrigate or fertilize based on live weather shifts.

```python code
def main():
    # Quick simulation showing how we match crops to soil data
    soil_data = {'nitrogen': 45, 'phosphorus': 50, 'potassium': 42, 'ph': 6.5, 'rainfall_mm': 120, 'humidity_pct': 75}
    prediction_scores = [0.91, 0.45, 0.78, 0.88] 
    crop_options = ['Tomatoes', 'Potatoes', 'Cotton','Soyabeans']
    
    print("--- Crop Match Results ---")
    for i in range(len(crop_options)):
        print("%s Match Score: %.1f%%" % (crop_options[i], prediction_scores[i] * 100.0))

main()
```



## Data sources and AI methods
The Data: I'm planning to use open-source crop recommendation datasets from Kaggle to train the initial model, along with the OpenWeatherMap API for live updates.

###  AI Approach<img width="1408" height="768" alt="system_flowchart" src="https://github.com/user-attachments/assets/243a8fd4-f15a-4d92-be72-63cef668b236" />


* **Challenges:** Using standard algorithms like Random Forest or XGBoost to handle the multi-class problem of picking the right crop type.

* **Regression:** Simple time-series forecasting to predict soil moisture depletion and schedule irrigation.


## Challenges
* **Sensor Quality:**  The app is only as good as the data coming in. If a farmer uses a faulty sensor or inputs wrong numbers, the recommendations won't be accurate.

* **Regional Differences:** A model trained on soil data from one part of the world might completely fail in another without proper regional tweaking and retraining.

* **Sustainability Risks:** We have to make sure the AI doesn't just chase maximum short-term profit at the expense of stripping the soil of all its nutrients long-term.
<img width="1408" height="768" alt="system_flowchart" src="https://github.com<img width="1408" height="768" alt="system_flowchart" src="https://github.com/user-attachments/assets/5747d76d-8ffd-4ea0-83c8-dc0f2d491475" />
<img width="1408" height="768" alt="system_flowchart" src="https://github.com/user-attachments/assets/e36febc9-4c45-4716-825d-187dcd5749a1" />
<img width="1408" height="768" alt="system_flowchart" src="https://github.com/user-attachments/assets/dd2a3a46-b61b-4edb-9f0f-7b4001f4bb7b" />
<img width="1408" height="768" alt="system_flowchart" src="https://github.com/user-attachments/assets/eae0c1a1-6d58-4303-b120-1ee1c10b7c20" />
/user-attachments/assets/e1df34f7-078f-4c9f-9307-6c1fff9675a0" />


## What's next?
* **Real IoT Testing:** I want to actually hook this up to automated smart valves so the system can water the fields on its own.

* **Disease Detection:** Adding a computer vision feature where you can take a picture of a sick leaf and have the AI diagnose the plant disease.

* **Looking for Help:** I'd love to team up with someone who knows agronomy or hardware development to test this out in a real field.


## Acknowledgments
Shoutout to the Building AI course team from Reaktor and the University of Helsinki for the project framework.
Thanks to the open-source data community for making agricultural datasets accessible.
