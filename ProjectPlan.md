# Overview

# Team

# Research or Business Question(s)

# Datasets

## Kaggle Clause

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
