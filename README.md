# bank_loan_case_study

Project description:

The project focuses on analysing a dataset containing information on customer loan
applications to identify patterns that predict loan defaults. The aim was to ensure that
creditworthy applicants are not rejected while mitigating financial risks from unreliable
applicants. Exploratory Data Analysis (EDA) was utilized to clean and explore the data,
uncover trends, and analyse factors influencing defaults.

Approach:

1. Data Cleaning and Preprocessing:
   
 Handling Missing Values: I Dropped columns with more than 40%
missing data. For other columns, categorical values were filled using mode,
and numerical values were filled with median.

 Negative Value Transformation: Negative values in time-related columns
(e.g., DAYS_BIRTH, DAYS_EMPLOYED) were converted to absolute
values and expressed in years.

 Outlier Detection: Identified and removed outliers using the Interquartile
Range (IQR) method for key columns like AMT_INCOME_TOTAL,
AMT_CREDIT, and CNT_CHILDREN.


3. Feature Reduction:
   
 I Dropped less significant columns such as document flags and features
with minimal predictive value.


5. Visualization and Analysis:

 I Plotted bar charts, histograms, boxplots, and scatterplots to analyse data
distribution and relationships.

 Segmented data by default status (TARGET) to compare characteristics of
defaulters and non-defaulters.

 Created correlation heatmaps to identify relationships among financial
metrics and defaults.


Tech-Stack Used:

 Python: Core language for data analysis.

 Pandas: Data manipulation and preprocessing.

 Matplotlib & Seaborn: Visualization libraries for insights.

 Google Colab: Hosted environment for analysis and execution.


Insights:

 Imbalance Ratio: 

Non-defaults significantly outnumber defaults, with a ratio of
11:1.

 Default Characteristics:

o Customers with higher credit amounts and lower incomes show a greater
likelihood of default.

o The number of children has a weak but notable association with default
rates.

 Contract Types: 
Defaults are more prevalent in specific loan types (e.g., Cash
Loans vs. Revolving Loans).

 Income and Credit Relationship: Weak correlation between income and default,
but stronger ties with credit amounts.


Result:

This project provided me a comprehensive understanding of patterns associated with
loan defaults. Key findings include the influence of income, credit amount, and
demographic factors. The insights obtained can assist in enhancing the company’s risk
evaluation strategies, enabling better loan approvals and financial planning.


Project Details:

Initial Data Handling:
 I began by importing the data from a CSV file, bringing in a hefty table with
almost 50,000 rows and 122 columns.

 I checked for duplicated rows and found none—clean start.


Data Cleaning:

 I tackled missing values. First, I identified columns with more than 40%
