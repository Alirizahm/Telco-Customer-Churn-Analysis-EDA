## Telco Customer Churn Analysis with EDA

Author's : Aliriza Hamonangan Matondang 

## Introduction
Telco Customer Churn data are composed of 7043 rows and 21 columns which are related to each other. Each customer or customer ID has 21 data within each column in which from each data we are able to see the pattern of each customer. It is because there are some similarities and differences based on gender, senior citizen, etc with churn in Telco Customer Churn Data. Here I would like to analyse churn relasionships with every variables, and make an EDA every Data Exploration

## Data Information
- CustomerID : Contains customer ID
- Gender: Are the customers female or male?
- SeniorCitizen : Whether the customer is a senior citizen or not (1, 0)
- Partner : Whether the customer has a partner or not (Yes, No)
- Dependents : Whether the customer has dependent or not (Yes, No)
- Tenure : The number of months the customer has subscribed to the company
- PhoneService : Whether the customer subscribes to PhoneService or not (Yes, No)
- MultipleLines : Whether the customer subscribes to MultipleLines or not (Yes, No, No no telephone service)
- InternetService : Customer internet service provider (DSL, Fiber optic, No)
- OnlineSecurity : Whether customer subscribes to OnlineSecurity or not (Yes, No, No no internet service)
- OnlineBackup : Whether the customer subscribes to OnlineBackup or not (Yes, No, No no internet service)
- DeviceProtection : Whether the customer subscribes to DeviceProtection or not (Yes, No, no internet service)
- TechSupport : Whether the customer subscribes to TechSupport or not (Yes, No, No internet service)
- streamingTV : Whether the subscriber (customer?) subscribes to streamingTV or not (Yes, No, No internet service)
- streamingMovies : Whether the subscriber subscribes to streamingMovies or not (Yes, No, no internet service)
- Contract : Customer contract term (Month-to-month, One year, Two years)
- PaperlessBilling : Whether the customer subscribes to PaperlessBilling or not (Yes, No)
- PaymentMethod : Customer payment method (electronic check, postal check, bank transfer, Credit Card)
- MonthlyCharges : Monthly bills charged to customers
- TotalCharges : Total billing charged to customers is calculated to the end of the determined quarter
- Churn : Whether the customer churn or not (Yes or No) Whether the customer churn or no (Yes or No)

