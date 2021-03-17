NB: This is a template to make documentation process easy. You can remove the `To-Do` notes in your final commit

# Analyze Supermarket Data Across the Country - Company XYZ

Company XYZ owns a supermarket chain across the country. Each major branch located in 3 cities across the country recorded sales information for 3 months, to help the company understand sales trends and determine its growth, as the rise of supermarkets competition is seen.
You will apply learnings to analyse the dataset in the data folder, and the description of each feature can be found in this link (https://docs.google.com/document/d/1Sv-DlynHpOBAs5qKokn5MtbzqZcumTSlSI4-wQ0kf0w/edit?usp=sharing)

# Project Steps

## Step 1 - Loading Dataset
There are 3 csv files for the dataset and each for Branch A, B and C. The 3 files were loaded into a list using glob modules to match the csv pattern. Each file was read and concateneated into a single csv file using `pd.read_csv` and `pd.concat`. The concatenated file was sorted by the Branch column before sending it to another csv file using `pd.to_csv`. The dataset was read back into a pandas DataFrame for analysis.

## Step 2 - Data Exploration
Imported necessary libraries for analysis which include Numpy, Pandas, Matplotlib and Seaborn.
Viewed the first few rows using `head` method and the last few rows using `tail` method to comfirm if the dataset was properly loaded. The `shape` attribite gives the row and column count detail which is 1000 by 17, `columns` attribute gives the column name for each column of the dataset. `describe` method shows the statistical summary of the of the dataset.

from the statistical summary, it is shown that;
- The average unit price of goods is ₦20,041.97 with the minimum unit price of ₦3,628.80 and maximum unit price of ₦35,985.60.
- The average quantity of the goods sold is 5.5 with minimum quantity of 1 and maximum quantity of 10.
- The average cost of goods sold is ₦110,731.46 with minimum of cost of ₦3,661.20 and maximum of ₦357,480.00.
- The average gross income is ₦5,536.57 with the minimum of ₦183.06 and maximum of ₦17,874.00.
- The average customer rating is 6.97 with minimum of 4 and maximum of 10.

Checked the dataset for missing values with `isnull` method and the information of the dataset using `info` method

## Step 3 - Dealing with DateTime Features
Converted the date and time columns to datetime datatype using pandas `to_datetime` method for easy extraction of of the days, months and hours of transaction. It shows that all transaction occured in 11 hours in a day from 10:00am to 8:00 pm.

## Step 4 - Unique Values in columns
Generated unique values from the categorical columns with with `unique` method and converted them into list. The branch column has 3 unique values, city has 3, customer type has 2, gender has 2, product line has 6 and the payment method has 3. All the counts for the unique values were also generated.

## Step 5 - Aggregation with GroupBy
Grouped the dataset on City column with the aggregate function of mean and sum which made it easy to explore the numerical column from the dataset

## Step 6 - Data Visualization
Generated charts with different plotting style using `seaborn visualization library` to uncover some insights from the dataset and provide answer to some questions. All the charts were titles using seaborn `set_title` method.
# Insights
- Branch A(Lagos) has the highest sales record.
- Fashion accessories is the highest sold product line while health and beauty is the lowest.
- For "electronics accessories" and "Sport and travel", the most used payment channel is cash, for "Fasion and accessories", "Health and Beauty" and "Home and Lifestyle", the most used payment channel is Epay and for "Food and beverages", the most used payment channel is Card.
- Branch C has cash as the most used payment channel, Branch A has Epay as the most used payment channel and branch B has card as the most used payment channel.
- Branch B has the lowest rating because most of the customer rating falls between 4-5 and 6-7.
- Females have the higher purchase of Fasion accessories, Food and beverages & Home and lifestyle than male. Also males have the higher purchase of Health and beauty.
Electronics accessories & Sport and travel sales among male and female are close although males have higher purchase of Electronic accessories than females and females also have higher puchase of Electronic accessories than female.
- Electronic accessories has the lowest average unit price while Sports and travel has the highest average unit price.
- Electronic accessories has the highest quantity purchased while Fasion acessories has the lowest quantity purchased.

# Future Work
- Diagnostic Analysis: Looking into the description of all the chart and figure out what caused the trend.
- predictive Analysis: With more previous data of the supermarket the gross profit can be predicted for the coming year.
- Prescriptive Analysis: Looking into what can be done to make the supermarket realize more gross profit.
# Standout Section
- The highest sales record appears in the first month. This is because all branches has high sales record especially branch C and A.
- The second month with a good sales record is month 3. In this month, Branch A has the highest sales across all records but the sales record in Branch C is low which brought down the ran of Month 3 on the list.
- Month 2 has the lowest sales record across the 3 months especially Branch A.
- Having a close look into Branch B sales, all the records for the 3 months are close to each other
# Executive Summary.
Executive Summary can be found in the read.me of the project repository.