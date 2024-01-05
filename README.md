# Opioid Abuse Modeling and Analysis
In this project I built, evaluated, and analyzed a variety of classification models to obtain the best performing model for predicting opioid abuse in US citizens. In addition to model evaluation, I determined and quantified the factors that have the greatest impact on likelihood of opioid abuse to propose healthcare policies intended to reduce incidence of opioid abuse.

**Project Report:** [Report](https://github.com/mikecrist/OpioidAbuseAnalysis/blob/main/Report/Report_OpioidAbuse.pdf)

## Credits
This project was created for the Georgia Tech Master of Analytics program.<br>

**Course:** Data Mining and Statistical Learning (ISYE7406)<br>
**Team:** Michael Crist

## Table of Contents
- [Abstract](#Abstract)
- [Dataset](#Dataset)
- [Citations](#Citations)

## Abstract
Complete report [here](https://github.com/mikecrist/OpioidAbuseAnalysis/blob/main/Report/Report_OpioidAbuse.pdf).

In this report I build, evaluate, and analyze a variety of classification models to obtain the best performing model for predicting prescription painkiller misuse in US citizens. In addition to model evaluation, I determine and quantify the factors that have the greatest impact on the odds of painkiller misuse.

The dataset used in this report was obtained from the National Survey on Drug Use and Health 2015-2017. The models evaluated in the report include Logistic Regression, Linear Discriminant Analysis (LDA), Quadratic Discriminant Analysis (QDA), Naïve Bayes, K-Nearest Neighbors (KNN), Random Forest, and Boosting. KNN was determined to be the best performing model, predicting painkiller misuse with 99.13% accuracy. The five factors with the greatest impact on odds of painkiller misuse were determined to be age, marital status, hallucinogen use, amphetamine use, and heroin use.

Opioid abuse/misuse results in $35 billion in healthcare costs each year in the US (“The High Price…”, 2021). In the US alone, opioid-involved overdoses have nearly quadrupled from 21,089 in 2010 to 80,411 in 2021 (“Drug Overdose Death Rates”, 2023). This is a problem that has plagued the US healthcare system for decades, and has negatively impacted millions of lives. This report aims to accomplish two goals:

- Build a variety of classification models to predict whether or not a person will misuse painkillers, and determine the best performing model.
- Determine the factors that most impact the odds of painkiller misuse, and quantify those factors’ impact.

The motivation for this project is to provide the necessary analytics to implement healthcare / political policy aimed at reducing prescription painkiller misuse.

## Dataset
The dataset I used for this project can be found [here](https://github.com/mikecrist/OpioidAbuseAnalysis/blob/main/Data/prlmis-data-full.csv/prlmis-data-full.csv).

The dataset was obtained from the National Survey on Drug Use and Health 2015-2017, and published on Kaggle. This dataset contains 170317 rows and 21 columns. 18 of the columns are predictor variables, and 3 are potential response variables (“misused prescription medication”, “abused prescription medication”, and “misused/abused minimum prescription medication”). For the intent of my project, I will use “misused prescription medication” as the response variable. This is a binary variable, labeled “PRLMISEVR”, with a 0 indicating no painkiller misuse and a 1 indicating painkiller misuse.

There are a variety of predictors in the dataset, both categorical and numeric. Examples of some of the predictor variables are age, marital status, education level, employment status, etc. The response variable, PLMISEVR, is a binary variable.

## Citations
“Drug Overdose Death Rates.” *National Institutes of Health*, U.S. Department of Health and Human Services, 9 Feb. 2023, https://nida.nih.gov/research-topics/trends-statistics/overdosedeathrates#:~:text=Opioid%2Dinvolved%20overdose%20deaths%20rose,with%2080%2C411%20reported%20overdose%20deaths.

“Opioid Data Analysis and Resources.” *Centers for Disease Control and Prevention*, Centers for Disease Control and Prevention, 1 June 2022, https://www.cdc.gov/opioids/data/analysis-resources.html.

“The High Price of the Opioid Crisis, 2021.” *The Pew Charitable Trusts*, The Pew Charitable Trusts, 27 Aug. 2021, https://www.pewtrusts.org/en/research-and-analysis/data-visualizations/2021/the-high-price-of-the-opioid-crisis-2021.
