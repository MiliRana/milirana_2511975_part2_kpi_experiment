# KPI Framework, Business Experiment Analysis & Decision Recommendation

## Business Context

A subscription-based digital product company launched a new onboarding and activation campaign to improve user conversion and early engagement. Users were randomly assigned to one of two groups:

* Control Group: Existing onboarding experience
* Treatment Group: New onboarding campaign experience

The objective of this analysis is to determine whether the treatment should be launched to all users based on experiment results, business metrics, and guardrail metric evaluation.

---

## Business Problem Statement

The company must decide whether the new onboarding campaign should be rolled out to all users.

This decision impacts business leadership, product teams, marketing teams, and future users of the platform.

The primary metric expected to improve is the Paid Conversion Rate. However, before making a launch decision, potential risks such as increased refund requests, higher support ticket volume, lower engagement, or negative segment-level performance must be evaluated.

Evidence required for the recommendation includes experiment results, conversion performance, revenue impact, engagement metrics, guardrail analysis, and hypothesis testing outcomes.

---

## Dataset Description

The dataset contains user-level experiment data including:

* User ID
* Signup Date
* Experiment Group
* Region
* Device Type
* Traffic Source
* Plan Type
* Landing Page Visit Status
* Trial Start Status
* Onboarding Completion Status
* Paid Conversion Status
* Revenue (30 Days)
* Support Tickets (30 Days)
* Refund Requests
* Days to Convert
* Engagement Score

Total Users:

* Control Group: 693
* Treatment Group: 715

---

## North Star Metric

### Paid Conversion Rate

Paid Conversion Rate was selected as the North Star Metric because it directly measures the percentage of users who become paying customers.

### Why This Is The Main Success Metric

The objective of the onboarding campaign is to increase user activation and drive subscription purchases. Paid Conversion Rate directly measures business success and revenue generation.

### Why Other Metrics Are Supporting Metrics

Metrics such as Landing Page Visit Rate, Trial Start Rate, Onboarding Completion Rate, Engagement Score, and Revenue Per User are important indicators of user behavior but represent intermediate stages of the customer journey.

### Connection To Business Growth

An increase in Paid Conversion Rate leads to more paying customers, increased revenue, and improved business profitability.

### Risk Of Optimizing Blindly

Focusing only on Paid Conversion Rate could ignore negative outcomes such as increased refund requests, higher support ticket rates, or poor user experience. Therefore, guardrail metrics must also be monitored.

---

## KPI Tree Summary

North Star Metric:

* Paid Conversion Rate

Primary Drivers:

1. User Acquisition

   * Landing Page Visit Rate
   * Trial Start Rate

2. Onboarding Effectiveness

   * Onboarding Completion Rate
   * Days To Convert

3. User Engagement

   * Engagement Score
   * Revenue Per User

Guardrail Metrics:

* Refund Rate
* Support Ticket Rate
* Segment-Level Decline

---

## Data Cleaning And Preparation

The following data quality checks were performed:

### Missing Values

Missing values were identified in:

* Device Type
* Traffic Source
* Engagement Score

These missing values were documented and retained for analysis where appropriate.

### Group Counts

Control and Treatment group distributions were verified.

### Duplicate User IDs

Duplicate User IDs were checked and no material issues were identified.

### Invalid Binary Values

Binary fields were validated to ensure values were limited to 0 and 1.

### Revenue Outliers

Revenue values were reviewed for unusually large observations.

### Segment Distribution

Region, Device Type, Traffic Source, and Plan Type distributions were reviewed across experiment groups.

---

## Experiment Analysis Approach

The analysis compared Control and Treatment groups across key business metrics:

* User Count
* Landing Page Visit Rate
* Trial Start Rate
* Onboarding Completion Rate
* Paid Conversion Rate
* Average Revenue Per User
* Average Revenue Per Converted User
* Refund Rate
* Support Ticket Rate
* Average Engagement Score
* Average Days To Convert

Additional segment analysis was performed by:

* Region
* Device Type
* Traffic Source

---

## Hypothesis Test Summary

### Metric Tested

Paid Conversion Rate

### Null Hypothesis (H₀)

The treatment onboarding campaign does not improve Paid Conversion Rate compared to the control group.

### Alternative Hypothesis (H₁)

The treatment onboarding campaign improves Paid Conversion Rate compared to the control group.

### Test Type

One-tailed hypothesis test

### Significance Level

α = 0.05

### Results

| Metric               | Control | Treatment |
| -------------------- | ------- | --------- |
| Users                | 693     | 715       |
| Conversions          | 22      | 50        |
| Paid Conversion Rate | 3.17%   | 6.99%     |

The treatment group achieved a substantially higher Paid Conversion Rate than the control group.

---

## Guardrail Metrics Considered

### Refund Rate

* Control: 0.00%
* Treatment: 0.42%

A small increase in refund requests was observed.

### Support Ticket Rate

* Control: 14.72%
* Treatment: 24.76%

Support ticket volume increased in the treatment group and should be monitored.

### Average Days To Convert

* Control: 8.86
* Treatment: 6.40

Users converted more quickly under the treatment experience.

### Average Engagement Score

* Control: 57.03
* Treatment: 62.93

User engagement improved under the treatment experience.

---

## Final Recommendation

### Recommendation: Launch With Monitoring

The treatment onboarding campaign increased Paid Conversion Rate from 3.17% to 6.99%, improved engagement scores, and reduced the average time required for users to convert.

Although refund requests and support ticket rates increased, the overall business impact remains positive.

The treatment should be launched while continuing to monitor refund rates and support ticket volume after deployment.

---

## Assumptions And Limitations

* Missing values were retained where appropriate.
* Analysis was limited to the available experiment period.
* Results are based on the provided dataset and may not fully represent future user behavior.
* Long-term retention effects were not measured.

---

## Screenshots Included

* summary_metrics.png
* hypothesis_test_output.png
* kpi_tree_preview.png
