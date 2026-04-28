# fifa-permutation-test
Permutation test analysis comparing overall ratings of attackers vs defenders using FIFA 21 dataset.

# FIFA Permutation Test Analysis

## Hypothesis
Do attackers have higher overall ratings than defenders in FIFA 21?

## Dataset
The dataset comes from the FIFA 21 complete player dataset available on Kaggle. It contains player-level information such as position, overall rating, age, and other attributes.

For this analysis, we focus on:
- `position` to classify players into attackers and defenders
- `overall` as the main outcome variable

## Method
We compare the average overall rating between two groups:
- Attackers (e.g., ST, LW, RW, CF)
- Defenders (e.g., CB, LB, RB)

We compute the observed difference in mean overall rating between attackers and defenders.

To assess whether this difference is statistically significant, we use a permutation test:
- Under the null hypothesis, player position is unrelated to overall rating
- We randomly shuffle position labels and recompute the difference in means
- We repeat this many times to generate a reference distribution

Finally, we compare the observed difference to this distribution to compute a p-value.

We also use bootstrapping to estimate uncertainty in the mean difference.

## Goal
Test whether the observed difference is statistically significant.
