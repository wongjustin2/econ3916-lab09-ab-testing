# A/B Testing -- Designing the Data-Generating Process

## Objective
I estimated the causal effect of a job training program from a randomized experiment and used the same tests to judge a mobile game A/B test.

## Methodology
- I loaded the LaLonde NSW job training experiment of 445 people, 185 trainees and 260 controls, and computed the experimental ATE.
- I simulated an observational comparison group to show selection bias and split the observational ATE as Observational ATE = True ATE + Selection Bias.
- I ran a permutation test with 9,999 shuffles and a bootstrap BCa 95% confidence interval for the ATE.
- I ran a power analysis for the power of this study and the sample size needed for three dollar effects.
- I applied the same tests to the Cookie Cats mobile game A/B test of 90,189 players, with the gate at level 30 or 40 and Day-1 retention as the outcome.
- I wrote a sample-size function, n_needed(), checked it against the power analysis, and used it to size a rerun of Cookie Cats.

## Key Findings
- Trainees earned \$1,794.34 more (permutation p = 0.0046, 95% CI \$575.18 to \$3,262.37).
- The simulated comparison group gave an ATE of -\$14,784.45, so without random assignment the program looked like it lowered earnings.
- In Cookie Cats, gate_30 had a Day-1 retention 0.59 pp higher than gate_40, but the difference wasn't significant (p = 0.0752).
- A rerun of Cookie Cats would need 111,192 players per group to detect that difference.
