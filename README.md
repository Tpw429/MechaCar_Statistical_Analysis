# MechaCar_Statistical_Analysis

In this repository, I will be exploring MechaCar data vs Competitors to see who has the edge in certain aspects. During this project, I worked with excel files (csv) and loaded them into R and Rstudio to run analysis. The results of my project will be explained below.

## Linear Regression to Predict MPG

Question 1: Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?
- The variables/coefficients that provided the most non-random amount of variance to the mpg values were the Spoiler Angle, AWD, and Vehicle Weight all provided non-random variance to the mpg value. They are directly tied to the impact on the mpg value.

Question 2: Is the slope of the linear model considered to be zero? Why or why not?
- The slope of the linear model is not considered 0. The p-value for this data set was 5.35x10^-11 which is much lower than the alpha value of .05. This means changes in the predictor variable are tied with changes in the response variable.

Question 3: Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?
- My R-squared value predicted the mpg of MechaCar prototypes correctly 71.49% of the time. This mean nearly 28.5% if failed. Although it is almost 3/4 of the way effective, I would not feel comfortable setting this model forward. There are other factors/variable that could greatly increase the effectiveness of our R-sqaured value. There are probably many variables we do not have access to which would increase our model effectiveness. A figure showing my R-squared value is shown below.

![LinearRegressionOverview](Resources/LinearRegressionOverview.PNG)

## Summary Statistics on Suspension Coils

Do the design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. Does the current manufacturing data meet this design specification for all manufacturing lots in total and each lot individually? Why or why not?

- Lot 1 will work. It meets the specification requirements listed above.
- Lot 2 will work. It meets the specification requirements listed above.
- Lot 3 will not work. It has a variance of 170.3 which exceeds the 100 psi set forth in the design specifications.


![CompleteSummary](Resources/CompleteSummary.PNG)

![LotSummary](Resources/LotSummary.PNG)


## T-Tests on Suspension Coils

The next portion of this project I would like to talk about are the T-tests. The first image is a combination of the three T-tests. The following ones are the individual T-test for lots 1, 2, and 3.

In the first combo T-test we see the p-value as 0.06 which is greater than the significance level of 0.05. For this reason, the distribution is not very different from the normal distribution and we can assume normality. T-test for lot 2 is shown below.

![TtestFull](Resources/TtestFull.PNG)

For the T-test on Lot 1 the p-value was 1 which is greater than the significance level of 0.05. For this reason, the distribution is not very different from the normal distribution and we can assume normality. T-test for lot 1 is shown below.

![TtestLot1](Resources/TtestLot1.PNG)

For the T-test on Lot 2 the p-value was 0.6 which is greater than the significance level of 0.05. For this reason, the distribution is not very different from the normal distribution and we can assume normality. T-test for lot 2 is shown below.

![TtestLot2](Resources/TtestLot2.PNG)

For the T-test on Lot 3 the p-value was 0.04 which is less than the significance level of 0.05. For this reason, the distribution is  very different from the normal distribution and thus we cannot assume normality. T-test for lot 3 is shown below.

![TtestLot3](Resources/TtestLot3.PNG)

## Study Design: MechaCar vs Competition

In this segment, I will be comparing MechaCar to the Competition. In specific, we will need to look at certain attributes like safety rating, horsepower, fuel efficiencies, etc. To do this we need to lay out a mission. The metric that I think most people would consider first is cost. How does MechaCar price its cars in comparison to its close competition. Is it much cheaper? Is it extremely expensive? This is a great question which can help us understand MechaCar evaluations against its competitors. The null hypothesis is the researcher;s prediction is false. We would predict that that MechaCar is priced competetively with competition. The alternate hypothesis is that the researcher's predicted difference is true. In order to test the hypothese, I would use a sample t-test whcih allows us to decide between and null hypothesis and an alternative hypothesis. In order to run the statistical test we would have to take sample data with certain features between the compeitition and MechaCar to perform a t-test. We would then compare the p values to see if the difference is greater than the significance level (0.05) to show that the distribution is not significantly different from the norm distribution. If this is true, we can assume MechaCar's product is similarily priced to competition and has normality.
