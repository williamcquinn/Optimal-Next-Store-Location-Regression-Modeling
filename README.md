# Optimal-Next-Store-Location-Regression-Modeling
Croq'Pain: Building, evaluating, and analyzing the results of regression models to find the most optimal next store locations.

**Croq’Pain**

CroqPain.rds is the full data set that includes all stores as well as a set of 10 potential new store locations. Below, we provide some extra guidance as you work through each part of the case.

Before you start …
There is a problem in the data file CroqPain.rds (i.e., the data needs some ‘cleaning’). Find the issue and propose a fix before you continue with the analysis.

Hint: Check data histograms
Post questions on Piazza as needed. Discuss your “fix” with the TAs during a work session or post your proposed data “fix” on Piazza as a private post. Review the help file for Data > Transform to get some “inspiration” on ways to detect issues and clean the data. Apply your fix and “store” it into a dataset called CroqPainFix.

**Part (a)**

Visualize the data: examine histograms and scatterplots. Add line and loess to the scatter plots in turn. Also look at correlations between variables and try to identify sources of concern. Pay particular attention to the correlation for total and P15 through P55. Do these correlations make sense to you?

Apply a transformation to the variables EARN, P15, P25, P35, P45, P55, COMP, NCOMP, and NREST where you Normalize them by total. You can apply this normalization by going to the Data > Transform tab, selecting all 9 variables, selecting Normalize as the Transformation type, and selecting total as the Normalizing variable. After examining the transformed data in the main (right-hand) panel to make sure the transformations were applied correctly, click the Store button.

Evaluate correlations and regressions with both the transformed and un-transformed data. Which do you prefer and why?

When you run regressions, be sure to use the VIF feature in Radiant for a more rigorous evaluation of multicollinearity. As you are building a model it can also be useful to select standardized coefficients (see the regression helpfile). Also, conduct linear regression validation checks by using the dashboard plots in the Plots tab (see section 6.6 in the book and the help file for Regression > Linear (OLS)).

Finally, experiment with the Stepwise selection option in the Summary tab (i.e., click the checkbox). This is a feature in Radiant that uses a purely statistical approach to model building based on the Akaike Information Criterion (AIC). It will go through a series of steps and recommend a final model (see the bottom of the output). Compare the model selected using Stepwise selection to the model you arrived at yourself. Be critical and make a decision about the final model to recommend for Croq`Pain.

**Part (b)**

To use a subset of the CroqPainFix data with only the 50 stores opened up prior to 1994 specify the following filter in Data > View (and press return).

STOR <= 50

After you build your regression model using CroqPainFix select the Predict tab in Regression > Linear (OLS). Here you can select a dataset that you want to generate predictions for using the regression model you specified. Select Data from the Prediction input dropdown. Then from the Prediction data dropdown select the dataset to use for prediction. You can save the predictions for further analysis in Excel by clicking the download icon on the top-right of your screen.

**Part (c)**

This part can be completed using the same Radiant features applied earlier.

Copyright (c), 2018 by Vincent Nijs, Rady School of Management, University of California, San Diego, Otterson Hall, 3W116, 9500 Gilman Drive, MC 0553, La Jolla, California 92093-0553, e-mail: vnijs@ucsd.edu
