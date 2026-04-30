# Analysis for an Insurance Company

## A report on the Fraud Analysis of Claims from customers of an Insurance Company 

### Project Overview & Background
This project analyzes the claims of Ubuntu Insurance Ltd. who is facing:
- Increasing claim costs
- Suspected fraudulent claims
- Low customer retention

 The tools used:
- SQL (Databricks)
- Power BI (Dashboard)
- Power Point (Presentation)

Data Exploration Questions
The Following questions were answered in the data exploration notebook:
- Total number of customers 
- Total number of policies 
- Total number of claims 
- Total claim amount 
- Claims by policy type 
- Average claim amount per policy type 
- Number of fraud vs non-fraud claims 
- Top 5 highest claim amounts 
- Claims per location 
- Claims trend over time 

Dashboard and Insights
A Power BI Dashboard was built to visualize and summarize the insights from the cleaned table dataset
Dashboard Link: https://app.powerbi.com/viewr=eyJrIjoiYTAyNTg0MDYtNDJhZi00ZmY0LTk2N2MtMDlhNWZiMGUxMjNiIiwidCI6IjczNjVmODNhLWViY2UtNGM5ZS1iYTI2LWY5ZjM5ZmZhYTk4ZSJ9
![](Presentation%20Assets/Customer%20Risk%20%20Claims%20Analysis%20for%20an%20Insurance%20Company-1.png)

Insights were drawn mainly from these questions:
- What trends do you observe?
- Which policy type is most risky?
- Where is fraud most common?
- Which customers or segments are high-risk?

### Dataset Structure
The dataset was a CSV that has 15 columns that are all in the format of a string.

### Data Cleaning
The dataset that was ingested on Databricks is cleaned in a separate SQL notebook and it creates a new cleaned dataset.

The dataset was initially very messy, presenting issue such as:
- Missing values
- Blank values
- Text casing inconsistencies
- Unnecessary spaces
- Inconsistent date formatting
- Inconsistent numeric formatting
- Inconsistent data types
- Redundant naming such as different terms with same meaning

Customer_ID cleaning:
- Removed unnecessary spaces

Gender cleaning:
- Removed unnecessary spaces
- Replaced missing values
- Standardized the values

Age cleaning:
- Removed unnecessary spaces
- Changed data type to INT

Province cleaning:
- Removed unnecessary spaces
- Replaced missing values
- Standardize the missing values

Monthly_Income cleaning:
- Removed unnecessary spaces
- Replaced missing values
- Standardized the values
- Change data type to DOUBLE

Join_Date cleaning:
- Removed unnecessary spaces
- Standardized the values
- Changed data type to DATE

Policy_ID cleaning:
- Removed unnecessary spaces

Premium_Amount cleaning:
- Removed unnecessary spaces
- Replaced missing values
- Standardized the values
- Changed data type to DOUBLE

Policy_Status cleaning:
- Removed unnecessary spaces
- Standardized the values

Claim_ID cleaning:
- Removed unnecessary spaces

Claim_Date cleaning:
- Removed unnecessary spaces
- Standardized the values
- Changed data type to DATE

Claim_Amount cleaning:
- Removed unnecessary spaces
- Replaced missing values
- Standardized the values
- Changed data type to DOUBLE

Claim_Status cleaning:
- Removed unnecessary spaces
- Standardized the values

Fraud_Flag cleaning:
- Removed unnecessary spaces
- Standardized the values
- Replaced missing values

The cleaned table is created and displayed with it’s appropriate data types.

Invalid data handling:
- Remove data where the Customer_ID is blank
- Remove data where the Age of the Customer is under 18

### Data Exploration
The insurance dataset was uploaded onto Databricks and was processed using SQL in a notebook.
The dataset was used to create a table in a database using SQL.

## Insights
Total number of customers
- Total number of customers is 518 customers

Total number of policies 
- Total number of policies is 520 policies 

Total number of claims 
- Total number of claims is 547 claims

Total claim amount 
- Total Claim Amount is R12 578 657.02

