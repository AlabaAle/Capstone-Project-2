# Capstone-Project-2
---
## Project title: Customer Subscription Data
---

### Outline 

[Project Overview](project-overview)

[Data Sources](data-sources)

[Data Description](data-description)

[Tools Used](tools-used)

[Data Cleaning and Preparation](datacleaningandpreparation)

[Data Transformation](data-transformation)

[Data Visualisation](data-visualiztaion)

### Project Overview
---
This dataset provides a comprehensive look at customer subscription patterns and revenue, enabling insights into the drivers of pattern and high-demand subscription of different customer.

### Data Source
---
The main source of data here is Capstone Customer Subscription data.csv which was previously an excel data file then cleaned and converted to Csv file before importing to Sql then visualization on Power Bi for proper investigation

### Data Description
---
The Dataset includes the following fields; 

i. Customer ID: Unique identifier givemn to each customers

ii.Customer Name: Names of the customers

iii.Region: Regions subscriptions were made from

iv.Subscription Type: Type of Subscription package done bu the customers

v. Subscription Start: Date when the subscription commenced

vi.Subscription End: Date when the subscription ended

vii. Cancelled: Shows if the subscription was actually cancelled or not

viii.Revenue: Total amount of money made from the packages

ix. Subscription Duration: Time the Subscription lasted

### Tools Used
---
Microsoft Excel[Dowmload Here](https://Microsoft.com)

  i. For Data Input

 ii. For Analysis

 iii.For Data Cleaning

 iv.For Data visualization

Microsoft SQL Server[Download Here](https://Mictosoft.com)

  i. To manage and querry data

Microsoft Power BI [Download Here](https://Micosoft.com)

  i. For Data Transformation
     Data modelling

  ii.To Create reports and              dashboards that are                collections of visuals.

GitHub[Download Here](https://Alabaale.github.com)

  i. For Portfolio Building

### Data Cleaning and Preparation
---
In the initial data entry phase the following actions were performed;

i. Ensuring data quality by correcting spellings errors, removing duplicates entries and addressing missing values.

ii.Standardization; made to standard by using find and replace in certain fields

iii.Importing of data from excel to SQL then Power Bi.

### Data Transformation
---
Data was transformed to thoroughly clean, remove issues and increase column quality of data, column distribution and profile to 100%.

i. Data Types and Formatting;This was to ensure the data fields were assigned the correct data type with numerical fields formatted as whole numbers, text as text and date fields set to date format.

ii. Sorting: Sorted the dataset by the Date column to organize transactions chronologically.

iii. Created New Columns: Added a new column to have more calculations like Revenue.

### Data Analysis
---
Some of the code used to analysed the data are:

VLOOKUP(lookup_value,table_array,col_index-number,[range_lookup])
LEFT(text,[num_char])
SUMIF(range,criteria,[sum_range])
---

SELECT * FROM [dbo].[LITA Capstone Dataset CSV(1)]

select Region,
count(customeriD) as Total_Customers
from [dbo].[LITA Capstone Dataset CSV(1)]
group by
Region;

select Top 1
SubscriptionType,
count(customerID) as Number_of_Customers
from 
[dbo].[LITA Capstone Dataset CSV(1)]
Group by
SubscriptionType
Order By
Number_of_customers DESC
