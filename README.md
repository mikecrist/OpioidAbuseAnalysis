# Opioid Abuse Modeling and Analysis
In this project I built, evaluated, and analyzed a variety of classification models to obtain the best performing model for predicting opioid abuse in US citizens. In addition to model evaluation, I determined and quantified the factors that have the greatest impact on likelihood of opioid abuse to propose healthcare policies intended to reduce incidence of opioid abuse.

**Project Report:** [Report](https://github.com/mikecrist/OpioidAbuseAnalysis/blob/main/Report/Report_OpioidAbuse.pdf)

## Credits
This project was created for the Georgia Tech Master of Analytics program.<br>

**Course:** Data Mining and Statistical Learning (ISYE7406)<br>
**Team:** Michael Crist

## Table of Contents
- [Abstract](#Abstract)
- [Conclusions](#Conclusions)
- [Dataset](#Dataset)
- [Citations](#Citations)

## Abstract
Complete report [here](https://github.com/mikecrist/OpioidAbuseAnalysis/blob/main/Report/Report_OpioidAbuse.pdf).

In this project I built, evaluated, and analyzed a variety of classification models to obtain the best performing model for predicting opioid abuse in US citizens. In addition to model evaluation, I determined and quantified the factors that have the greatest impact on likelihood of opioid abuse to propose healthcare policies intended to reduce incidence of opioid abuse.

The dataset used in this report was obtained from the National Survey on Drug Use and Health 2015-2017. The models evaluated in the report include Logistic Regression, Linear Discriminant Analysis (LDA), Quadratic Discriminant Analysis (QDA), Naïve Bayes, K-Nearest Neighbors (KNN), Random Forest, and Boosting. KNN was determined to be the best performing model, predicting opioid abuse with 99.13% accuracy. The five factors with the greatest impact on odds of opioid abuse were age, marital status, hallucinogen use, amphetamine use, and heroin use.

Opioid abuse/misuse results in $35 billion in healthcare costs each year in the US (“The High Price…”, 2021). In the US alone, opioid-involved overdoses have nearly quadrupled from 21,089 in 2010 to 80,411 in 2021 (“Drug Overdose Death Rates”, 2023). This is a problem that has plagued the US healthcare system for decades, and has negatively impacted millions of lives. This report aims to accomplish two goals:

- Build a variety of classification models to predict whether or not a person will misuse opioids, and determine the best performing model.
- Determine the factors that most impact the odds of opioid misuse, and quantify those factors’ impact.

The motivation for this project is to provide the necessary analytics to implement healthcare / political policy aimed at reducing opioid misuse.

## Conclusions
![image](https://github.com/mikecrist/OpioidAbuseAnalysis/assets/31662579/af22390d-7379-42ad-9f78-8ebcc47fd2c3)
<p align="center">
Results Summary
</p>

The best performing model was the KNN model, which obtained an accuracy of 99.13%. The optimal k-value was determined by evaluating the cross-validation error for many values of k. This model should be used to predict opioid misuse in individuals so that healthcare professionals may take the necessary steps to avoid dangerous outcomes.

The KNN model was clearly the best performing model because it performed best on all metrics. However, selecting the second and third best models becomes more interesting, because accuracy / total error is not necessarily the most important metric to use for evaluation. The objective of the model is to predict whether an individual will misuse opioids, which is very dangerous for the individual and can result in overdose or death. For this reason, sensitivity is the most important metric, because this is the “true positive rate”, meaning the percentage of cases of opioid misuse that were correctly classified. It is more dangerous for the model to miss a case of opioid misuse (type II error) than it is for the model to incorrectly predict opioid misuse (type I error). The three best-performing models, ranked by sensitivity, are:
1. KNN (sensitivity 94.97%)
2. Naïve Baes (sensitivity 48.30%)
3. QDA (sensitivity 46.31%)

In addition to evaluating model performance, I also evaluated factor importance to determine the factors that had the greatest impact on the odds of opioid misuse. The five factors that most impact odds of opioid misuse are summarized below:
1. **Age:** We expect an 89-92% decrease in odds of opioid misuse if a person’s age is >= 50 (versus baseline of age 12-17), holding all other factors constant.
2. **Marital Status:** We expect a 35-48% decrease in odds of opioid misuse if a person is unmarried (versus baseline of divorced), holding all other factors constant.
3. **Hallucinogen Use:** We expect a 58-64% increase in odds of opioid misuse for each unit increase in hallucinogen use on the Likert scale, holding all other factors constant.
4. **Amphetamine Use:** We expect a 47-56% increase in odds of opioid misuse for each unit increase in amphetamine use on the Likert scale, holding all other factors constant.
5. **Ever Used Heroin:** We expect a 45-102% increase in odds of opioid misuse if a person has ever used heroin, holding all other factors constant.

***Policy Proposals***

Based upon the results of this project, the policy actions below would reduce opioid misuse in the US:
1. Educate students on the dangers of opioid misuse, beginning in elementary school. Continue education throughout high school.
    - Opioid misuse is more likely in younger age categories, so education must start early.
2. Incentive programs to reduce use of all illicit drugs.
    - Use of illicit drugs is a clear risk factor for opioid misuse. Offer incentive programs to encourage drug users to reduce or eliminate illicit drug use.
3. Offer marriage counseling to reduce divorce rate in the US.
    - Divorce is a clear risk factor for opioid misuse. Cultivating healthy marital relationships would reduce risk of opioid misuse.
4. Regular screening of patients.
    - Healthcare providers should request patients to complete the survey used to obtain the dataset for this project. Survey results can be entered into the KNN model to predict whether the patient will misuse opioids. If the model predicts opioid misuse, healthcare providers may decide against opioid prescription, or further educate the patient on responsible opioid use.


## Dataset
The dataset I used for this project can be found [here](https://github.com/mikecrist/OpioidAbuseAnalysis/blob/main/Data/prlmis-data-full.csv/prlmis-data-full.csv).

The dataset was obtained from the National Survey on Drug Use and Health 2015-2017, and published on Kaggle. This dataset contains 170317 rows and 21 columns. 18 of the columns are predictor variables, and 3 are potential response variables (“misused prescription medication”, “abused prescription medication”, and “misused/abused minimum prescription medication”). For the intent of my project, I will use “misused prescription medication” as the response variable. This is a binary variable, labeled “PRLMISEVR”, with a 0 indicating no opioid misuse and a 1 indicating opioid misuse.

There are a variety of predictors in the dataset, both categorical and numeric. Examples of some of the predictor variables are age, marital status, education level, employment status, etc. The response variable, PLMISEVR, is a binary variable.

## Citations
“Drug Overdose Death Rates.” *National Institutes of Health*, U.S. Department of Health and Human Services, 9 Feb. 2023, https://nida.nih.gov/research-topics/trends-statistics/overdosedeathrates#:~:text=Opioid%2Dinvolved%20overdose%20deaths%20rose,with%2080%2C411%20reported%20overdose%20deaths.

“Opioid Data Analysis and Resources.” *Centers for Disease Control and Prevention*, Centers for Disease Control and Prevention, 1 June 2022, https://www.cdc.gov/opioids/data/analysis-resources.html.

“The High Price of the Opioid Crisis, 2021.” *The Pew Charitable Trusts*, The Pew Charitable Trusts, 27 Aug. 2021, https://www.pewtrusts.org/en/research-and-analysis/data-visualizations/2021/the-high-price-of-the-opioid-crisis-2021.
