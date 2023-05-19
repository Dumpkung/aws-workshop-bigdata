# AWS Workshop Bigdata
## Before starting this lab
1. Using this table to obtain an user and password for access Aws console.

User name | Password | Console sign-in URL
----- | ----- | ----- |
Chanagunc.mitrphol | 5+gNE1_J | https://548746805562.signin.aws.amazon.com/console
chinnachotc.mitrphol | sNE'R42+ | https://548746805562.signin.aws.amazon.com/console
Krisanat.mitrphol | #nXE6n}[ | https://548746805562.signin.aws.amazon.com/console
Nawaratp.mitrphol | =QOnE95_ | https://548746805562.signin.aws.amazon.com/console
Nuttapons.mitrphol | I1pC7*1Y | https://548746805562.signin.aws.amazon.com/console
Phuvanat.mitrphol | (uH4{O%' | https://548746805562.signin.aws.amazon.com/console
Pitchayac.mitrphol | 7fE5ET2_ | https://548746805562.signin.aws.amazon.com/console
sarotc.mitrphol | ehT2a7%] | https://548746805562.signin.aws.amazon.com/console
Sitthapongk.mitrphol | 9adGt31\| | https://548746805562.signin.aws.amazon.com/console
Suriya.mitrphol | nU7{vF6& | https://548746805562.signin.aws.amazon.com/console

2. Login to Aws console. (Open link from **"Console sign-in URL"**)

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/3fb41889-59ed-4ac7-8d02-b71bc9a309ef">

3. After successful login, you will see this window.

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/08eab7af-149a-46eb-9deb-3b0e9389c3b0">


## Getting started

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/a733946f-37ad-4033-8b67-527b3e83850a">


### LAB Part 1 : Manage your data lake storage with Aws S3
##
### Create Aws S3 bucket
1. Using the AWS Console, navigate to the Aws S3 Storage. In the search bar, search for **AWS S3** and click on it.

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/b76bc75d-7b54-4a52-94d7-2ad31b30f7be">


2. Select **Create bucket** to navigate to the Aws S3 create bucket page.

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/6f63f23b-3e0c-49c1-a8bf-1cbc6b372b7b">


3. Enter a unique name for the **Bucket name** (Follow this pattern "bigdata-firstname-bucket"). Select “Asia Pacific (Singapore) ap-southeast-1”  for Aws Region.

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/b112b1d1-6c64-49a8-b25b-d127b41df5a1">

Scroll down to the bottom and click **Create bucket**.
   
<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/307e406f-6bcd-4946-be86-6e8b6b7de7c1">

When finally created, you should see a text **successfully created bucket "yourbucketname"** and your bucket will appear in the **Buckets** menu.

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/3c66cbcb-e41a-4f76-8c99-b3d5b3513f1b">

### Add some data to your Aws S3 bucket

4. Using this link https://drive.google.com/drive/folders/1kJTRMb60gHQmg78InAwgsSgwCeGukVY1?usp=share_link to obtain a data. (download file in this link to your computer)
 
 <img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/0f8f1f18-dc38-4a5a-9fb8-abe29271c53b">

Click on your bucket and click **Upload**.

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/9c20c899-a7ab-44c9-87b7-4c416f2d8697">

In upload page click **Add files** and Select file **sensor_data.parquet** from your local directory then click **Upload**.

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/a65511a2-c3c4-4d83-b882-7ff2f10e6b84">

When finally uploaded, you should see a text **Upload Succeeded** and your file will appear in the **File and folders** menu.

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/f77f1cf0-d963-405e-bd23-fde5b78ee62f">

And when you go back to your bucket you will see **sensor_data.parquet** in the Ojects menu.

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/0fb653f6-5186-4bf4-a1ce-f2a3e36c3581">

##

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/5e69f00a-fdf1-4e19-b7b5-1b4b7f82f75a">

### LAB Part 2 : Working with Aws Glue for Data Movement, Ingestion
##
### Create Aws Glue database in Glue data catalog

1. Using the AWS Console, navigate to the Aws Glue. In the search bar, search for **AWS Glue** and click on it.

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/935de13d-8968-48dd-b02f-8c2a393741e2">

2. Make sure you are using the **Asia Pacific (Singapore) ap-southeast-1** region.

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/ed58b6d1-8223-4308-958d-adc61b98c18a">

3. Click **Databases** on the left under Data Catalog section and click **Add database**.

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/7a884aa1-75d7-4315-b9b3-90a3cb01bcbf">

4. Enter a unique name for the **Database name** (Follow this pattern "bigdata-firstname-glue-database") then click **Create Database**.

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/d16809e5-0a24-4def-ac4c-09772f426f1d">

When finally created, your database will appear in the **Databases** menu.

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/dd164173-5b9c-4060-a3dd-a7338df775ee">

### Create Aws Glue Crawler

5. Click **Crawlers** on the left under Data Catalog Section and click **Create crawler**.

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/09951e98-bf87-4b85-a527-a05b44ef6811">

6. On **Set crawler properties** page, provide a name for the new crawler (Follow this pattern "bigdata-firstname-crawler") then click **Next**.

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/f2c86702-fd7b-4b35-b72c-3cd74f7530ba">

7. On **Choose data sources and classifiers page**, select **Not Yet** under Data source configuration then click **Add a data source**.

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/fe4454cb-4c11-4a0a-afce-e118b0ff15bb">

Select **S3** for **Data source** and in **S3 path** browse to **s3://${your bucket}** then click **Add an S3 data source**.

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/99c13e89-4517-450c-8b68-910f1fa01fa2">

You will be back on **Choose data sources and classifiers page** again and you will see your data source appear in **Data sources menu**. Make sure your data source is selected and then click **Next**.

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/e2461778-5bf1-4b9b-b41c-690415b71169">

8. On **Configure security settings** page, in **IAM role** click Choose an existing IAM role and pick the role **AWSGlueServiceRole-default**, then click Next.

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/440c14ad-fff3-4840-a623-3c6e217fefdb">

9. On **Set output and scheduling** page, under Output configuration section, choose **your glue database** from the **Target database** dropdown list. Under Crawler schedule keep **On demand** frequency, click **Next**.

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/56584240-a700-4db7-b7b7-ecd48e515ef6">

10. Review all the parameters and click **Create crawler**.

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/f82855d8-025b-4b57-905b-68536a84a0fc">

When finally created, you should see a text **One crawler successfully created"**

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/c6fc5978-9254-42b8-ae24-2360c03dd870">

### Run Aws Glue Crawler

11. Once we have created the crawler, go back to **Crawlers** page and then click the check box next to **your crawler** and choose to run the crawler by clicking the **Run** button at the top of the page. It will take a minute or two for the crawler to finish.

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/5379afb7-bb79-4fda-b5ce-93d45deaf118">

12. Once the crawler finish running, you can see the results by clicking **Tables** on the left of the page. You should see 1 new tables that were created by the crawlers - **bigdata_firstname_bucket** (The number of table depends on all file and folder in **your aws s3 bucket**, now you have only 1 file : **sensor_data.parquet**).

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/08846d88-67f4-41f0-ab01-2fae98361555">

13. Click on table **bigdata_firstname_bucket** and you will see the table schema automatically generated by the crawler based on the file **sensor_data.parquet**.

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/b7e02335-f0fc-4d1f-87ec-b207c38f1513">

##

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/fcf9f9f8-e38c-4e71-b106-c8225250d840">

### LAB Part 3: Working with Aws GlueDatabrew for Data Profile, Quality, Transform
##
### Create Aws GlueDatabrew Dataset

1. Using the AWS Console, navigate to the Aws GlueDatabrew. In the search bar, search for **AWS GlueDatabrew** and click on it.

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/d3d75466-b6b0-43d9-b39e-d924bc1c8957">

2. Make sure you are using the **Asia Pacific (Singapore) ap-southeast-1** region.

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/f2452077-74bf-445b-912f-50f9e6c13445">

3. Click **Datasets** from the left menu and click **Connect new dataset**.

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/26b1b514-6852-4ff2-830d-86aa18929c50">

4. Enter a unique name for the **Dataset name** (Follow this pattern "bigdata-firstname-dataset")

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/0bfb2656-c123-4bb6-878a-0e2cc3b45f7c">

In **Connect to new dataset menu** select **Data Catalog S3 tables** and select **your glue database** then click on **your glue table**. After finish selecting dataset, click **Create dataset**.

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/7adff0f4-79dc-44e2-871b-234787891742">

When finally created, your dataset will appear in the **Datasets** menu.

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/b17a0c64-e4b7-451a-902d-247dbc4bb76b">

### View data profiling and data quality

5. Once we have created the dataset, click the check box next to **your dataset** and click **Run data profile** at the top of the page then click **Create profile job**.

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/649502af-e8c0-4af7-969f-bb9ae607ffb0">

6. Enter a unique name for the **Job name** (Follow this pattern "bigdata-firstname-profile job") and select **Full dataset**.

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/e44cc58a-14e5-43f0-b38e-ce0e694a4ba6">

In job output settings browse to **s3://${your bucket}**.

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/d2e055ee-f70c-44f5-af0e-fd20a64eb410">

Expand Data profile configurations, and select Enable PII statistics to identify PII columns when running the data profile job. Under PII categories, select All categories.

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/7a9ef332-5482-4d2f-9795-97b7f87691f8">

In **Permission** click Choose an existing IAM role and pick the role **AWSGlueDataBrewServiceRole-default**, then click **Create and run job**. It will take a minute or two for the profile job to finish.

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/0f793363-1282-4f31-9e98-11dfbc7f2e52">

Once the profile job finish running, This will take you to **Data profile overview** tab of **your dataset**.

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/28a11467-5c8e-47d3-b33b-c9e3edbdb27a">

Select the **Columns statistics** tab and view data quality.

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/7b5d0e4b-90ab-45a8-95d4-45f00e102a4e">

### Standard Transform

7. Click **Projects** from the left navigation pane and click **Create project**.

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/7e1448cd-9f17-44eb-bac6-f609fa0a9f06">


