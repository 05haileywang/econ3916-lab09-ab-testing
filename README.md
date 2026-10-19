# econ3916-lab09-ab-testing

# A/B Testing — Designing the Data-Generating Process

## Objective
The objective of this lab was to understand how A/B testing can be used to estimate causal effects, evaluate statistical significance, and determine the sample size needed for an experiment.

## Methodology
- Used the LaLonde NSW job training dataset to compare earnings between 185 trainees and 260 control participants.
- Calculated the experimental Average Treatment Effect (ATE) and compared it with an observational estimate to understand selection bias.
- Conducted a permutation test with 9,999 shuffles to determine whether the treatment effect was statistically significant.
- Used bootstrap resampling to construct a 95% confidence interval for the ATE.
- Performed a power analysis to evaluate whether the experiment had enough participants to detect the treatment effect.
- Analyzed the Cookie Cats A/B test with 90,189 players to compare Day-1 retention between gates at levels 30 and 40.
- Created a function called `n_needed()` to calculate the sample size required to achieve 80% statistical power.

## Key Findings

### LaLonde Job Training Experiment
The experimental ATE showed that participants in the job training program earned an average of $1,794.34 more than the control group. The permutation test produced a p-value of 0.0046, indicating that the effect was statistically significant at the 5% level.

The 95% bootstrap confidence interval ranged from $575.18 to $3,262.37, providing further evidence of a positive treatment effect.

However, using a simulated observational comparison group produced an ATE of -$14,784.45. This demonstrated how selection bias can lead to misleading conclusions about the effectiveness of a program.

### Cookie Cats A/B Test
The Cookie Cats experiment compared player retention between gates placed at levels 30 and 40. Gate 30 had a slightly higher Day-1 retention rate, with a difference of approximately 0.59 percentage points.

The permutation test produced a p-value of 0.0752, which was above the 0.05 significance level. This suggests that there was not enough statistical evidence to conclude that moving the gate would improve retention.

### Power Analysis
The LaLonde experiment had an estimated statistical power of 80.8%, slightly above the recommended 80% threshold.

I also created a sample-size function to estimate how many participants would be needed to detect a given effect. This showed how smaller effects generally require larger sample sizes to achieve the same statistical power.

## Conclusion
This lab helped me understand the importance of random assignment, statistical significance, and sample size when evaluating experiments. I learned that observational comparisons can produce misleading estimates because of selection bias, and that statistically significant results do not necessarily indicate a large practical effect. I also learned how power analysis can help researchers design experiments before collecting data.
