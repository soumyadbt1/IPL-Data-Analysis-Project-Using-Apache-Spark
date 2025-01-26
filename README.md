# IPL-Data-Analysis-Project-Using-Apache-Spark
This project is mainly aimed at using AWS S3 and Apache Spark on Databricks to do data analysis on IPL Data.

### Tools and Services Used:
1. AWS S3
2. IAM User
3. Azure Key Vault
4. Azure Databricks

### Dataset Used :
This is a Kaggle Dataset of IPL which comprises of 5 set of files
  - Ball by Ball.csv 
  - Match.csv
  - Player_match.csv
  - Player.csv
  - Team.csv
![Image](https://github.com/soumyadbt1/IPL-Data-Analysis-Project-Using-Apache-Spark/blob/main/Snapshots/Dataset%20used.JPG)

https://github.com/soumyadbt1/IPL-Data-Analysis-Project-Using-Apache-Spark/tree/main/Data

### STEPS FOLLOWED :

1. Uploaded all CSV files to S3 bucket.

   ![Image](https://github.com/soumyadbt1/IPL-Data-Analysis-Project-Using-Apache-Spark/blob/main/Snapshots/Upload%20to%20S3.JPG)

   ![Image](https://github.com/soumyadbt1/IPL-Data-Analysis-Project-Using-Apache-Spark/blob/main/Snapshots/Data%20on%20S3.JPG)

2. Created an IAM user, granted S3 bucket access to it, also generated access key for the user.

   ![Image](https://github.com/soumyadbt1/IPL-Data-Analysis-Project-Using-Apache-Spark/blob/main/Snapshots/created%20a%20IAM%20user%20with%20access%20key.JPG)

3. Logged in using the user and checked for S3 access :
   
   ![Image](https://github.com/soumyadbt1/IPL-Data-Analysis-Project-Using-Apache-Spark/blob/main/Snapshots/logged%20in%20via%20the%20user%20and%20access%20S3.JPG)

4. Used Azure Key Vault to store the secrets of Access Key :

   ![Image](https://github.com/soumyadbt1/IPL-Data-Analysis-Project-Using-Apache-Spark/blob/main/Snapshots/Key%20Vault%20to%20Store%20the%20AWS%20user%20access%20keys.JPG)

5. Created databricks secret scope to use azure key vault secrets and also used those secret scope in spark cluster config :

   ![Image](https://github.com/soumyadbt1/IPL-Data-Analysis-Project-Using-Apache-Spark/blob/main/Snapshots/Created%20Secret%20Scope%20on%20DB.JPG)

   ![Image](https://github.com/soumyadbt1/IPL-Data-Analysis-Project-Using-Apache-Spark/blob/main/Snapshots/Used%20the%20secret%20scope%20in%20Cluster%20config.JPG)

6. Made connection to S3 bucket via Azure Databricks by loading data to dataframe

   ![Image](https://github.com/soumyadbt1/IPL-Data-Analysis-Project-Using-Apache-Spark/blob/main/Snapshots/Loaded%20Data%20into%20DF.JPG)

7. Then all of the remaining transformation and analysis spark code is in the below python script.

   https://github.com/soumyadbt1/IPL-Data-Analysis-Project-Using-Apache-Spark/blob/main/Code/IPL%20Data%20Analysis%20Work.ipynb



   
