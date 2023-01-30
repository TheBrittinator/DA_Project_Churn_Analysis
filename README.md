# DA_Project_Churn_Analysis
## BANK CHURN

*Brittney Kakie*

![](Churn-Prediction-scaled.jpg)

> **About this dataset**
> 
> A bank is concerned that more and more customers are leaving its credit card services. It would be appreciated if someone could analyze it and come up with recommendations for how the bank can mitigate the reasons for leaving. It is the bank's intention to keep their customers happy by proactively implementing these recommendations.

## Data Definitions

`BankChurners.csv`   - this file contains basic information about each client (10 columns)
> 
> `CLIENTNUM` - Client number. Unique identifier for the customer holding the account;
>- `Attrition Flag` - Internal event (customer activity) variable - if the client had churned (attrited) or not (existing).
>- `Dependent Count` - Demographic variable - Number of dependents
>- `Card_Category` - Product Variable - Type of Card (Blue, Silver, Gold, Platinum)
>- `Months_on_book` - Period of relationship with the bank
>- `Months_Inactive_12_mon` - No. of months inactive in the last 12 months
>- `Contacts_Count_12_mon` - No. of Contacts in the last 12 months
>- `Credit_Limit` - Credit Limit on the Credit Card
>- `Avg_Open_To_Buy` - Open to Buy Credit Line (Average of last 12 months)
>- `Avg_Utilization_Ratio` - Average Card Utilization Ratio

`basic_client_info.csv` - this file contains some basic client info per each client
(6 columns)
> 
> `CLIENTNUM` - Client number. Unique identifier for the customer holding the account
>- `Customer Age` - Demographic variable - Customer's Age in Years
>- `Gender` - Demographic variable - M=Male, F=Female
>- `Education_Level` - Demographic variable - Educational Qualification of the account holder (example: high school, college graduate, etc.
>- `Marital_Status` - Demographic variable - Married, Single, Divorced, Unknown
>- `Income_Category` - Demographic variable - Annual Income Category of the account holder (< 40K, 40K - 60K, 60K - 80K, 80K-120K, > 120K, Unknown)

`enriched_churn_data.csv` - this file contains some enriched data about each client -
(7 columns)
> 
> `CLIENTNUM` - Client number. Unique identifier for the customer holding the account
>- `Total_Relationship_Count` - Total no. of products held by the customer
>- `Total_Revolving_Bal` - Total Revolving Balance on the Credit Card
>- `Total_Amt_Chng_Q4_Q1` - Change in Transaction Amount (Q4 over Q1)
>- `Total_Trans_Amt` - Total Transaction Amount (Last 12 months)
>- `Total_Trans_Ct` - Total Transaction Count (Last 12 months)
>- `Total_Ct_Chng_Q4_Q1` - Change in Transaction Count (Q4 over Q1)


## Project Parts

- SQL Analysis
    - Using SQL to answer questions posed by the company to assist with churn recovery.
- Tableau Dashboard
    - An interactive dashboard explaing my bank churn analysis by demographics and credit card type.
- Deep Dive
    - An exploratory and explanatory Analysis using python libraries to better understand the problem, along with a few recommendations.
    - A distribution of each quantitative variable, as well as a sumamry of interesting insights.
    - A correlation analysis to further pinpoint the variables that contribute most to this problem.
    - After a thorough analysis I answered the following four questions:
        `Is there a Difference in Transaction Counts by Age Groups for CHURNED and EXISTING CUSTOMERS?`
        > **YES:**
        - Transaction counts do not exceed more than 50 for all attrited customers, across all age groups.
        - For existing Customers, the 40 - 50 age group makes the most transactions compared with all other age groups.

        `About 93% of all customers have the Blue Card. What is the distribution of blue card holders across age groups and gender?`
        > **The 40-50 age group make up most of the blue card holders for both genders.**
        > **The 30 and younger age group has the fewest blue card holders.**
        > **There are more female blue card holders than male blue card holders.**

        `What is the proportion of all customers by age group, and how does that compare with churned customers?`
        > **The 40-50 demographic make up almost 50% of all customers, and the 30 and Younger demographic makes up the smallest proportion of customers.**
        > **All demographics across all age groups hold the same rankings in the churned customer category.**

        `What is the distribution of card types by education level across all customers, and how does that compare with churned customers?`
        > **Most Blue card holders are in the Graduate demographic.**
        > **The second highest number of blue card holders are of the High School education level.**
        > **Both categories hold the same ranking in churned customers.**

## Conclusions 

#### There are others, but here is what stood out to me the most:

- **93 % of all customers have the Blue credit card. Making some demographic comparisons might shed some new insights on attrited customers.**
- **46 % of all customers are ages 40-50. Which peaks my interest for a number of reasons:**
	- **Is this because card benefits only appeal to this age group?**
	- **Is there a way to sell this product to the younger demographic?**
	- **ONLY 1% of all churned customers are of the 30 and Younger demographic, compared with the 40-50yr age group (48%). Perhaps appealing to this age group may improve churn rates.**
- A total of 41% of all customers have had some higher education. I would like to compare demographic information and see if perhaps a student card offering would appeal to more customers of a younger demographic. 
- **Income category also peaked my interest as well. 38% of all churned customers are in the less than 40K income category, and this same category makes up 37% of all customers.** 
- **The distribution of the number of products held by each customer also yielded some unexpected results. It is left-skewed, meaning the number of clients increases as the number of the products increases. The highest peak is at 5!**

#### Recommendations based on these findings:

> In short, a campaign to recover churned customers in your largest demographic (40 - 50 year-olds) would be recommended. 

> I would also suggest a campaign to appeal to younger age demographics, perhaps a student product or benefits that appeal to users in a lower income category.

> Recovering lost customers and attracting new customers would be an ideal strategy in reducing bank churn.
