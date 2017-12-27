# SpringBoard Exercise: Racial discrimination (Exploratory Data Analysis)

## Context
This repository contains an exercise on Exploratory Data Analysis for the SpringBoard program. The statistical analysis is to establish whether race has a significant impact on the rate of callbacks for resumes. The experiment examines the level of racial discrimination in the United States labor market by randomly assigning identical résumés to black-sounding or white-sounding names and observing the impact on requests for interviews from employers.

The following questions and the working to obtain their answers below can be found in the jupyter notebook.

1. What test is appropriate for this problem? Does CLT apply?
  - A: The problem has discrete outcomes (hired or not hired). Each line, whether the employer response to the resume, can be treated as an independent observation. The CLT states that when independent random variables are added, their properly normalized sum tends toward a normal distribution (informally a "bell curve") even if the original variables themselves are not normally distributed. Therefore I would expect CLT to apply to the rate of call backs.

  We shall apply a two sample permuatation test.

2. What are the null and alternate hypotheses?
  - A: Null hypothesis: The rate of callbacks for resumes is equal for both races (w & b). Alternative hypothesis: Race has a significant impact on the rate of callbacks for resumes.

3. Compute margin of error, confidence interval, and p-value.
  - A: The empirical difference of rates between whites and blacks is  0.032.
  The difference in rates for a 99% confidence interval is between  -0.020 and 0.020
  The margin of error is  0.020
  p-value = 2e-05 (z value of empirical difference in rates:  4.12483009562)

4. Write a story describing the statistical significance in the context or the original problem.
  - A: There is a statistically significant difference in the rate of callbacks between white sounding and black sounding names. In the sample above we see that the rate of call back is ~ 9.7% for white sounding names vs 6.4% for black sounding names. However, the data requires further analysis to determine if black sounding names and white sounding names have any multicollinearity with the other variables before we are able to determine the cause.

5. Does your analysis mean that race/name is the most important factor in callback success? Why or why not? If not, how would you amend your analysis?
  - A: The analysis does not mean that race / name is the most important factor in callback success. To determine if black sounding names and white sounding names are the most important factor, we need to study the other factors. For example, we'd look at multicollinearity with the other variables and determine if other variables have a stronger correlation to callback success.
  It should be noted that even then, we'd only be able to talk to make assumptions based on the data provided. Truly isolating the variables would require sending the exact same resume to the same people at the same time. This, for practical reasons, would not work but running the experiment several times to observe the direction of the bias would be telling.
