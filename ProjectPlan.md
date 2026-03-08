# Overview
This project analyzes how electricity use and electricity prices have changed in each U.S. state from 2014 to 2024. It focuses on the shift in who generates power, spanning from traditional Electric Utilities to Independent Power Producers (IPPs), and explores whether this change is related to higher or lower electricity prices for residential, commercial, and industrial users. To do this, we use two main datasets from the U.S. Energy Information Administration. The first dataset describes supply-side data from the EIA-860 dataset, which provides information on power plant capacity, producer type, and fuel sources such as coal, natural gas, wind, and solar.  The second dataset represents demand-side data from the EIA-861 dataset, which includes electricity sales (MWh) and average prices (cents per kWh) across sectors and states. After merging the datasets by state and year, we create a timeline that links changes in generation structure to electricity usage and prices. Using this combined dataset, we aim to identify patterns across states and construct simple indicators, such as price relative to generation capacity, to compare areas that rely more on Electric Utilities with those that rely more on Independent Power Producers. 

# Team
Yerin Yun
- Convert the "Existing Capacity" Excel file into a CSV, ensuring the "Producer Type" and "Fuel Source" columns are correctly formatted.
- Summarize generator-level data into State-Year and State-Year-Fuel buckets by source type
- Calculate the Renewable Share and Fossil Share of a state’s total capacity.
- Lead the basic statistical modeling (e.g., regressions) to see if a higher renewable share correlates with lower or higher electricity prices.
- Create "Capacity per Customer" metrics to assess grid reliability.

Brisa Jasso
- Convert the Excel file (HS861 2010-) into a CSV and clean the multi-layered headers.
- Create standardized columns for Sales (MWh), Revenues, Customers, and Average Price.
- Calculate Usage per Customer to measure residential and industrial efficiency.
- Set up the master data merge (Join) between EIA-861 and EIA-860 by State and Year.
- Build the initial time-series trends and geographic maps showing price variations across the U.S.

Shared responsibilities
- Clean data for both datasets. 
- Finalize research questions and analysis plans.
- Review each other’s code through pull requests; ensure both members appear in the git history.
- Co‑write the report, prepare final figures, and polish the project repository.

# Research or Business Question(s)
1. Do states with a higher percentage of Independent Power Producers (IPPs) have lower average Residential Prices (Cents/kWh) compared to states dominated by traditional Electric Utilities?
2. Do states with a higher share of Renewable Generation Capacity (such as wind and solar) have higher or lower average Electricity Prices across different sectors compared to states that rely on fossil fuels?
3. How do trends in Electricity Use per Customer differ for Residential, Commercial, and Industrial sectors when a state's Total Capacity significantly changes?

# Datasets
Two datasets from the U.S. Energy Information Administration (EIA) provide the supply and demand perspectives of the U.S. electricity market. Dataset 1 (EIA-861) represents the demand side of our project, and it has columns of annual electricity sales, revenues, and average prices across the residential, commercial, industrial, and transportation sectors from 2014 to 2024. Dataset 2 (EIA-860) represents the supply side and contains information on power generation infrastructure and ownership, including fuel sources (such as coal, natural gas, wind, and solar) and producer types such as Electric Utilities and Independent Power Producers. These datasets are highly compatible and will be integrated using Year and State Code as common identifiers. This integration allows us to link changes in a state's electricity generation capacity and producer structure to electricity prices paid by consumers. Both datasets are sourced directly from the U.S. federal government, ensuring high standards of data quality, accuracy, and reproducibility.

Dataset 1- EIA-861 Annual Electric Power Industry Report (released: 10/7/2025)
- Annual sales to ultimate customers by state and sector
- Date range: 2014 – 2024 (we will use this timeframe of data only)
- Columns - Year, State, Residential, Commercial, Industrial, Transportation,  Total (Revenues (thousand dollars), sales (MWh), Customers (count), Price (Cents/kWh) )

