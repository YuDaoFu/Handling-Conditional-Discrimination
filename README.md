# Handling-Conditional-Discrimination

**Machine Learning Fairness**

The idea is based on the paper Handling Conditional Discrimination

## Dataset 
COMPAS dataset (Correctional Offender Management Profiling for
Alternative Sanctions)

A database containing the criminal history, jail and prison time,
demographics, and COMPAS risk scores for defendants from Broward
County from 2013 and 2014. The ground truth on whether or not
these individuals actually recidivated within two years after the
screening is also being collected.
Recidivism is defined as a new arrest within two years.
ProPublica’s analysis shows that the COMPAS risk scores are
discriminatory against race and gender.

## Objects:

Dataset:
- COMPAS but restricted to a subset that contains only two race groups
(Caucasian and African-American)

Binary class label (y):
- Whether or not the defendant recidivated within two years
(“two_year_recid” column in “compas-scores-two-years.csv”)

Binary sensitive attribute:
- race (Caucasian: 1, African-American: 0)

Evaluation Metrics:
- Accuracy; and
- Calibration: Accuracy difference between two race groups.

Data splitting:
- training : testing = 7 : 3

## Approaches

**Local Massaging**
- The local massaging for every partition in the training data
induced by the explanatory attribute will modify the values of
labels

**Local Preferential Sampling**
  - The preferential sampling technique does not modify the
  training instances or labels, instead it modifies the composition
  of the training set.

## Conclusion 
The accuracy and Calibration slightly decreased after modified algorithms but in return of a good elimination towards bad discrimination. After all we conclude that the trade between accuracy and discrimation is worth the shot.
