# Salesforce-DragonVariety-Project
(The Project includes system integration, data cleaning &amp; syncing, workflow design, system customization and so on.)
## 1. Project Overview
The project aims to play a key role in the business operation, and the business owner had a great expectation of what it can achieve. Before utlizing the CRM system, the company only
had an inventory management system, and required a customer management system to efficiently manage customers efficiently and serve them in a higher standard.
Based on the context, the goal of integrating Salesforce into the business includes data management, business operation support, sales management, customer management and so on.

## 2. Tools and Technology
### System Configuration
Salesforce Org, Sales Cloud, Salesforce Maps, Microsoft Outlook, Sandbox,etc.
### Data Management and Synchronization
Data Loader, Excel, Tableau, Zapier,Python,etc.
### Business Operation Support
Flow, Reports, Email2Case, Web2Case, Chatter, etc.

## 3. Business Pain Points and Solution
#### Challenge 1
Currently all the business data is in another system, the sales supervisor required data to be synced into Salesforce, and Sync order and customer data in real time.
#### Solution 1
Use Data loader to import original data, then use zapier to link two different systems
<img width="1919" height="902" alt="image" src="https://github.com/user-attachments/assets/c91dc916-1685-4abc-b3eb-bf88f498c6e7" />
<img width="1920" height="891" alt="image" src="https://github.com/user-attachments/assets/342a30ac-8523-4a83-9317-6b8850598f50" />


#### Challenge 2
Sales Supervisor needs to make routine for the team and check sales situation everyday, and requires visualizing store classification according to 'last order date time' rather than
static index like industry classification.
#### Solution 2
Create a text field on the account object and map the CreatedDate field of order (in descending order) to get the last order date time by using FLOW. 
Edit Marker Layer on the Salesforce Map and use account object, filtering by the last order date time field.
<img width="1908" height="906" alt="image" src="https://github.com/user-attachments/assets/20e01dd2-d7fb-4bdc-822f-fcafeaabb29b" />
<img width="1925" height="907" alt="image" src="https://github.com/user-attachments/assets/ad314b38-f15f-42e8-9a21-5c14437248bd" />


#### Challenge 3
It's difficult for sales team to find important communication emails in the Emailbox, the supervisor required linking email to Salesforce, so the team can view all the email communication
with a customer on the same page.
#### Solution 3
Transfer email service from foxmail to Microsoft Outlook, then connect email accounts with Salesforce Org.
<img width="1902" height="887" alt="image" src="https://github.com/user-attachments/assets/c15b7499-c387-4527-ac94-98a458dabaa5" />


#### Challenge 4
New accounts are synced from new customers in another system. Therefore, some related information is missing, further influencing the email sync.
#### Solution 4
Create FLOW to automatically create contacts once a new account is created, ensuring the email records to be synced.
<img width="1921" height="909" alt="image" src="https://github.com/user-attachments/assets/15723484-f854-45e2-bbca-d97e22e0582c" />


#### Challenge 5
Leads are generated in multiple channels including online and offline and need to be classified and followed up in time.
#### Solution 5
Create different Record Types for Leads, assign corresponding page layouts to the record type, and create different list for demonstrating different types of leads.
In addition, create a FLOW with Email Alert to send welcome letter to the email address of the leads.
<img width="1916" height="907" alt="image" src="https://github.com/user-attachments/assets/065c46c6-570d-42ec-994f-37b5b73beb9f" />
<img width="1655" height="805" alt="image" src="https://github.com/user-attachments/assets/73a4132a-dfb9-4117-b0a6-a7be9bd027cb" />
<img width="1912" height="906" alt="image" src="https://github.com/user-attachments/assets/a7bbb611-693b-49cf-bfa1-8649cd89f1d7" />


#### Challenge 6
Usually regular customers contact sales team once they need something urgently, but sales are unable to answer calls or messages in time due to scattered working time.
Therefore, the sales supervisor required a solution to hook customers' enquiry and respond to them instantly.
#### Solution 6
Designed a flyer and add an QR code on the flyer. When sales visited customers'store, they distributed flyers and introduce its function. When customers needed, they could 
simply scan the QR code and fill in the form. From the backend, we used web2case to automatically generate cases when customers fill in the information
<img width="1851" height="1065" alt="image" src="https://github.com/user-attachments/assets/00901d7e-aeb4-4e93-9b48-949520621d10" />
<img width="2244" height="1043" alt="image" src="https://github.com/user-attachments/assets/e8a5d454-e1b4-49e4-9860-a7ad127b161b" />


#### Challenge 7
The sales team wanted to try placing orders directly in the Salesforce system, during the test, some issues were found such as missing price book, missing products photos, and so on.
#### Solution 7
##### Update Price books by using Data Loader (Update Price Book Entry)
##### Upload Product Images by using ContentVersion and ContentDocumentLink.
##### Utilize Sandbox to test place order inside the system through integrating with Pappasales.
<img width="1902" height="1176" alt="image" src="https://github.com/user-attachments/assets/c8eff29d-c11d-450f-8e6a-c07ffe8b7b9c" />