missing data and dropped them, trimming down the dataset to 73 columns.
![Screenshot 2024-11-17 152439](https://github.com/user-attachments/assets/21805191-c77d-4b8a-aa36-66af2dc8c42f)

Then I took care of those negative values by converting them to positive, and
converted to absolute days ensuring the data stays realistic.

![Screenshot 2024-11-17 152751](https://github.com/user-attachments/assets/384b9580-760d-4186-b2da-e4d4c37229da)


Further Reduction and Cleaning:

 I dropped a bunch of document-related flags and other less relevant columns
based on my discretion, further reducing the dataset to 48 columns.

 Filling in missing values for categorical and numerical data was up next, using
modes and medians.


Outlier Handling:

 Addressing outliers is critical in loan data to avoid skewed analysis, and I
handled it by defining reasonable bounds and filtering out the extremes. This
step helps in refining the model’s predictions by keeping only the most
representative data.
![Screenshot 2024-11-17 153906](https://github.com/user-attachments/assets/2c305005-78ee-43bb-9c3d-0b853f1c2f9f)
![Screenshot 2024-11-17 153917](https://github.com/user-attachments/assets/c3078339-57ac-464b-a036-de1e5392510b)
![Screenshot 2024-11-17 153928](https://github.com/user-attachments/assets/e0bf4fd2-966a-4972-8c39-bb8fdf639b86)
![Screenshot 202![![Screenshot 2024-11-17 154001](https://github.com/user-attachments/assets/456421f2-bacf-4c49-9d3c-e79989156100)
Screenshot 2024-11-17 153951](https://github.com/user-attachments/assets/51a3840e-93d6-4ef9-9ec6-6dfda9450856)
4-11-17 153938](https://github.com/user-attachments/assets/a8002888-2180-4aff-bd38-5fe6806c1484)

Cleaned data visualization:

![download](https://github.com/user-attachments/assets/df1317f6-74c4-42c6-a3eb-a4636f73e17c)


Distribution of Total Income:

o Shows a multimodal distribution, with major peaks indicating common
salary levels, indicating that the majority have lower incomes, with a few
high earners.


 Distribution of Credit Amount:

o Suggesting specific loan amounts are more popular than others. Most loans
are concentrated in the lower range, with fewer high-value loans.


 Distribution of Annuity Amount:

o With a peak around 25,000, indicating this is a common annuity amount.
It suggests most loans have similar repayment terms.


 Total Income vs. Credit Amount Scatter Plot:

o Displays a positive correlation, indicating that generally, as income
increases, so does the credit amount. However, there is substantial
variability, especially at lower income levels.

Sharp and concise, these visuals indicate the dataset features common financial
behaviours and preferred loan structures, with variability that requires deeper
analysis to fully understand borrower behaviour and credit risk.


Exploratory Data Analysis (EDA):

 Univariate Analysis: I started simple with histograms and boxplots to understand
the distribution of key variables like income, credit amount, and annuity. This
helped me get a sense of the central tendencies and variability—fundamental for
any risk analysis.

![Untitled design](https://github.com/user-attachments/assets/28b7a77a-e262-468d-88c9-b339ce5fce43)


Credit Amount: 

Peaks early, suggesting most loans are small to mid-sized. The
long tail hints at fewer high-value loans.

 Total Income: Highly concentrated at lower incomes showing very high
earnings, indicating income disparity among applicants.

 Annuity Amount: Most annuity payments cluster under 20,000 with a smooth
decline afterwards, suggesting standard loan terms for the majority.

 Number of Children: Most applicants have no or one child, with very few having
two, showing a trend towards smaller families among loan applicants.

 Boxplot of Total Income: Indicating some applicants have exceptionally high
income levels compared to the norm.

 Boxplot of Credit Amount: Most credits are moderate, but the range is wide,
indicating diverse loan sizes are being issued.


Bivariate and Multivariate Analysis: 

I analysed relationships between various
financial variables and the loan default status (TARGET). Using scatter plots and
correlation analysis, I identified how different financial behaviours might relate
to default risks.
![Screenshot 2024-11-17 162249](https://github.com/user-attachments/assets/61e80929-743c-4089-97c8-29c7a4ad240f)

Annuity Amount vs. Default Status:

o Virtually no correlation (0.01), indicating annuity amount doesn’t strongly
predict default status.

 Number of Children vs. Default Status:

o Weak correlation (0.02); more children doesn't significantly increase
default risk.

 Credit Amount vs. Default Status:

o Slight negative correlation (-0.02); higher credit amounts marginally
decrease the likelihood of default, albeit very weakly.

 Total Income vs. Default Status:

o Negligible negative correlation (-0.02); higher income doesn’t strongly
protect against defaulting.



![download (20)](https://github.com/user-attachments/assets/c1beb70e-7828-4ef3-a392-6d72b2381d77)
![download (19)](https://github.com/user-attachments/assets/61f6f88c-a323-4f03-83b7-a8b417baefd2)

Contract Type by Default Status:


o Cash loans are significantly more common than revolving loans.

o Default rates are proportionally higher for cash loans compared to
revolving loans.


 Gender by Default Status:

o Males have a slightly higher default rate compared to females.

o Overall, females take out more loans but have a lower relative frequency
of default.

Cash loans are more prone to defaults, and gender does play a role, with males
showing a marginally higher tendency to default than females.


Segmented Analysis: 

By splitting the data based on the loan default status, I
could tailor my insights into how different groups (defaulters vs. non-defaulters)
behave. This kind of segmented analysis is crucial for developing targeted
strategies in risk management.

Income by Default Status:


o Higher counts of non-defaulters across most income levels.

o Defaulters slightly more common in lower income brackets.


 Credit Amount by Default Status:

o Non-defaulters dominate across all credit amounts, particularly at lower
amounts.

o Default rates slightly increase at mid-credit amounts.


 Annuity Amount by Default Status:

o Similar to credit amounts, non-defaulters are more frequent across all
annuity levels.

o Defaulters are slightly more frequent at lower annuity amounts.


 Boxplot Insights:

o Total Income: 

Median income for non-defaulters slightly higher than
defaulters.

o Credit Amount:

Defaulters and non-defaulters have similar medians, but
defaulters have slightly higher variability in credit amounts.


o Annuity Amount: 

Non-defaulters show a higher median annuity,
indicating possibly larger or longer-term loans compared to defaulters.
Sharp and clear, these graphs underscore that non-defaulters generally exhibit
higher or more consistent financial engagement across income, credit, and
annuity metrics, with defaulters showing a tendency towards lower economic
activity and higher variability in credit engagement.

![Screenshot 2024-11-17 162834](https://github.com/user-attachments/assets/a0ef3d25-ccb1-4394-bb2c-3ad713b741f8)


Heatmap:
![download (17)](https://github.com/user-attachments/assets/e2e2a1e1-8239-4f64-b424-c888c2988202)

Income and Loan Amounts: 
There are moderate correlations between income,
credit amount (0.34), and annuity (0.42), indicating that as income increases, so
generally do the loan and annuity amounts.


 Credit and Annuity:

A strong correlation (0.77) exists between credit amount
and annuity, suggesting that higher loan amounts usually come with higher
annuity payments.


 Target (Default Status): 

Virtually no correlation with income, credit, or annuity
(all ≤ 0.02), suggesting that these financial metrics alone are not predictive of
defaulting on loans.
While financial amounts are interconnected, they don’t tell us much about who’s
going to default.


Visualizations and Insights:

 I created various visualizations such as histograms segmented by TARGET,
boxplots for income and credit segmented by default status, and heatmaps of
correlations. These visual tools not only make my findings more accessible but
also highlight key patterns that can inform risk assessments and decision-making
processes.

![download (18)](https://github.com/user-attachments/assets/7dcd2e68-cdf3-4272-8bfc-49d2b1a61069)


Age and Employment:

A strong correlation between days since birth (age) and
days employed (0.63), indicating a logical increase in employment duration as
age increases.


 City Ratings:

High correlation between the client's city rating and the region
rating (0.95), suggesting that these ratings typically align and are possibly
redundant.


 Registration and Employment: 

Days since registration shows moderate
correlation with days employed (0.33), possibly indicating longer-term residents
tend to have stable employment.


 Employment and Phone Change: 

Negative correlation between days employed
and days since last phone change (-0.27), hinting at less frequent phone changes
as employment duration increases, perhaps reflecting stability.


 Independence of Default: 

No strong correlations directly tying default status
with other individual metrics, suggesting default is influenced by a complex set
of factors not solely described by any single attribute here.

This heatmap shows some expected relationships between personal and regional
characteristics, but these alone don’t straightforwardly predict loan defaulting,
indicating a need to consider broader, possibly more complex models.



Final Steps:


 After cleaning and analysing, I prepared the dataset for predictive modelling or
further analysis by other teams. My work sets a solid foundation for making
informed decisions on loan approvals based on data-driven insights.