Claims by policy type 
- Home policy has 94 claims
- Auto policy has 128 claims
- Health policy has 134 claims
- Motor policy has 10 claims\
- Life policy has 105 claims
- Funeral policy has 68 claims
- Medical policy has 5 claims
- Property policy has 3 claims

Average claim amount per policy type 
- Funeral policies claimed R14198.58
- Home policies claimed R25467.26
- Medical policies claimed R17714.30\
- Motor policies claimed R14929.18
- Health policies claimed R12234.46
- Life policies claimed R45518.10
- Auto policies claimed R19049.83
- Property policies claimed R20201.64

Number of fraud vs non-fraud claims
- 79 fraudulent claims
- 471 non-fraudulent claims

Claims per location 
- Gauteng has 64 claims
- Limpopo has 47 claims
- Eastern Cape 75 claims
- North West has 72 claims
- Free State has 72 claims
- Mpumalanga has 55 claims
- Western Cape has 75 claims
- KwaZulu-Natal has 90 claims

Top 5 highest claim amounts
- CUST1050 claimed R143857.60
- CUST1324 claimed R115579.76
- CUST1429 claimed R97527.12
- CUST1425 claimed R92918.98
- CUST1068 claimed R89909.74

Claims trend over time
Claims over time has mainly single claims with a few multiple claims on some dates. Considering that there are dates with multiple claims, we could say that the claims are increasing on an upward trend overtime.

What trends do you observe?




All claims
<table>
  <tr>
    <th align="center">All Claims</th>
    <th align="center">Fraudulent Claims</th>
  </tr>
  <tr>
    <td><img src= Presentation%20Assets/1(1).png width="200"></td>
   <td><img src= Presentation%20Assets/1(3).png width="200"></td>
  </tr>
  <tr>
    <td><img src= Presentation%20Assets/1(2).png width="200"></td>
    <td><img src= Presentation%20Assets/1(4).png width="200"></td>
  </tr>
</table>
Claims have been on a downward trend in general but the fraudulent claims have been increasing on an upward trend over time along with the claim amount.

Which policy type is most risky?
<table>
  <tr>
    <td><img src= Presentation%20Assets/2%20v2%20(1).png width="100%"></td>
    <td><img src= Presentation%20Assets/2%20(2).png width="100%"></td>
  </tr>
</table>
Life policy is most risky as it has 18 claims with that being the highest claim amount of R970,90k in total, 8 of the claims being approved to the amount of R531,48k.

Where is fraud most common? 
<table>
  <tr>
    <td><img src= Presentation%20Assets/3.png width="100%"></td>
  </tr>
</table>
Fraud is most common in KwaZulu-Natal as it has 14 fraudulent claims to the amount of R403,27k

Which customers or segments are high-risk?
High-Risk Customers
<table>
  <tr>
    <td><img src= Presentation%20Assets/4.png width="100%"></td>
  </tr>
</table>
- CUST1324 claimed 2 times to the amount of R115,58k
- CUST1415 claimed 1 time to the amount of R80,06k
- CUST1119 claimed 1 time to the amount of R73,93k
- CUST1136 claimed 1 time to the amount of R70,42k
- CUST1504 claimed 1 time to the amount of R63,46k
- CUST1220 claimed 1 time to the amount of R61,24k
- CUST1336 claimed 1 time to the amount of R58,79k

High-Risk Segments
<table>
  <tr>
    <td><img src= Presentation%20Assets/4(2).png width="100%"></td>
  </tr>
</table>
- Life policy has 18 claims to the amount of R970,90k
- Home policy has 20 claims to the amount of R587,02k
- Auto policy has 12 claims to the amount of R292,31k
- Funeral policy has 15 claims to the amount of R246,40k
- Health policy has 11 claims to the amount of R150,80k

### Recommendations
- Lower the claim amount of each high-risk segment to discourage customers from doing fraud.
- To improve customer retention, it is best to target customers within the age range of 30 years to 50 years and to target males and females earning a monthly income of around R28k.
- Make an adjustment to the premiums by increasing them to improve profitability.
