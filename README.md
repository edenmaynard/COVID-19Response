# North Dakota's COVID-19 Response

# Overview

This project analyzes North Dakota's response to the COVID-19 pandemic using the Susceptible-Infectious-Recovered (SIR) epidemiological model. It applies optimization techniques to estimate transmission rates under public health measures and evaluates the impact of government policies on the state's unsuccessful recovery efforts.

# Key Features

Data Smoothing: Central censoring computes weekly averages to simplify analysis and mitigate the impact of minor fluctuations in the data.
SIR Model Implementation: Simulates the dynamics of susceptible, infectious, and recovered populations using differential equations.
Optimization: Identifies optimal transmission rates (α) by minimizing the residual sum of squares between real-world data and the model's predictions.
Akaike Information Criterion (AIC): Assesses model accuracy using AIC scores to identify the best-fit model for real-world data.
Visualization: Generates graphs comparing the infectious population trends from the SIR models against real data.

# SIR Model Overview

The SIR model categorizes the population into three groups:

Susceptible (S): Individuals at risk of infection.
Infectious (I): Infected individuals capable of transmitting the disease.
Recovered (R): Individuals who have recovered and are no longer infectious.

## Other Variables:
α: Transmission rate (force of infection)
β: Recovery rate
ΔT: Time interval

## Key Insights
Transmission Rate (α): Influenced by public health measures such as mask mandates, social distancing, and business closures.
Recovery Rate (β): Based on the average duration of infectiousness (e.g.,  β=0.05 for a 20-day period).
Exclusions: This model does not consider immunity loss and reinfection, which simulates the initial 120 days of the pandemic.

# North Dakota Government Response

## Timeframe
This analysis focuses on the first 120 days of the COVID-19 pandemic in North Dakota (March 19, 2020, to July 17, 2020).

## Key Policies Analyzed
Business Closures: Implemented on March 27, 2020 (Day 8).
Reopening of Buildings: Initiated on May 1, 2020 (Day 42).
"Smart Restart" Plan: Launched on May 22, 2020 (Day 64) to resume normal activities.
Note: Policies such as mask mandates and social distancing were also introduced but had minimal effect due to low compliance.

# Results

## Real Data
The daily reported COVID-19 infections during the 120-day period are included in the provided CSV file. These data serve as a baseline for comparing the SIR models.

## SIR Models
The simulation evaluates seven models, each considering one or more policies:

Reopening of Buildings + Smart Restart
Business Closures + Reopening of Buildings
Business Closures + Smart Restart
Business Closures Only
Reopening of Buildings Only
Smart Restart Only
No Policies Enacted

## Optimization Results
Optimized Transmission Rates (α)

The optimized transmission rates for each model are:


1. α=0.14,0.07,0.04
2. α=0.26,0.12,0.05
3. α=0.40,0.08,0.04
4. α=0.50,0.06
5. α=0.15,0.04
6. α=0.12,0.03
7. α=0.09

## AIC Scores

Akaike Information Criterion (AIC) is a statistical method for comparing models. The model with the lowest AIC score, when compared to the real number of infections, is the best fit for the real data.

- Model 1: -290.32
- Model 2: -290.46 (Best Fit)
- Model 3: -287.69
- Model 4: -269.21
- Model 5: -281.33
- Model 6: -270.11
- Model 7: -245.91

## Graphical Analysis
The infectious population from each model is plotted against the real data for comparison.

Legend:
- Red: Model 1
- Blue: Model 2
- Green: Model 3
- Yellow: Model 4
- Orange: Model 5
- Purple: Model 6
- Pink: Model 7
- Black: Real data

# Implications

The analysis reveals that Model 2, which includes Business Closures and Reopening of Buildings, aligns most closely with the real data. These policies significantly contributed to North Dakota's failure to contain COVID-19, emphasizing the importance of timing in public health interventions.

This project highlights lessons for future pandemics: poorly timed policy implementation can undermine recovery efforts, even with public health measures in place.
