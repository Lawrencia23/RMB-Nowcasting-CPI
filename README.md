# CPI Nowcasting Project – RMB Monthly Mini Challenge

## Project Overview
This project focuses on nowcasting short‑term inflation using historical Consumer Price Index (CPI) data. Nowcasting refers to estimating near‑term economic indicators before official figures are released. The aim of this project is to provide an early, data‑driven indication of inflation trends that can support timely decision‑making.
The project was developed as part of the RMB Monthly Mini Challenge 4, hosted on Zindi Africa, which tasks participants with estimating CPI values for July 2023 based on available historical data.

## Problem Statement
Inflation plays a critical role in economic and business decision‑making, influencing interest rates, household spending, and cost‑of‑living assessments. However, official inflation figures are released with a delay, creating a gap between when decisions need to be made and when updated information becomes available. This project addresses the challenge of using historical CPI data to estimate near‑term inflation trends before official figures are published, providing an early signal to support more timely and informed decisions.

## Data Description
The analysis uses monthly CPI data covering the period:

January 2022 – May 2023

The dataset includes 13 CPI categories, such as:

Headline CPI
Food and non‑alcoholic beverages
Transport
Housing and utilities
Health
Education
Restaurants and hotels
Miscellaneous goods and services

Each category represents a different component of consumer spending, allowing inflation to be analysed in a more detailed and meaningful way rather than as a single aggregate number.

## Methodology
### Data Preparation

Multiple CPI CSV files were combined into a single dataset.
Dates were standardised and categories were cleaned for consistency.
The data was reshaped into a wide, time‑series format suitable for modelling.

### Feature Engineering

Lagged CPI values were created (previous month values) to capture inflation persistence.
Lagged features reflect the fact that inflation tends to change gradually over time rather than abruptly.

### Modelling Approach

#### A regression‑based model (Ridge Regression) was used.
The approach prioritises:

Stability
Transparency
Short‑term accuracy

The model was evaluated using out‑of‑sample testing, meaning predictions were tested on months the model had not seen during training.

### Baseline Comparison

Model performance was compared against a naive baseline that simply assumes inflation does not change from the previous month.
The model significantly outperformed the naive baseline, confirming that it adds predictive value beyond simply repeating past values.


## Key Visual Outputs
### The following visuals were produced as part of the analysis:


#### Headline CPI Trend
Shows the overall inflation trend over time and highlights inflation persistence.


#### Category Drivers of Inflation
Illustrates how different CPI categories (e.g. food, transport, housing) contribute differently to inflation dynamics.


#### Out‑of‑Sample Actual vs Predicted CPI
Demonstrates how well the model generalises to unseen data.


#### Predicted July 2023 CPI by Category (Bar Chart)
Displays the estimated CPI levels for each category, ranked from highest to lowest.

These visuals were designed to be interpretable for non‑technical audiences while remaining analytically sound.

## Results and Insights
### Key findings from the analysis include:

Inflation remains elevated and persistent over the analysed period.
Food and transport are among the most influential and volatile contributors to inflation.
CPI exhibits strong month‑to‑month persistence, making short‑term estimation feasible.
The model provides realistic and stable predictions, avoiding unrealistic jumps.


### Key Takeaways

Short‑term inflation trends can be estimated reliably using recent historical data.
Simple, interpretable models are well‑suited for nowcasting tasks.
Breaking inflation down into categories provides deeper insight than using headline figures alone.
Nowcasting can act as a decision‑support tool, complementing official statistics rather than replacing them.

#### Disclaimer
This project is intended for analytical and educational purposes. The predictions generated are estimates based on historical data and should not be interpreted as official inflation figures.
