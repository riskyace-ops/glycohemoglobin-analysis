INTRODUCTION

As a type one diabetic of fifteen years I've taken a great interest in exploring my disease to the fullest extent I possible can.
I've taken it upon myself to collect as much data as I possibly can that'd gear me towards polishing my understanding further - more specifically an understanding
of glycohemoglobin levels(HbA1c) and its respective connection with several physiological & behavioral variables: Systolic/Diastolic BP, BPM, HDL Cholesterol, Total Cholesterol, Weight, Height, Depression Screening, Smoking Habits, 
Alcohol Consumption Habits. This exploratory analysis project collects its 10,000+ lines of indivisual data from the NHANES organization. However, in my discovery when merging the several data tables together in union with
each participant's unique ID, I've identified only ~1,000+ viable participants. This will indefinitely impact the strength of the findings of this project but nonetheless
still provide some level of insight into the connection between HbA1c & the aforementioned variables.

==================================================================================================================================================

SECTION #1
Preliminary Measures

#1 All data files collected pertaining to biomarker data & questionnaire data are collected with exact
corresponding year.
#2 All missing rows for the target variable(HbA1c) are deleted
#3 All participants are ADULTS
#4 Methodology of imputing missing data is contingent on whether it's continious or categorical & if it's an approximately normal distribution

    Height, Weight missing values are replaced with mean value
    Systolic, Diastolic, Pulse, Cholesterol & HDL Cholesterol are replaced with median values

    Categorical variables including: depression, smoking, and alcohol questionnaire missing values are imputed with value of 0 and put into seperate category.
    No analysis is performed on missing values

#5 All values are converted into an int64 Dtype
#6 Categorical variables are illustrated in pie graphs, whereas continious variables are illustrated in histograms, boxplots & scatterplots.

==================================================================================================================================================

SECTION #2
Univariate analysis
Categorical

(1) Alcohol questionnaire
    97% of sample have consumed alcoholic beverages in lifetime & 3% have not. (1042 > 32)

(2) Smoking questionnaire
    57.1% of sample not consumed tobacco, 33.9% consume tobacco regularly & 9% consume tobacco intermittently. (613 > 364 > 97)

(3) Depression questionnaire
    50.9% experience depression several days, 27.8% never experience depression, 11.9% experience depression more than 1/2 of days & 9.3% experience depression nearly every day. (547 > 299 > 128 > 100)


Disclaimer/Authors Note: All three categorical variables do not provide a conclusive understanding of participant smoking, alocohol consumption & depressive behaviors because of insufficient data.
We can determine to some degree our particpants have a higher likelihood of consuming alcohol, experiencing depressive tendencies & not regular consumers of tobacco products through means of smoking. 

==================================================================================================================================================

SECTION #3
Univariate analysis
Continious 

(1) Systolic Blood Pressure
Histogram depicts a unimodal, approximately normal distribution with outliers exceeding the 160 systolic value, exceeding beyond into hypertensive readings.
Sample participants have a mean systolic reading of 124 with a standard deviation of 19 indicating moderate variability.
Majority of sample participants(first, second, & third quartile) have a relatively healthy/mildly elevated systolic blood pressure reading 

(2) Diastolic Blood Pressure
Histogram depicts a unimodal, stronger approximate normal distribution with outliers exceeding the 110 value.
Sample participants havee a mean diastolic reading of 76 & a standard deviation of 12 indicating moderate variability
Majority of sample participants(first, second & third quartile) also have a relatively healthy diastolic blood pressure reading which is to be expected.

Disclaimer/Authors Note: Systolic & Diastolic readings aren't entirely accurate because of several confounding variables including but not limited to; accuracy of device, pre-existing medical conditions,
genetic predispositions, anxiety, etc. We can determine however that the majority of participants fall within the normal or mildly high blood presure bracket. 


(3) Pulse Rate
Pulse rate of distribution is unimodal & approximately normal with a mean of 73 & standard deviation of 18. 
Most participants fall within 60 & 90 beats per minute (BPM) with observed outliers in the bradycardic (< 60 BPM) & tachycardic (> 100) ranges

Disclaimer/Authors Note: BPM readings aren't also entirely accurate readings and aren't strong indicators of cardiac health of participants because of the aforementioned confounding variables. 
We can determine based off the data that majority of participants present with healthy BPM readings.

(4) Height & Weight

