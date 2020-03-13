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

## Use the gcam dashboard

GCAM dashboard is a climate data visualizer written in R. I'd adapt the output of EPPA to fit format expected by GCAM. I've [forked GCAM dashboard](https://github.com/cypressf/GCAM-dashboard/commit/559d2181f4c502f9daf315c1ba5bc6354716d3b9) to start changing it to do what we need.

- drawback: not the best option for graphical interface
- drawback: the regional definitions are different than GCAM
    definitions, which may be difficult to change

## Build it using a javascript data-viz library

We could use a library such as d3.js

- drawback: building more from scratch
