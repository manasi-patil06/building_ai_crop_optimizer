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

```python
def main():
    # Quick simulation showing how we match crops to soil data
    soil_data = {'nitrogen': 45, 'phosphorus': 50, 'potassium': 42, 'ph': 6.5, 'rainfall_mm': 120, 'humidity_pct': 75}
    prediction_scores = [0.91, 0.45, 0.78, 0.88] 
    crop_options = ['Tomatoes', 'Potatoes', 'Cotton','Soyabeans']
    
    print("--- Crop Match Results ---")
    for i in range(len(crop_options)):
        print("%s Match Score: %.1f%%" % (crop_options[i], prediction_scores[i] * 100.0))

main()

## Data sources and AI methods
The Data: I'm planning to use open-source crop recommendation datasets from Kaggle to train the initial model, along with the OpenWeatherMap API for live updates.

#  AI Approach-

* **Classification:** Using standard algorithms like Random Forest or XGBoost to handle the multi-class problem of picking the right crop type.

* **Regression:** Simple time-series forecasting to predict soil moisture depletion and schedule irrigation.

## Challenges
* **Sensor Quality:**  The app is only as good as the data coming in. If a farmer uses a faulty sensor or inputs wrong numbers, the recommendations won't be accurate.

* **Regional Differences:** A model trained on soil data from one part of the world might completely fail in another without proper regional tweaking and retraining.

* **Sustainability Risks:** We have to make sure the AI doesn't just chase maximum short-term profit at the expense of stripping the soil of all its nutrients long-term.

## What's next?
* **Real IoT Testing:** I want to actually hook this up to automated smart valves so the system can water the fields on its own.

* **Disease Detection:** Adding a computer vision feature where you can take a picture of a sick leaf and have the AI diagnose the plant disease.

* **Looking for Help:** I'd love to team up with someone who knows agronomy or hardware development to test this out in a real field.

## Acknowledgments
Shoutout to the Building AI course team from Reaktor and the University of Helsinki for the project framework.
Thanks to the open-source data community for making agricultural datasets accessible.
