# AWS-Youtube-Project

**Commands Used** to install **AWS CLI**:
* Inside the terminal write: **aws**
* Enter **aws configure** and then enter your **Access Key ID** , **Secret Key ID** and **region** of the account.
* After this if we write: **aws s3 ls** this will give us all the s3 buckets.
* This will set the **AWS CLI**.


**Data Ingestion Process:**
1. Utilized AWS CLI commands to seamlessly extract YouTube data sourced from Kaggle and transfer it into an Amazon S3 bucket, leveraging the power and flexibility of AWS cloud services for efficient data management.

2. Commands used:
* Create a S3 bucket de-on-youtube-raw-useast02-dev
* Navigate to the directory inside the terminal where data is stored.
* Now to move data to the bucket we will use: **aws s3 cp . s3://de-on-youtube-raw-useast02-dev/youtube/raw_statistics_reference_data/ --recursive --exclude "*" --include "*.json"** this command.

For **CSV files**:
# To copy all data files to their location, follow Hive-style patterns:

aws s3 cp CAvideos.csv s3://de-on-youtube-raw-useast02-dev/youtube/raw_statistics/region=ca/

aws s3 cp DEvideos.csv s3://de-on-youtube-raw-useast02-dev/youtube/raw_statistics/region=de/

aws s3 cp FRvideos.csv s3://de-on-youtube-raw-useast02-dev/youtube/raw_statistics/region=fr/

aws s3 cp GBvideos.csv s3://de-on-youtube-raw-useast02-dev/youtube/raw_statistics/region=gb/

aws s3 cp INvideos.csv s3://de-on-youtube-raw-useast02-dev/youtube/raw_statistics/region=in/

aws s3 cp JPvideos.csv s3://de-on-youtube-raw-useast02-dev/youtube/raw_statistics/region=jp/

aws s3 cp KRvideos.csv s3://de-on-youtube-raw-useast02-dev/youtube/raw_statistics/region=kr/

aws s3 cp MXvideos.csv s3://de-on-youtube-raw-useast02-dev/youtube/raw_statistics/region=mx/

aws s3 cp RUvideos.csv s3://de-on-youtube-raw-useast02-dev/youtube/raw_statistics/region=ru/

aws s3 cp USvideos.csv s3://de-on-youtube-raw-useast02-dev/youtube/raw_statistics/region=us/
   


   



<img width="1356" alt="Screenshot 2023-12-23 at 2 41 24 PM" src="https://github.com/jasumonga17/AWS-Youtube-Project/assets/76562774/bb6375df-cf12-4cb1-b5b0-d1585e907e45">
