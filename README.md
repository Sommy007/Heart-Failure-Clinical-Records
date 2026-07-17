# Project Overview
Heart failure is a chronic cardiovascular condition in which the heart cannot pump blood efficiently to meet the body's needs. It is associated with high hospitalization and mortality rates, making early patient assessment and risk stratification essential for improving clinical outcomes. Healthcare providers routinely collect demographic, clinical, and laboratory data during patient follow-up, but identifying meaningful patterns within this information can be difficult due to the complexity of patient health profiles.

Patients with heart failure often differ significantly in terms of age, medical history, laboratory measurements, and underlying health conditions. Traditional analysis may not easily reveal natural groupings of patients who share similar clinical characteristics. Unsupervised machine learning techniques such as K-Means clustering provide a data-driven approach for discovering these hidden patterns without relying on predefined outcome labels.

This project leverages K-Means clustering to group heart failure patients based on their clinical and laboratory records using the UCI Heart Failure Clinical Records dataset. By identifying distinct patient clusters, the project demonstrates how unsupervised learning can support patient segmentation, reveal similarities among patient profiles, and provide valuable insights that may assist healthcare professionals in personalized treatment planning, patient monitoring, and clinical decision-making.

## Project Goal
This project is aimed at using unsupervised machine learning (K-Means clustering) to identify distinct groups of heart failure patients based on their clinical characteristics and laboratory measurements.

## Features Used
Age (years), Anaemia, Creatinine Phosphokinase (CPK), Diabetes, Ejection Fraction (%), High Blood Pressure, Platelets (kiloplatelets/mL), Serum Creatinine (mg/dL), Serum Sodium (mEq/L), Sex, Smoking Status, Follow-up period (days).

## Data Source
This project uses a publicly available dataset that follows standard academic citation practices.  
Dataset Name: Heart Failure Clinical Records  
Source: UCI Machine Learning Repository  
Authors: Davide Chicco & Giuseppe Jurman  
Year: 2020  DOI / Reference: https://doi.org/10.24432/C5Z89R

## Key Findings
* Smoking shows the clearest difference between male and female patients. Most smokers in the dataset are men, while only a small number of women are smokers. Anaemia, diabetes and high blood pressure are observed in both sexes with fairly similar distributions. Although more men are affected by these conditions in absolute numbners, this is largely because the dataset contains more male than female patients.
* Looking at these 4 conditions (Smoking, anaemia, high blood pressure and diabetes) with respect to the following age groups (<50, 50 - 60, 60 - 70, and 70+ years), older patients tend to carry a heavier health burden overall but not all the time. Anaemia and high blood pressure both climb noticeably as people age, with high blood pressure especially common in the 70+ group. Diabetes stays steady through the 60s but then reduce in the oldest patients, which is probably less about aging being protective and more about the fact that fewer people with both diabetes and heart failure make it to that age. Smoking follows its own pattern too, ticking up through middle age before tapering off later on, likely reflecting people quitting over time or simply not surviving as smokers into old age.


**Cluster 0:** This first group is entirely made up of men, with an average age of about 61. The standout feature here is lifestyle: nearly half of them (47.9 %) are active smokers. On the clinical side, we see some clear signs of heart strain. Their average ejection fraction is on the lower side at 36.55 %, meaning their hearts aren't pumping quite as efficiently as they should. They also show much higher CPK levels (643.40 mcg/L), which is typical for men due to higher average muscle mass, though it can also point to extra cardiac stress. The good news for this group is that they have relatively lower rates of diabetes (35.4 %) and high blood pressure (30.7 %) compared to the other cohort.

**Cluster 1:** This second group is mostly female (98.1 %) and slightly younger, averaging just under 60 years old. In stark contrast to the first group, smoking is incredibly rare here, fewer than 4% of these patients smoke. Their hearts also seem to be holding up a bit better structurally, with a slightly healthier average ejection fraction of 40.83%. However, this group faces a much heavier burden when it comes to metabolic and chronic issues. More than half ($53.3 %) are living with diabetes, and they have significantly higher rates of both high blood pressure (43.0 %) and anemia (49.5 %).








## Tech Stack
Programming Language: Python  
Libraries: NumPy, Pandas, Matplotlib, Seaborn  
Machine Learning: Scikit-Learn  
Model Used: K-Means Clustering  
Environment: Jupyter Notebook

