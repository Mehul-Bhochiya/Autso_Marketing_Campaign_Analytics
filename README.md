**Austo Motor Company - Customer Purchase & Marketing Analytics**

A complete exploratory data analysis (EDA) project on 1,581 customer purchase records for Austo Motor Company, a manufacturer of SUV, Sedan, and Hatchback vehicles. The project investigates who buys what, fact-checks three marketing-team assumptions against the data, and turns the findings into actionable customer-segmentation and campaign recommendations.


**Problem Statement**
Austo Motor Company's board raised concerns about the effectiveness of its current marketing campaign. This analysis explores the customer purchase dataset to understand who buys which vehicle type, what drives purchase price, and how the marketing team can target customer segments more precisely instead of running a one-size-fits-all campaign.


**Objectives**
- Clean and profile the raw dataset (duplicates, mislabelled categories, missing values)
- Perform univariate analysis on every customer attribute
- Perform bivariate analysis to find relationships between customer attributes and vehicle Make
- Statistically validate three claims made by marketing team members using proportions and repeated sampling
- Quantify spend by gender and loan status
- Test whether partner employment affects purchase price
- Build a four-way customer segmentation with targeting recommendations


**Dataset**
Key columns: Age, Gender, Profession, Marital_status, Education, No_of_Dependents, Personal_loan, House_loan, Partner_working, Salary, Partner_salary, Total_salary, Price, Make


**Data Cleaning**
- Standardised misspelled Gender labels
- Imputed missing Gender values with the mode
- Derived missing Partner_salary values as Total_salary − Salary
- Verified zero duplicate records


**Methodology**
- Data Profiling - shape, dtypes, summary statistics
- Univariate Analysis - distribution of every categorical and numerical field (bar charts, histograms)
- Bivariate Analysis - crosstabs and grouped bar charts of Make against every other attribute
- Sampling - repeated random sampling of the majority class to remove group-size bias before comparing SUV preference by gender
- Stakeholder Claim Validation - three claims tested using proportions rather than raw counts
- Spend Analysis - total/average spend by gender and personal loan status
- Partner Employment Impact - average price by Partner_working, overall and by Make
- Customer Segmentation - Married Male / Married Female / Single Male / Single Female, profiled by vehicle mix and average spend


**Key Findings**
- Sedan is the top-selling body type overall (44%), followed by Hatchback (37%) and SUV (19%)
- When compared as a share of each gender's own purchases, women favor SUVs far more than men (52.6% vs. 9.9%) - the opposite of the raw-count impression and of one stakeholder's assumption
- Age and Salary are the strongest predictors of purchase price; partner employment has virtually no effect
- Married women are the highest-value segment (avg. spend 47,919); single men are the largest budget/entry-level segment
- Existing personal or house loans are associated with lower spend and a lower likelihood of buying an SUV

All three stakeholder claims (Steve Rogers, Ned Stark, Sheldon Cooper) were tested and found not supported by proportional analysis - see the full report for details.


**Tech Stack**
- Python 3
- pandas - data cleaning, profiling, pivot tables, crosstabs
- seaborn / matplotlib - histograms, scatter plots, pair plots, categorical plots
- Jupyter Notebook - analysis environment


**Project Structure**
├── auto.ipynb                  # Main analysis notebook (data cleaning → EDA → segmentation)
├── austo_automobile.csv        # Raw dataset 
├── Austo_Motor_Report.docx     # Full formatted business report
└── README.md


**Full Report**
The complete write-up - including the data dictionary, all univariate/bivariate observations, stakeholder claim verdicts, spend analysis, and segmentation strategy with recommended messaging per segment - is available in the accompanying report document.
