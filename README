# Bayesian Hierarchical Models for Expected Goals, Temporal Stability, and Possession Value in the AHL

**Project Contributors:**
Sydney Stanton

## Project Overview
This study applies Bayesian hierarchical modeling to tracking-enhanced event-level data from 480 American Hockey League games, provided directly by the Colorado Avalanche analytics department through the HALO Hackathon. Prior studies have developed expected goals models using frequentist methods or black-box commercial systems, whereas this study leverages NHL Edge player and puck tracking data — collected via active infrared sensors embedded in pucks and sewn into players' jerseys — to address three interconnected research questions using principled Bayesian inference throughout.
Traditional hockey evaluations rely on goals and assists, which are poor metrics as they are rare and random events. A challenge in hockey is the sparsity of player-level data, where players may take only 30-80 shots in an entire season. Partial pooling in Bayesian hierarchical models addresses this by borrowing information across players, making Bayesian methods particularly well-suited to hockey analytics. This research quantifies patterns previously based solely on intuition to inform evidence-based strategies, transforming subjective hockey intuition into measurable and quantifiable intelligence for coaches, general managers, and analysts.

Research Questions:
1. How does xG (Expected Goals) vary by shot location and player?
2. Is that xG relationship stable across time, or does a player's shooting probability from a given location drift across a 10-game window?
3. How does each puck action change the probability of generating a dangerous offensive outcome within the next 10 seconds, given spatial and game context?

Data
Source: Colorado Avalanche analytics team via the HALO Hackathon

## Final Results Summary 
### Question 1 — How does xG vary by shot location and player?
Shot location is the dominant driver of expected goals. The quadratic depth term was the strongest predictor of goal probability, confirming that shooting percentage does not decline linearly with distance from the net but accelerates as shots move further away. The posterior mean xG surface showed the hot zone (30%+ xG) directly in front of the net, fanning outward in a cone shape, confirming the model learned correct hockey geography. A correlation of 0.56 was calculated between the model's xG and the Colorado Avalanche's proprietary xG metric, demonstrating that location and player alone explain roughly 32% of variance before adding any contextual features. The player random effect was near zero (sd = 0.05) after controlling for location, confirming that where you shoot from matters far more than who is shooting.

### Question 2 — Is the xG surface stable across a season?
The static xG surface from Question 1 is a reliable seasonal summary. Sigma drift was estimated at 0.025 on the log-odds scale (95% CI: 0.001–0.071), corresponding to a shift of just 0.10% in goal probability per 10-game window, less than one-twentieth of a single goal across a typical block of 30 shots. Player shooting profiles do not meaningfully drift across 10-game windows, meaning coaches and analysts can rely on single-season location-adjusted xG estimates without worrying that early-season patterns will become obsolete by playoff time. A scatter plot classified players into four quadrants — reliable high-danger shooters (Fagemo, Samuel; Gawdin, Glenn), skilled but inconsistent (Gaudette, Adam), consistent underperformers, and below-average inconsistent, visually confirming that temporal instability is negligible for the vast majority of players.

### Question 3 — How does each puck action change danger probability?
Puck action context substantially outweighs location in predicting danger. The most important findings were:

One-timers (+1.54 log-odds) — the strongest single predictor, adding roughly 15-20 percentage points of danger probability regardless of location
Successful actions (+1.33) — whether an action succeeds is nearly as predictive as whether it is a one-timer
Slot passes (+1.08) — passing to the home plate area is nearly as dangerous as a one-timer
Rush passes (+0.67) — passes off the rush substantially increase danger over static zone passes
Pass + one-timer (65%) — the most dangerous specific scenario in the dataset, nearly triple the overall danger rate of 21.9%

The gap between a baseline pass (33%) and a pass setting up a one-timer (65%) is a 32 percentage point difference from a single contextual feature — the most striking quantitative finding of the project. Individual player skill in generating dangerous situations proved substantial (sd = 0.37), a finding completely invisible to traditional location-only xG models.

## Conclusion 
First, shot location is the lead driver of expected goals and individual finishing skill is largely insignificant, where you shoot from matters more than who is shooting. Second, the static xG surface is a reliable seasonal summary, player shooting profiles do not drift across 10-game windows, validating its use as a stable evaluation tool. Third, and most importantly, when the lens shifts from shot-making to danger creation, context reigns above everything else. The same action can have drastically different implications for danger depending on its context, and some players are systematically better at creating danger regardless of what action they take or where they take it. A skill completely invisible to traditional xG models.
These findings show that Bayesian hierarchical modeling gives hockey analytics a reliable new path — quantifying uncertainty honestly, handling sparse player-level data responsibly, and revealing the contextual importance behind real offensive value.



