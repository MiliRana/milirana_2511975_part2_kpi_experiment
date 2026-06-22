# Hypothesis Test Notes

## Metric Being Tested

Paid Conversion Rate

## Reason for Choosing This Metric

The objective of the onboarding campaign is to increase the number of users who become paying customers. Paid Conversion Rate directly measures the effectiveness of the campaign in driving business growth and revenue.

## Null Hypothesis (H₀)

The treatment onboarding campaign does not improve the Paid Conversion Rate compared to the control group.

Treatment Conversion Rate ≤ Control Conversion Rate

## Alternative Hypothesis (H₁)

The treatment onboarding campaign improves the Paid Conversion Rate compared to the control group.

Treatment Conversion Rate > Control Conversion Rate

## Test Type

One-tailed hypothesis test

## Significance Level

α = 0.05

## Interpretation Logic

* If p-value < 0.05, reject the null hypothesis and conclude that the treatment significantly improves Paid Conversion Rate.
* If p-value ≥ 0.05, fail to reject the null hypothesis and conclude that there is insufficient evidence that the treatment improves Paid Conversion Rate.

## Business Decision Connection

The result of this test will be used to determine whether the new onboarding campaign should be launched to all users. A statistically significant improvement in Paid Conversion Rate would support a launch recommendation, subject to guardrail metric evaluation.

## Test Inputs

Control Users: 693

Treatment Users: 715

Control Conversions: 22

Treatment Conversions: 50

Control Conversion Rate: 3.17%

Treatment Conversion Rate: 6.99%

## Results

The Treatment group achieved a Paid Conversion Rate of 6.99% compared to 3.17% for the Control group.

This represents an increase of approximately 3.82 percentage points.

## Business Interpretation

The Treatment onboarding experience substantially improved Paid Conversion Rate compared to the Control experience.

The experiment provides evidence that the new onboarding campaign is more effective at converting users into paying customers.

## Decision Rule

If the treatment group demonstrates a statistically and practically meaningful improvement in Paid Conversion Rate without causing unacceptable deterioration in guardrail metrics, the treatment should be considered for launch.
