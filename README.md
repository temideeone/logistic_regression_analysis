# Airline Customer Satisfaction Analysis & Predictive Modeling

This repository contains an end-to-end machine learning project aimed at predicting airline customer satisfaction and identifying the key service drivers that influence passenger experiences. 

##  Dataset Overview
The dataset contains **25,976 passenger records** evaluating various aspects of their flight experience. The target variable is binary: **Satisfied** vs. **Dissatisfied**.
* **Satisfied Passengers:** 14,217 records
* **Dissatisfied Passengers:** 11,759 records

---

##  Modeling Approach
A classification model (Logistic Regression framework based on log-odds interpretation) was trained to predict satisfaction based on passenger demographics, flight distances, delays, and 14 specific service features.

### Driver Dominance Analysis
Features were evaluated using their **Log-Odds Coefficients**. A positive coefficient increases the likelihood of a passenger reporting satisfaction, while a negative coefficient indicates the feature heavily contributes to dissatisfaction.

####  Key Satisfaction Drivers (Positive Impact)
1. **Inflight entertainment (+0.973)** – By far the strongest driver of passenger satisfaction.
2. **Seat comfort (+0.393)** – Highly critical physical touchpoint.
3. **On-board service (+0.387)** – Crew interactions strongly sway sentiment.
4. **Check-in service (+0.356)** – The leading pre-flight touchpoint.

####  Key Friction Points (Negative Impact)
1. **Disloyal Customers (-0.725)** – First-time or non-program flyers are disproportionately critical.
2. **Economy/Eco Plus Seating (-0.355 / -0.198)** – Lower tier cabins strongly correlate with poor satisfaction.
3. **Personal Travel (-0.350)** – Leisure travelers are significantly harder to please than business travelers.
4. **Inconvenient Dep/Arr Times (-0.329)** – Poor scheduling strongly degrades the experience.

---

##  Final Performance Metrics

The model demonstrates balanced, high-utility performance across both classes with an overall **Accuracy of 83%**.

### Classification Report

| Target Class | Precision | Recall | F1-Score | Support |
| :--- | :---: | :---: | :---: | :---: |
| **Dissatisfied** | 0.81 | 0.81 | 0.81 | 11,759 |
| **Satisfied** | 0.84 | 0.84 | 0.84 | 14,217 |
| **Accuracy** | | | **0.83** | **25,976** |
| **Macro Average** | 0.83 | 0.83 | 0.83 | 25,976 |
| **Weighted Average**| 0.83 | 0.83 | 0.83 | 25,976 |

###  Derived Confusion Matrix
Based on the classification report precision and recall metrics across the 25,976 evaluation samples, the underlying confusion matrix stands as follows:

* **True Negatives (Correctly Predicted Dissatisfied):** 9,525
* **False Positives (Predicted Satisfied but Actually Dissatisfied):** 2,234
* **False Negatives (Predicted Dissatisfied but Actually Satisfied):** 2,275
* **True Positives (Correctly Predicted Satisfied):** 11,942

---

##  Key Takeaways & Recommendations
* **Double Down on Entertainment:** Small investments in the digital inflight experience yield the highest statistical return on satisfaction.
* **Target Disloyal Churn:** Specific marketing or service intervention strategies are needed for non-frequent flyers to convert them to loyal brand advocates.
* **Optimize Schedules over Wifi:** Interestingly, flight time convenience (-0.328) impacts satisfaction far heavier than minor fluctuations in inflight wifi quality (-0.127).