## The variable target
![download](https://user-images.githubusercontent.com/92624520/145713606-bff54c55-0746-4528-a5e3-d9d7d8ff87c0.png)

The variable target of this analysis is Churn. From the Churn column plot, it can be seen that 73.5% of customers remain under the service and 26.5% of customers opt-out of service or do not resubscribe.

## Correlation test
![download (2)](https://user-images.githubusercontent.com/92624520/145713842-d2b8c37c-4712-48d8-9a78-f74efb86ca12.png)

Findings:
- Customers with month-to-month contracts are more likely to discontinue their subscription (Churn Yes)
- Customers who do not use services such as OnlineSecurity, TechSupport, OnlineBackup, and DeviceProtection are more likely to discontinue their subscription (Churn Yes)
- Customers who use the Electronic check payment method are more likely to discontinue their subscription (Churn Yes) when compared to other payment methods
- Customers who choose the Fiber Optic internet service are more likely to discontinue the subscription (Churn Yes) which indicates that the Fiber Optic internet service is not very good
- The tenure variable has a negative correlation closest to -1 compared to other variables, which means that the higher the tenure value, the lower the possibility that the user will discontinue the subscription (Churn Yes)
- When we check Contract variable, customers who choose one and two years contracts have a negative correlation with the Churn variable so that, same with the tenure variable, customers who have long-term subscriptions are loyal customers and the possibility of users discontinue their subscriptions (Churn Yes) is getting lower
- Customers who do not have internet service but have certain services such as OnlineSecurity, TechSupport, OnlineBackup, StreamingMovies, StreamingTV, and DeviceProtection, the possibility of the user discontinue the subscription (Churn Yes) is getting lower
## Checking the Churn variable relationship with every variables
#### Checking the Churn variable relationship with variables that are similar or related to each other (gender, SeniorCitizen, Partner, and, Dependents)
![download (3)](https://user-images.githubusercontent.com/92624520/145714021-9a29715b-d6eb-4026-8b10-9a09ad39fb42.png)

Findings:
- When we check all of the relationships among the Churn variable and gender, Senior Citizens, Partners, and Dependents have appropriate results with the correlation test
- For the gender variable, indicates a similarity between female and male customers who have discontinued subscribing (Churn Yes) but percentage of female who discontinue subscribing (Churn Yes) is higher than male. However, for these variables, they have a similar percentage and similar correlation are close to 0 
- For the SeniorCitizen variable, it has the highest percentage of subscribers who are not SeniorCitizens who continue to subscribe. However, customers who are Senior Citizens may not continue to subscribe (Churn Yes) because the percentage of Senior Citizens who remain subscribed has a percentage that is close to Senior Citizens who discontinue to subscribe (Churn Yes)
- Customers who do not have both partners and dependents are more likely to discontinue the subscription (Churn Yes). However, for this variable, customers who do not have both partners and customers without dependents have a higher percentage of users who continue to subscribe, but for those who do not continue to subscribe has a fairly high percentage

#### Checking the Churn variable relationship with variables that are similar or related to each other (PhoneService, MultipleLines, InternetService, OnlineSecurity, OnlineBackup, DeviceProtection, TechSupport, StreamingTV, and StreamingMovies)
![download (4)](https://user-images.githubusercontent.com/92624520/145714263-2920f82c-93bf-4972-ae20-3c958bbf2bd6.png)

Findings:
- There are very few customers who choose not to use the PhoneService and the percentage is not significantly different between subscribers who continue to subscribe and those who do not continue to subscribe
- The MultipleLines service has the same percentage of customers who discontinue subscribing (Churn Yes) for customers who use and do not use the service
- Fiber Optic internet service has a high percentage of customers who do not continue to subscribe (Churn Yes), which indicates that the service is not good
- Customers who do not use services such as Online Security, Tech Support, Online Backup, and Device Protection are more likely to discontinue their subscription (Churn Yes) which means that these services may affect customers to continue to subscribe (Churn No)
- Customers who do not use both Streaming TV and Streaming Movies services have a high percentage in which the customers are more likely to discontinue subscribing (Churn Yes). However, if we carried out to re-rechecking, customers who choose to use these services but do not continue to subscribe (Churn Yes) also have a similar percentage with customers who do not use the service and do not continue to subscribe (Churn Yes) 

#### Checking the Churn variable relationship with the PaperlessBilling variable
![download (5)](https://user-images.githubusercontent.com/92624520/145715902-d1f91b8f-5f40-4955-90fb-92c22a33a366.png)

Findings:

In the PaperlessBilling variable, customers who use Paperless Billing have a high percentage of not continuing to subscribe (Churn Yes) when compared to customers who do not use Paperless Billing

#### Checking the Churn variable relationship with PaymentMethod variable
![download (10)](https://user-images.githubusercontent.com/92624520/145720152-7768dcb1-01ca-4604-a1ed-366fb7e18baa.png)

Finding:

In the variable PaymentMethod, customers who choose the electronic check payment method are more likely to discontinue subscribing (Churn Yes) and are the highest percentage of other payment methods that do not continue to subscribe

### Checking the Churn variable relationship with the Contract variable, and MonthlyCharges
![download (11)](https://user-images.githubusercontent.com/92624520/145720232-6ce2964e-35a1-48d2-8164-1adced47d0cd.png)

Finding:

In the contract variable relationship, and monthly billing with Churn, it can be seen that the contracts of customers who discontinue subscriptions have a higher average monthly bill than customers who continue to subscribe in each available contract

### Checking the Churn variable relationship with the Total Charges, tenure, and MonthlyCharges variables
![download (3)](https://user-images.githubusercontent.com/92624520/145718466-45473181-dae9-497b-92ed-c1ce9710277b.png)

Finding:
- Customers who do not continue to subscribe have a low average tenure value. It indicates that customers tend to be quick to decide not to continue subscribing
- Customers who discontinue subscriptions have a higher average Monthly Charges value than customers who continue to subscribe, However, when we look at the TotalCharges value, customers who discontinue subscriptions have a lower TotalCharges average value. Thus, it can be seen that customers who do not continue to subscribe are in accordance with the average tenure value so that the average value of TotalCharges is low

## Outliers analysis of TotalCharges and Churn
### Checking the outliers variable relationship with the Total Charges, tenure, and MonthlyCharges variables
![download (4)](https://user-images.githubusercontent.com/92624520/145718549-dbf85e8f-a166-4188-ab34-8e9d0a00c952.png)

Finding:

It is better not to use these outliers for further analysis because the value of the Churn yes percentage is small, so these outliers can also be used as a reference if you want to do an analysis related to the Churn variable. There are 109 customers who choose not to continue the service and these customers are customers with high tenure values, Monthly Charges, and high Total Charges. It indicates that the customer is an average old customer

### Checking the outliers variable relationship with every categorical variable
![download (7)](https://user-images.githubusercontent.com/92624520/145718644-73cdda24-7d58-4c7a-aa2c-98031405435e.png)

Finding:
- All customers who choose to discontinue, on average they choose other services and have high scores, only on TechSupport and OnlineService services, the average customer does not choose these services
- In the variable Contract, the 1-Year contract is mostly chosen by customers who choose to leave the service
- WHan we check the highest value, it can be found in the Phone Service variable in which all customers choose to use the Phone Service service, the lowest value is in the DSL variable

## Conclusion
- Customers prefer to continue the service than to discontinue service. So the customer are loyal customers
- Customers who do not have internet service but have certain services such as OnlineSecurity, TechSupport, OnlineBackup, StreamingMovies, StreamingTV, and Device Protection are less likely to continue the subscription (Churn Yes)
- A strong influence in which customers decide not to continue subscribing is in month-to-month contracts, customers who do not use services such as OnlineSecurity, TechSupport, OnlineBackup, and DeviceProtection are more likely to terminate the subscription (Churn Yes) Monthly Charges, PaperlessBilling_yes, Check PaymentMethod_Electronic and InternetService_Fiber optic
- Outliers of the relationship between Churn and TotalCharges can be used as a reference for further analysis
- The high percentage value of customers discontinuing subscriptions on Internet Service_Fiber optics indicates that the inter fiber optic service is not good enough. In result, giving customers a bad initial impression, thus causing a small average tenure value for customers who decide not to continue subscribing
