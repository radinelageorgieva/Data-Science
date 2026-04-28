# Data-Science
How socio-economic factors influence real estate prices in New York City

This project presents a comprehensive econometric analysis of the New York City real estate market. By integrating over 50,000 annualized sales records for the period 2016 september - 2017 september with granular US Census socio-economic data for 5 year - 2013 - 2017, the study moves beyond descriptive statistics to uncover the most drivers of property value in one of the world's most complex urban environments.

Research questions
1. Does location act as a primary driver for property valuation in NYC, and is this impact statistically significant?
2. How do professional occupations influence the property market?
3. Which factor square footage or the economic status of the neighborhood holds a stronger correlation with the sale price?
4. How do different modes of transport and commute times to work affect the market attractiveness and pricing of real estate?
5. Are there identifiable temporal cycles in the real estate market that suggest seasonality in transaction patterns?

Data sources
The study utilizes open-source data from:
1. NYC property sales dataset - nyc-rolling-sales.csv (https://www.kaggle.com/datasets/new-york-city/nyc-property-sales)
2. US Census tract dataset - acs2017_census_tract_data.csv (https://www.kaggle.com/datasets/muonneutrino/us-census-demographic-data)
3. Geographic correspondence table - geocorr2022_2611807397.csv : https://mcdc.missouri.edu/cgi-bin/broker?_PROGRAM=apps.geocorr2022.sas&_SERVICE=MCDC_long&_debug=0&state=Ny36&g1_=zcta&g2_=tract&wtvar=hus20&nozerob=1&fileout=1&filefmt=csv&lstfmt=html&title=&afacts2=on&xycentr=1&counties=&metros=&places=&oropt=&latitude=&longitude=&distance=&kiloms=0&locname=

Analitical framework:
1. Data Cleaning & integration: Addressed significant data gaps (MNAR) in Manhattan's square footage records and filtered the dataset at a $5M threshold to focus on the residential middle market.
2. Exploratory Data Analysis (EDA): Using histograms and scatter plots to visualize trends and relationships.
3. Hypothesis testing: Welch’s ANOVA & Games-Howell: Applied to handle heteroscedasticity and unequal group sizes across boroughs.
4. Multiple Linear Regression
5. Bayesian inference (Bayes Factor): Provided decisive evidence (BF10 = inf) for the impact of accessibility on price.
6. Fourier Transform (FFT): Identified rhythmic weekly and quarterly market cycles.

Code findings
1. Commute time is the strongest negative predictor (-0.45). In NYC distance is measured in minutes, not kilometers.
2. Status & Gentrification: A strong positive correlation (0.42) exists between property values and  professional density, showing active gentrification.
3. Economic decoupling: In core areas like Manhattan and Brooklyn, prices have significantly detached from local earnings (Affordability Ratios > 20), driven by global capital.
4. Buyers prioritize interior utility (Gross SQFT) and accessibility over land area, reflecting the vertical nature of the city.

Tech Stack
Language: Python
Libraries: pandas, numpy, matplotlib, seaborn, scipy, statsmodels, re, contextily, folium,  pingouin


