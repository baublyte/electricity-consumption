# Electricity Consumption profiles

This project analyzes electricity consumption data from 106  unique objects (total objects 1000) and electricity price data (https://www.litgrid.eu/index.php/sistemos-duomenys/elektros-energijos-kainos/86) to derive insights into usage patterns, costs, and optimal pricing plans (Minimalus, Standartinis, Lankstus). 


## Junior Data Analyst Tasks: Analyze electricity consumption and pricing data to derive summary statistics and trends.

- Task A: Calculate the total electricity consumption (kWh) for apartment 771822.

- Task B: Compute the median daily consumption (kWh) for apartments and houses for each month.

Present the results as:
A tabular summary and a plot illustrating monthly medians.

- Task C:  Identify the date and hour with the highest hourly electricity price in 2022. Calculate the percentage difference between this price and the average hourly price for the same year.

## Advanced Data Analyst Tasks: Simulate and evaluate optimal electricity pricing plans for residential users based on historical consumption and pricing data.

Optimal Pricing Plan Simulation:

- Minimalus: €1.00/month + €0.22/kWh.
- Standartinis: €2.00/month + €0.20/kWh.
- Lankstus: €3.00/month + €0.08/kWh + NordPool hourly price.

Calculate the monthly cost for each object under each pricing plan, identify the cheapest plan for each apartment for every month and generate a visualization showing the preferred plan for each apartment per month.

- Identify the apartment that most frequently benefits from the Minimal plan.
- Identify the apartment that most frequently benefits from the Flexible plan.

## Repository structure

consumptions-profiles/
├── data/
│   ├── raw/                                    # Folder for raw data files
│   ├── h5/                                     # Processed data files in HDF5 format
│   │   ├── cleaned_data.h5                     # Fully cleaned electricity consumption data
│   │   ├── combined_data.h5                    # Combined consumption and price data
│   │   ├── electricity_prices_2020-2022.h5     # Processed NordPool price data
│   │   ├── electricity_prices.h5               # General processed electricity price data
│   ├── Nordpool/                               # Folder for NordPool electricity price data
│   │   ├── 2022-electricity_price.csv # Raw 2022 price data
│   │   ├── electricity_prices_2020-06-01_2022-06-01.csv # Raw price data for 2020-2022
├── images/                                     # Folder for visualizations and plots
├── utils/                                      # Folder for Jupyter Notebooks and scripts
│   ├── data_preparation.ipynb                  # Notebook for cleaning and filtering raw data
│   ├── combine_data.ipynb                      # Notebook for merging consumption and price data
│   ├── electricity_consumption_price.ipynb     # Notebook for Junior Analyst tasks
│   ├── optimal_electricity_price_plan.ipynb    # Notebook for Advanced Analyst tasks
├── requirements.txt                            # Python dependencies for the project
├── README.md                                   # Project documentation
