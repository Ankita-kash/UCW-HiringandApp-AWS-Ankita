# UCW-HiringandApp-AWS-Ankita
Automating hiring and appointment services at UCW using AWS
# Project objective
This project involves leveraging AWS services to optimize and streamline the hiring and appointment processes at University Canada West (UCW). The solution incorporates various AWS tools and technologies to address data management, automation, and security needs. The project focuses on creating a robust infrastructure for managing applicant data, automating workflows, and ensuring data protection and governance.
# Datasets
I had taken Offer acceptance and decline report where dataset consists of applicants information with accepted and declined status. It had details including:
- Offer ID: It consists of offer number.
- Candidate ID: Unique Identifier for each applicant
- Position Title - The title for the positions available in UCW.
- Department - Which department does the position title belongs to.
- Offer date - Date of posting
- Response dat - Date of responding for the position.
- Offer Status - Accepted or Declinded Status
- Reason for Decline - If declined, the reason for that.
- Start date - start date for the accepted offers
- Salary offered - Salary offered to the specific positions.
# Technologies Used
AWS Services: Amazon S3, AWS Glue, AWS GlueDatabrew, Amazon DynamoDB, AWS Athena, Quicksight, Dashboard, VPC, EC2, AWS KMS, AWS CloudWatch, CloudTrail, IAM.
# Architecture
![Architecture drawio](https://github.com/user-attachments/assets/227d1af5-8ad8-4b58-a642-0a78002c91ea)
# Methodology
1. Data Discovery - Identified and described the datasets with use of chatgpt in the form of excel sheet for different operations. For eg- I had worked on Job acceptance log in which i have exported data with the name of offer acceptance and decline log.
2. Data storage design and preparation - Outlined the data storage solutions implemented by using Amazon S3 for data storage and created a bucket 'hroffice-hirandapp-ankita' and stored the data and prepared for further steps of ingestion.
3. Data Ingestion and storage - I uploaded the datasets for 2023 and 2024 to different Amazon S3 files and described the configuration and management of data storage solutions.
4. Data Cleaning and structuring - Identified and corrected any errors, missing values, and inconsistencies to make sure that the data is correct and reliable for analysis and clean dataset in an order that makes it easy to query, analyse, and draw conclusions.
5. Data Pipeline Implentation - Set up the data pipeline that automates the entire ETL (Extract, Transform, Load) process and also makes sure that the dataset is always loaded, cleaned, structured, and saved for analysis.
6. Data analysis - I have used athena for further analysis of the data. For this service it directly access the database from S3 bucket and I used SQL queries to analyse and structure my data in alphabetical order so that it is easy to read.
7. Data Visualisation - I exported the results generated using Athena and SQL queries to turn it into a visual format in forms of charts. Analyzed the acceptance and decline rates across job positions and departments. Visualized the percentage of offers accepted and declined using bar and pie charts.
8. Data Publishing - I have created a general server using the service EC2. Later I used that server to publish my data on that server so that it is accessible to anyone who have the access to my server. People with access to the server can view the reports and data published on the server. I have also created a web server to publish my data so that people outside my company or stakeholders can access my data using the link to my web page which I have created using EC2 service.
9. Data Protection and security - I used KMS to generate an encryption key and I also configured key administrative and usage permissions to my choice and the method I used is SSE-KMS (Server-Side Encryption with AWS KMS). Then, I used this key to encrypt my bucket by going into the properties of my bukcet and choosing the key I generated under the option of default encryption.I have turned on the replication rule to ensure that data is safe and available at different locations and readily available just in case we need that data to recover from a security event to reduce the time under business interruption. I used Visual ETL to work on my data. I uploaded my dataset and user functions like Detect Sensitive Data, and applied an action to redact any sensitive data, if found. I also used other function Evaluate Data Quality and I checked if my data is complete using a rule type called Completeness. Then I created a workflow to automate my ETL procedure by adding a trigger to make sure that my data remain in compliance and should be well structured. I have used CloudWatch to track the charges that have been applied to the service S3 that I use to store my data. I created a dashboard and added a widget to track my charges for S3 and this monitoring will refresh every 6 hours as selected. And I have also added another widget to track the number of objects that I have in my bucket. Besides this, I added an alarm on my CloudWatch dashboard so that it will notify me if I have reached my set limit of $35 for the charges for S3. I also used CloudTrail to design a trail to the activity of the users. It logs every action taken by users, whether they are making changes to the data or are taking actions like creation and deletion of data.
# Insight and Findings
1. Offer Acceptance Rates - Majority of the job offers were accepted in the departments with higher compensation and benefits. Lower acceptance rates were observed in entry-level positions, suggesting a mismatch in expectations.
2. Time to offer response - Candidates who accepted offers responded within a shorter time window compared to those who declined, indicating faster decisions when an offer is attractive.
# Recommendation
1. Enhance Communication: Provide clearer communication about job role expectations and benefits to reduce declines, especially for entry-level roles.
2. Targeted Offer Strategies: For roles with high decline rates, consider adjusting salary packages or offering additional perks to improve acceptance rates.
# Deliverables
A concise, visual presentation that highlights the key findings (acceptance trends, decline causes), and offers recommendations for improving the hiring and offer process.
This presentation is designed for HR managers and decision-makers to help them take immediate actions based on the insights.
Bar charts, and pie charts are used to make the data easy to understand and act upon.