Both Height & Weight histograms depict an approximately normal, bell-curve shaped distribution. Weight histogram is slightly skewed right with several outliers weighing < 130 kilograms. Minimal variability 
can be observed in the height distribution with few outliers < 150cm & >185cm. Most participants land within the 50-100kg weight range & 150-185cm height range.

Disclaimer/Authors Note: We can confidently determine the vast majority of the participants lie within the national average in height & weight.

(5) Total Cholesterol (HDL + LDL - Triglycerides/5)

Distribution is unimodal & approximately normal and skewed right with several outliers exceeding the 250mg/dL value. Participants on average have a value of ~186mg/dL.

Disclaimer/Authors Note: A higher total cholesterol value is indicative of an unhealthy dietery lifestyle & poor lifestyle habits. This value is contingent on several confounding variables including but not
limited to genetic predispositions & environment. A healthy total cholesterol range is below 200mg/dL and values 200-239mg/dL incdicating borderline high. Approximately half of the participants rest on the borderline
high & high values. 

(6) HDL Cholesterol

Distribution is skewed right with high variability. Several outliers can be observed at values exceeding 70mg/dL. Average HDL value for all participants is ~52mg/dL.

Disclaimer/Authors Note: HDL values below 40mg/dL & above 80mg/dL indicate poor dietery lifestyles. We can determine the vast majority of participants present within the healthy normal HDL range for adults.

(7) HbA1c (Target Variable)

Distribution is unimodal, and skewed right with several outliers exceeding values of 7%. Mean HbA1c for participants is ~6%

Disclaimer/Authors Note: We can confidently determine more than 50% of participants present with a healthy HbA1c range of between (5% - 6%).

==================================================================================================================================================

SECTION (#4)
Bivariate Analysis (Continious Variables Comparison with Target Variable(HbA1c))
PEARSON CALCULATIONS

(1) HbA1c vs. Systolic BP 
A positive but weak correlation can be observed. The calculated Pearson value is 0.124.

(2) HbA1c vs. Diastolic BP
A positive signifanctly but weak correlation can be observed. The calculated Pearson value is 0.0604.

(3) HbA1c vs. Pulse
A positive but weak correlation can be observed. The calculated Pearson value is 0.1562.

(4) HbA1c vs. Weight
A positive but weak correlation can be observed. The calculated Pearson value is 0.145.

(5) HbA1c vs. Height
A negative and signifanctly weak correlation can be observed. The calculated Pearson value is -0.0256.

(6) HbA1c vs. Total Cholesterol
A negative and signifanctly weak correlation can be observed. The calculated Pearson value is -0.01.

(7) HbA1c vs. HDL Cholesterol
A negative and weak correlation can be observed. The calculated Pearson value is -0.172.

==================================================================================================================================================
SECTION (#5)
Bivariate Analysis (Categorical Variables Comparison with Target Variable(HbA1c))
ANOVA CALCULATIONS

(1) HbA1c vs. Alcohol questionnaire group
There is a statistically signifanct association between alcohol consumption habits & HbA1c values. The calculated ANOVA f-statistic is 16 with a p-value of >0.005

(2) HbA1c vs. Depression questionnaire group
There is no statistical signifance and weak association between depression & HbA1c values. The calculated ANOVA f-statistic value is 0.8371 with a p-value of 0.43.

(3) HbA1c vs. Smoking questionnaire group
There is no statistical signifance and weak association between smoking & HbA1c values. The calculated ANOVA f-statistic value is 0.2431 with a p-value of 0.78.

==================================================================================================================================================
SECTION (#6)
Conclusion

In the bivariate analysis section, I've identified a common theme between all continious variables. Blood pressure, BPM, height, weight, and cholesterol value measures 
indicate a consistently weak yet positive correlation with HbA1c. There is no statistical signifance observed in the connection between the physiological variables & HbA1c.

Categorical variable connections, similar to continious, also reflect a consistent lack of statistical signifance w/ correlations in HbA1c & smoking & depression groups.
It is noted however though that HbA1c levels in participants who consume alcohol exhibit a higher HbA1c reading compared to those participants who did not consume alcohol. 

Given the modest sample size (~1000), and the presence of several confounding variables that impede findings; medications, dietery lifestyle, and genetic predispositions, 
it's difficult for me to report any conclusive findings. A more comprehensive collection of data geared specifically towards HbA1c research is needed in order to better understand
the determinants of HbA1c in more larger and diverse populations. 

Thank you to whomever took the time out of their day to read through my project!
