# Opioid Abuse Modeling and Analysis
In this project I built, evaluated, and analyzed a variety of classification models to obtain the best performing model for predicting opioid abuse in US citizens. In addition to model evaluation, I determined and quantified the factors that have the greatest impact on likelihood of opioid abuse to propose healthcare policies intended to reduce incidence of opioid abuse.

**Project Report:** [Report](https://github.com/mikecrist/OpioidAbuseAnalysis/blob/main/Report/Report_OpioidAbuse.pdf)

## Credits
This project was created for the Georgia Tech Master of Analytics program.<br>

**Course:** Data Mining and Statistical Learning (ISYE7406)<br>
**Team:** Michael Crist

## Table of Contents
- [Environment Setup](#Environment-Setup)
- [Demo](#Demo)

## Environment Setup
The below instructions are provided to set up your environment within Anaconda.

In Anaconda, create a new environment and then run these commands in the Anaconda Prompt:
```
conda install -c conda-forge fiona=1.8.19
 
conda install -c conda-forge shapely rasterio pyproj pandas jupyterlab geopandas flask

pip install statsmodels
```
These packages are needed to work with Geopandas and using Flask as the framework for the website.

## Demo
![image](https://github.com/mikecrist/AirbnbSafety/assets/31662579/79f6c0f3-c38f-4010-90af-3ea3baa0c6ec)
***User selects city and desired Airbnb features***

![image](https://github.com/mikecrist/AirbnbSafety/assets/31662579/b747e77a-2833-47ad-98e5-730d17ccce22)
***User is provided interactive map displaying heat map of crimes overlayed with Airbnb properties, filtered by the regression model price prediction for the given user inputs.***

![image](https://github.com/mikecrist/AirbnbSafety/assets/31662579/3ef8ecb6-ffc2-4110-a169-264d98ff4719) <br>
***Zoomed image displaying Airbnb property feature data that is displayed when a user clicks on a listing.***
