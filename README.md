# PXL Assignments 2024 - Time series analytics

Assignments for students at PXL Hasselt.

## Assignment 1 - Data preparation

**Objective**: Understand how to prepare a data matrix from possibly non-equidistant multivariate input data.

**Method**: Load the feather file 'tsai-antwerp_data.feather’ into a dataframe.  Select only data with series names containing “CV”. Create a data matrix (pivot). Resample so you have a data point every minute. Interpolate missing values. Make sure to inspect results after every step.

**Questions**:
- Did you need to add additional preprocessing steps?
- How did you decide on the interpolation mechanism?


## Assignment 2 - Amazon Chronos

**Objective**: Understand how recent foundational models can be used for time series predictions.

**Method**: Run the minimal example explained in the [amazon git repo](https://github.com/amazon-science/chronos-forecasting?tab=readme-ov-file).  Adapt the code to answer the questions below.

**Questions**:
- Is the predicted behavior logical?
- Do we need (cross-)validation?
- What happens if you increase the prediction length (to 5 years after the last available data point)?
- Change the model to the “tiny” version and analyze how this changes the results. 
- Apply the model on a new dataset (eg. sensor-1.csv with prediction length of 64, or an example you generate or download yourself). 

## Assignment 3 - Autogluon

**Objective**: Understand how autogluon can be used to find the best performing time series model for your data

**Method**: Run the quick start example from the autogluon website: https://auto.gluon.ai/stable/tutorials/timeseries/forecasting-quick-start.html#. Adapt it to train on the provided dataset (eg. D1RN1L02VO01.csv). Use .train_test_split to split the data set in a training and test set for the forecast based on your desired prediction length (eg. 48 hours). 

**Questions**:
- Plot the predictions against the true values
- Which model performs best?
- Can you interpret the model scoring metric used (MASE)?

## Assignment 4 - CUSUM

**Objective**: Understand how the very basic cusum technique works.

**Method**: Create a noisy sample signal with a mean shift and implement the statistic. Assume you know the mean of the data before the shift. Reset the statistic when a change point is detected.

**Questions**:
- How do the statistics behave when there is no shift? And after the shift?
- Add a way to detect negative mean shifts
- Adapt the threshold and the threshold value, and observe impact, and observe the impact on ARL0 and detection delay

