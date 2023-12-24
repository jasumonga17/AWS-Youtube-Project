# AWS-Youtube-Project

**Commands Used** to install **AWS CLI**:
* Inside the terminal write: **aws**
* Enter **aws configure** and then enter your **Access Key ID** , **Secret Key ID** and **region** of the account.
* After this if we write: **aws s3 ls** this will give us all the s3 buckets.
* This will set the **AWS CLI**.

**Data Ingestion Process**
1. Utilized AWS CLI commands to seamlessly extract YouTube data sourced from Kaggle and transfer it into an Amazon S3 bucket, leveraging the power and flexibility of AWS cloud services for efficient data management.

2. Commands used:
* Create a S3 bucket de-on-youtube-raw-useast02-dev
* Navigate to the directory inside the terminal where data is stored.
* Now to move data to the bucket we will use: **aws s3 cp . s3://de-on-youtube-raw-useast02-dev/youtube/raw_statistics_reference_data/ --recursive --exclude "*" --include "*.json"** this command.

**AWS Glue Catalog-JSON files**  
1. Established an **AWS Glue catalog** by employing a crawler to automatically extract metadata from our dataset, setting the stage for effective Extract, Transform, Load (ETL) processes within the AWS ecosystem.
* So, inside the crawler formatting plays an important part.
    * Eg: JSON data needs to appear once per line.
    * Like this { “key” : 10 } , { “key” : 20 }
* Since the YouTube data is in that format we will use AWS lambda to write Python code inside that and convert the file into Apache Parquet

**AWS Lambda**
1. Conducted data pre-processing for JSON files using **AWS Lambda**, where Python code leveraging AWS SDK to seamlessly enhance and prepare the data for subsequent processing steps.
* If we want AWS Lambda to access the AWS S3 bucket we need to create a **role** for lambda to access it.
* In that permit **AMAzonS3FullAccess**
* The error we are trying to resolve is that in our JSON data, we have data in the array format instead of in the key-value pair format so we need to do pre-processing before we use crawler.

**AWS Glue-for CSV files**
1. Designed and implemented a robust ETL pipeline, seamlessly moving data from the source to the target, ensuring efficient data processing and transformation within the system.
* **AWS-Jobs**
* Created a visual ETL pipeline where data from the source moved to the target

<img width="338" alt="Screenshot 2023-12-23 at 7 11 45 PM" src="https://github.com/jasumonga17/AWS-Youtube-Project/assets/76562774/1bdb5d5a-4bfa-458b-9763-2185570d6769">

**AWS Athena**
Utilized **Athena** to execute SQL queries on our data, leveraging its serverless and interactive query capabilities for efficient and on-demand analysis

   
<img width="1356" alt="Screenshot 2023-12-23 at 2 41 24 PM" src="https://github.com/jasumonga17/AWS-Youtube-Project/assets/76562774/bb6375df-cf12-4cb1-b5b0-d1585e907e45">
