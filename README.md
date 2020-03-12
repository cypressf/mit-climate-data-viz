# Background on the MIT Global Change model (EPPA)

- It's written in general algebraic modeling software (GAMS)
- The foundational data is in GTAP (paid data, so they have to make the public model lag behind the most recent data release)
- It takes ~20 min to run
- We'll precompute a set of standardized scenarios, then plot that in the data-viz, and allow people to select the variables they want to plot
- Whenever we want to run the model on a new case, we'd want to precompute more results and add that to the visualization

# Use cases

1. Public outreach and communications tool (wouldn't upload everything)
    - Preloaded with a couple scenarios
    - Allow people to upload their own scenarios
2. Help researchers explore results of test runs (sometimes 15 different scenarios a day)
    - Currently they use excel, but it could be faster to use this tool

- energy by type, by region
- electricity use by type, by region

# Choosing the best approach

1. Ue the gcam dashboard, written in R, adapt output of models to fit format expected by that
    - drawback: not the best option for graphical interface
    - drawback: the regional definitions are different than GCAM
    - although the visualizations are similar (energy by region, energy by fuel), code may have different regional definitions, which may be difficult to change
2. Build it using javascript + html, and a data-viz library such as d3.js
    - drawback: building more from scratch