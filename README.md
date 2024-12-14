<h1 align="center">AWS Project 2</h1>


# Project Description: Data Protection, Governance, and Monitoring
* This project involves setting up a comprehensive data analytics platform using AWS services to manage the City of Vancouver’s animal control data. 
## Project Title: AWS Data Analytic Platform for the City of Vancouver - Part 2
* This project involves setting up a comprehensive data analytics platform using AWS services to manage  to give a better protection on data monitoring and enriching the City of Vancouver’s animal control data. 
## Project Objective:
* This project aims to design and implement a Data Analytics Platform (DAP) using Amazon Web Services (AWS) to Data Enriching, Data Protection, Governance, and Monitoring
## Methodology:
* The process of providing Data Enriching, Data Protection, Governance, and Monitoring for DAP designed as follows.
### 1. Data Enriching
- The main purpose of this phase was to maintain data security within the AWS S3 client environment. The following screenshots describe main security settings like Bucket Policies and Encryption, Replication that enhances the secure data management on the platform.

![Screenshot (184)](https://github.com/user-attachments/assets/e932c86d-d5f6-4f89-aedd-b7e99936b357)



- Data Enriching is the process of making raw data more valuable, effective or better which can be done by incorporating attributes from internal as well as external sources. Data mining is especially important in business as it is helpful for data analysis in the different sectors including marketing and business intelligence.
Figure: Database creation for Data Enriching.


Figure: Crawler Creation for Data Enriching.  

![Screenshot (185)](https://github.com/user-attachments/assets/cb440508-7282-4f6d-b8e7-09d4fcafaf33)

Figure: Athena for Serverless Interactive Analytics Services.

![Screenshot (179)](https://github.com/user-attachments/assets/2581731e-f61d-4a63-aa37-f4a9a62d0db2)


### 2. Data Protection
- The main purpose of this phase was to maintain data security within the AWS S3 client environment. The following screenshots describe main security settings like Bucket Policies and Encryption, Replication that enhances the secure data management on the platform.

1. 	In this setup, a new key was created to create extra security measure using AWS Key Management Service (KMS). The NAME of the key created on AWS is “grp6-prt2-anmlcnvin-lstfnd-kms-karthik it is a SYMMETRIC type and is designed to perform the ENCRYPTION and DECRYPTION within the confines of the AWS. This key will serve a lot of importance in keeping secured the data placed in AWS S3.

![Screenshot (174)](https://github.com/user-attachments/assets/1d7a7215-3f92-4d17-835d-30e7f93f51c8)

The following screenshots show basic steps in setting up protection of an S3 bucket on AWS using encryption and replication capabilities.
2. Encryption: 
 	By default, the S3 bucket has server-side enforcement of encryption of data at rest with AWS Key Management Service (KMS). Data protection at rest is achieved with the help of an encryption key that KMS uses in order to encrypt data. The last figure in the right corner of the heading Illustrates that a KMS key (ARN) belongs to the bucket and show that the bucket key is enabled to minimize costs through minimizing Encryption requests to AWS KMS. It ensures protection of sensitive data, and addresses compliance standards.

![Screenshot (177)](https://github.com/user-attachments/assets/73478084-5753-422a-bf1d-3eff670f1cf0)


3.	Replication: 
 	They have set up a replication rule that would create an asynchronous copy of the objects from a source bucket to another different destination bucket within the same region of US East. Replication helps to make data copies, which leads to a feature known as high availability, and the overlapping also makes copies, and is termed as redundancy. It applies to the whole bucket, and replicating objects encrypted using SSE-KMS uses the same KMS key. Another advantage of replication is to produce a second copy of the data simply to use in case of disaster.

![Screenshot (176)](https://github.com/user-attachments/assets/119c2ef4-96a1-483d-9b3e-f37866c6f8bb)


4.	Versioning:
When enabled, S3 versioning enables the creation of many versions of an object within a single bucket in order to retain, recall, and restore each version of an object that replaced by or eliminated by other versions. When versioning is on, one can always get a previous version of the object despite the fact that it has been deleted or perhaps altered, which of course offers another extra layer of security to accidental data deletion or modification. This is especially true when several files must be edited now and then.
SSE-KMS besides replication and versioning increases the durability of data. When used together with replication, it makes not only the current versions of the objects stored in the bucket replicated to the destination bucket but also the previous versions of an object.

![Screenshot (175)](https://github.com/user-attachments/assets/997656ae-1b4e-4aed-9e23-5f27cab7526f)




### 3. Data Governance
- To achieve better data management and data availability I created a data pipeline with AWS Glue and S3. The pipeline starts with data accumulation in an S3 bucket and contains stages for the identification of, for instance, personal information. It then assesses the quality of the data thus improving on the quality of the data gathered for integrity. A row-level transformation is turned on to change the data then a conditional router filters the data according to set conditions. Specific columns not relevant for judgments are deleted by altering the scheme so that only relevant data is stored.

![Screenshot (180)](https://github.com/user-attachments/assets/56215053-087e-4715-8ef7-ef6f2f0d9051)



Then, the processed data is transferred and stored in the Trusted folder in S3 for further use.

![Screenshot (181)](https://github.com/user-attachments/assets/0e5593c7-14bb-44f8-9df6-91a52ce292c9)



### 4. Data Monitoring

- In general, the ability to monitor data adequately is important to determine system status and utilization rates. The examples of the screenshots imply use of Amazon CloudWatch to customize dashboard which in turn help in monitoring and controlling the performance of systems.


![Screenshot (182)](https://github.com/user-attachments/assets/a18f7160-f83f-46f0-a564-1d512319420c)



-The CloudWatch dashboard, named " grp6-prt2-anmlcnvn-lstfnd-DAP_DASH-karthik" includes:
 •	Estimated Charges: Features a meter which shows the current estimates of costs.
 •	Number of Objects: Mostly contains a graph to describe the count of objects over time.
 •	Bucket Size in Bytes: It clears an understanding to depict the size of the bucket in byte so that it will be convenient to mention about the storage usage.
 •	Alam: An alarm named “grp6-prt2-anmlcnvn-lstfnd-alarm-karthik” is raised for certain limit like number of objects or even estimated charges. This means that beyond the limits, the system has a capacity to send an email alert to encourage active monitoring.


![Screenshot (183)](https://github.com/user-attachments/assets/fabae73b-99d9-4c92-9a04-7561e6c4213e)




- Additionally, AWS Glue job monitoring is depicted, summarizing job runs with details such as:
•	Total Runs: One job executed, with One successful run.
•	Run Success Rate: 100% success rate.
•	Resource Usage: The graphical display of resource use over time for the purpose of identification and analysis.