Dataset 2 - EIA-860 Annual Electric Generator Report (released: 9/9/2025)
- Existing Nameplate and Net Summer Capacity by Energy Source, Producer Type and State (EIA-860)1, 3
- Date range: 1990 – 2024 (2014 – 2024 (we will use this timeframe of data only)
- Columns - Year, State Code, Producer Type, Fuel Source, Facilities, Nameplate Capacity (Megawatts), Summer Capacity (Megawatts)

## Kaggle Clause
Our team doesn't use Kaggle datasets.

# Timeline
This project will be completed over several weeks through a structured plan that involves data acquisition, cleaning, integration, analysis, and final reporting.

### Week 1 - Data Acquisition and Data Cleaning (Brisa and Yerin)
- Download the EIA-860 and EIA-861 datasets from the U.S. Energy Information Administration (EIA).
- Convert Excel files into CSV format to prepare for future analysis.
- Upload datasets to GitHub Repository.
- Clean the EIA-860 dataset with Python and correctly format the "Producer Type" and "Fuel Source" columns.
- Clean the EIA-861 dataset in Python by reformatting the multi-layered headers and standardizing Sales (MWh), Revenues, Customers, and Average Price columns.
- Prepare datasets for integration by summarizing generator-level data into State-Year and State-Year-Fuel groups.
- Verify that state and year identifiers match across both datasets.

### Week 2 - Data Integration (Brisa and Yerin)
- Merge the EIA-860 and EIA-861 datasets using State and Year as shared keys.
- Validate the merge by checking that states and years are properly matched.
- Calculate Renewable Share, Fossil Share, Capacity per Customer, and Usage per Customer columns.

### Week 3 - Exploratory Data Analysis (Brisa)
- Generate time-series visualizations showing electricity price trends across states.
- Create geographic visualizations to compare electricity prices by state.
- Calculate statistical summary measures for the target variables.
- Calculate correlations between capacity share, producer type, and electricity prices.

### Week 4 - Statistical Analysis (Yerin)
- Use Python to conduct regression analysis to test if higher renewable share is associated with electricity prices.
- Evaluate model results and statistical significance.
- Interpret model results in the context of electricity market changes.

### Week 5 - Final Report (Brisa and Yerin)
- Write the final report including methodology, analysis, and conclusions.
- Ensure code is reproducible and upload the final project to GitHub.

# Constraints
While these datasets come from a reliable source, there are still chances of constraints as we work though our project plan. 

First, the datasets contain complex structures such as the multi-layered headers and large amounts of variables. This may lead to technical difficulties in the data cleaning and preparation steps.

Second, challenges may be presented during the merging of the EIA-860 and EIA-861 datasets. Formats or definitions may vary across dataset or even update over time. It is important to repeatedly validate and keep track of what version of the datasets we are working with to ensure accurate merging.

Third, our analyses will be completed at the state level which can be an issue during analysis and reporting. Our state calculations may be too broad or skewed because it captures the entire state and does not account for variations within states. This may lead to missed trends or patterns in the electric market within states or other local levels.

Finally, we focused our project on data for generation capacity and producer type, but electricity prices likely have other highly impactful variables that are not captured by our datasets. For example, electricity prices can be influenced by weather, regional regulations, or fuel prices. Thus, we cannot make any causal relationships, but we can find correlations with the variables we do cover.

# Gaps
As with any analysis, there are endless factors that can highly impact the target variable and improve analysis. While our focus on the supply and demand variables available are strong choices for analysis on electricity prices, there are still other variables that could lead to more insights. 

One main gap is the lack of data on fuel prices. Electricity prices are often strongly influenced by fuel prices such as natural gas or coal. With more time, this would be the top gap to address and strengthen our analysis. 

Another gap is the lack of policy information. State renewable portfolio standards, subsidies, or regulatory changes may significantly affect renewable adoption and electricity pricing but are not included in the datasets.

Aside from variable gaps, one area that could also strengthen our findings is exploring other statistical or modeling methods. We currently plan to use simpler statistical modeling techniques such as regression, but there may be other methods that would be better suited for this data. 

If ever to continue this project beyond this class, it would be important to find more data and explore other modeling techniques to best understand how electricity prices fluctuate and what influences those changes.
