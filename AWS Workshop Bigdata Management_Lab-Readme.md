# AWS Workshop Bigdata Management
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
1. Using the AWS Console, navigate to the **Aws S3 Storage**. In the search bar, search for **AWS S3** and click on it.

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/b76bc75d-7b54-4a52-94d7-2ad31b30f7be">


2. Select **Create bucket** to navigate to the Aws S3 create bucket page.

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/6f63f23b-3e0c-49c1-a8bf-1cbc6b372b7b">


3. Enter a unique name for the **Bucket name** (Follow this pattern **"bigdata-firstname-bucket"**). Select “Asia Pacific (Singapore) ap-southeast-1”  for Aws Region.

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/b112b1d1-6c64-49a8-b25b-d127b41df5a1">

Scroll down to the bottom and click **Create bucket**.
   
<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/307e406f-6bcd-4946-be86-6e8b6b7de7c1">

When finally created, you should see a text **successfully created bucket "yourbucketname"** and your bucket will appear in the **Buckets** menu.

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/3c66cbcb-e41a-4f76-8c99-b3d5b3513f1b">

### Add some data to your Aws S3 bucket

4. Click on **your bucket** and click **Create folder**

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/7b410feb-70a2-4949-931e-c189a3e9be4d">

Enter **data** for the **Folder name** and click **Create folder**.

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/25352163-a2dc-4e31-a1a2-663d05b6ed1e">

Repeat this step and create another folder name **service output**. Once finish creating, you will see the result like this.

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/cdcfcb82-5756-4e2d-9254-f2f1e591e6f5">

5. Using this link https://drive.google.com/drive/folders/1kJTRMb60gHQmg78InAwgsSgwCeGukVY1?usp=share_link to obtain a data. (download file in this link to your computer)
 
<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/0f8f1f18-dc38-4a5a-9fb8-abe29271c53b">

Click on folder **data** and click **Upload**.

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/8c79ea98-79b9-4865-9321-2dd8dfd7dc6c">

In upload page click **Add files** and Select file **sensor_data.parquet** from your local directory then click **Upload**.

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/2c03dd7d-7f26-4fc7-9b09-ec5bd4c31337">

When finally uploaded, you should see a text **Upload Succeeded** and your file will appear in the **File and folders** menu.

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/f6581ec2-97f3-4fad-b7de-d1325c3815ca">

And when you go back to **your bucket/data** you will see **sensor_data.parquet** in the **Ojects** menu.

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/0dd26af7-b61c-4e89-a6e1-dcecb59dc86c">

##

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/5e69f00a-fdf1-4e19-b7b5-1b4b7f82f75a">

### LAB Part 2 : Working with Aws Glue for Data Movement, Ingestion
##
### Create Aws Glue database in Glue data catalog

1. Using the AWS Console, navigate to the **Aws Glue**. In the search bar, search for **AWS Glue** and click on it.

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/935de13d-8968-48dd-b02f-8c2a393741e2">

2. Make sure you are using the **Asia Pacific (Singapore) ap-southeast-1** region.

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/ed58b6d1-8223-4308-958d-adc61b98c18a">

3. Click **Databases** on the left under Data Catalog section and click **Add database**.

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/7a884aa1-75d7-4315-b9b3-90a3cb01bcbf">

4. Enter a unique name for the **Database name** (Follow this pattern **"bigdata-firstname-glue-database"**) then click **Create Database**.

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/d16809e5-0a24-4def-ac4c-09772f426f1d">

When finally created, your database will appear in the **Databases** menu.

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/dd164173-5b9c-4060-a3dd-a7338df775ee">

### Create Aws Glue Crawler

5. Click **Crawlers** on the left under Data Catalog Section and click **Create crawler**.

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/09951e98-bf87-4b85-a527-a05b44ef6811">

6. On **Set crawler properties** page, provide a name for the new crawler (Follow this pattern **"bigdata-firstname-crawler"**) then click **Next**.

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/f2c86702-fd7b-4b35-b72c-3cd74f7530ba">

7. On **Choose data sources and classifiers page**, select **Not Yet** under Data source configuration then click **Add a data source**.

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/fe4454cb-4c11-4a0a-afce-e118b0ff15bb">

Select **S3** for **Data source** and in **S3 path** browse to **s3://${your bucket}/data** then click **Add an S3 data source**.

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/4417d35e-76c9-43b4-8f03-5c1d89b9588a">

You will be back on **Choose data sources and classifiers page** again and you will see your data source appear in **Data sources menu**. Make sure your data source is selected and then click **Next**.

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/7374666b-c6d8-41cf-9e8d-a9e1dda11b3b">

8. On **Configure security settings** page, in **IAM role** click Choose an existing IAM role and pick the role **AWSGlueServiceRole-default**, then click Next.

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/440c14ad-fff3-4840-a623-3c6e217fefdb">

9. On **Set output and scheduling** page, under **Output configuration** section, choose **your glue database** from the **Target database** dropdown list and enter a unique name for the **Table name prefix** (Follow this pattern "**firstname-sensor**"). Under **Crawler schedule** keep **On demand** frequency, click **Next**.

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/5f18fede-9aa1-4f8e-a42f-988d01c2baa3">

10. Review all the parameters and click **Create crawler**.

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/ae4c6f48-ae5c-4635-bd03-68d23976bfba">

When finally created, you should see a text **One crawler successfully created"**

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/8d3c0a4f-8073-498e-8d60-e1ea04c2046e">

### Run Aws Glue Crawler

11. Once we have created the crawler, go back to **Crawlers** page and then click the check box next to **your crawler** and choose to run the crawler by clicking the **Run** button at the top of the page. It will take a minute or two for the crawler to finish.

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/5379afb7-bb79-4fda-b5ce-93d45deaf118">

12. Once the crawler finish running, you can see the results by clicking **Tables** on the left of the page. You should see 1 new tables that were created by the crawlers - **firstname-sensordata** (The number of table depends on all file and folder in **your aws s3 bucket/data**, now you have only 1 file : **sensor_data.parquet**).

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/a83cc9e3-c5db-4606-8745-99f08bafb7a4">

13. Click on table **data** and you will see the table schema automatically generated by the crawler based on the file **sensor_data.parquet**.

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/b2a66597-faf9-49af-a584-d5264db60c1f">

##

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/fcf9f9f8-e38c-4e71-b106-c8225250d840">

### LAB Part 3: Working with Aws GlueDatabrew for Data Profile, Quality, Transform
##
### Create Aws GlueDatabrew Dataset

1. Using the AWS Console, navigate to the **Aws GlueDatabrew**. In the search bar, search for **AWS GlueDatabrew** and click on it.

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/d3d75466-b6b0-43d9-b39e-d924bc1c8957">

2. Make sure you are using the **Asia Pacific (Singapore) ap-southeast-1** region.

<p align="center">
  <img src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/f2452077-74bf-445b-912f-50f9e6c13445">
</p>

3. Click **Datasets** from the left menu and click **Connect new dataset**.

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/26b1b514-6852-4ff2-830d-86aa18929c50">

4. Enter a unique name for the **Dataset name** (Follow this pattern **"bigdata-firstname-dataset"**)

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/0bfb2656-c123-4bb6-878a-0e2cc3b45f7c">

In **Connect to new dataset menu** select **Data Catalog S3 tables** and select **your glue database** then click on **your glue table**. After finish selecting dataset, click **Create dataset**.

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/33361733-12e1-40f4-898a-4f1a4fc9e089">

When finally created, your dataset will appear in the **Datasets** menu.

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/541f2061-20f5-4ec1-bdb8-1b0a68a3674b">

### View data profiling and data quality

5. Once we have created the dataset, click the check box next to **your dataset** and click **Run data profile** at the top of the page then click **Create profile job**.

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/f0a0a8dc-7982-4ae7-a840-6646d30c22a7">

6. Enter a unique name for the **Job name** (Follow this pattern **"bigdata-firstname-profile job"**) and select **Full dataset**.

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/e44cc58a-14e5-43f0-b38e-ce0e694a4ba6">

In **job output settings** browse to **s3://${your bucket}/service output**.

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/c9b5f50f-b6b0-400d-8b50-170e136d501b">

Expand Data profile configurations, and select Enable PII statistics to identify PII columns when running the data profile job. Under PII categories, select All categories.

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/7a9ef332-5482-4d2f-9795-97b7f87691f8">

In **Permission** click Choose an existing IAM role and pick the role **AWSGlueDataBrewServiceRole-default**, then click **Create and run job**. It will take a minute or two for the profile job to finish.

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/0f793363-1282-4f31-9e98-11dfbc7f2e52">

Once the profile job finish running, This will take you to **Data profile overview** tab of **your dataset**.

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/f982f4d0-ff82-47a8-9562-0dd43410ce0c">

Select the **Columns statistics** tab and view data quality.

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/27ae508f-b1f4-46ea-880b-99fd225604cd">

### Standard Transform

7. Click **Projects** from the left navigation pane and click **Create project**.

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/7e1448cd-9f17-44eb-bac6-f609fa0a9f06">

8. Enter a unique name for the **Project name** (Follow this pattern "bigdata-firstname-project").

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/ba1c4b77-9a9e-4ebd-a882-79b63b317995">

Select **My datasets** and select **your dataset** you created in the previous lab module.

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/1fadd8cf-6f47-4541-82d0-ee9087f168ba">

In **Permission** click Choose an existing IAM role and pick the role **AWSGlueDataBrewServiceRole-default**, then click **Create project**. It will take a minute or two for project to finish.

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/50076ae8-37d2-431b-aad7-e38d7f4509aa">

Once project finish creating, This will take you to **Your Project Workspace**.

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/f09dc571-6df6-4391-a38d-3f6e2d9b809f">

9. Once we have created the project, next step we will transform some data in **your project workspace** by following these steps.
* Click **SPLIT** from the top menu and select **On a single delimiter**. You will see the **setting tab** at the right of your project workspace.
<p align="center">
  <img src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/835fb7d3-f287-4eb3-93ec-c6681e5e1d6d">
</p>

In the **setting tab**,
- Select **event_time** for **Source column**.
- Select **Enter custom value** then enter **T** for **Delimiter**.
- Enter **1** for **Number of times to split**.
<p align="center">
  <img src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/df760ac2-903f-4795-93e4-e9b76f713881">
</p>

Click on **Preview changes** and verify that the preview gives the expected result then select **Apply**.
<p align="center">
  <img src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/d84c4bad-f445-4b4a-bc78-17545dd1714c">
</p>

* Click the ellipsis (**…**) that appear above the column **event_time_2** and select **Delete**.
<p align="center">
  <img src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/15d10d43-84b6-4f35-9479-429c6ad1829b">
</p>

In the **setting tab**, click **Apply**.
<p align="center">
  <img src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/4e131fe2-3027-4adb-870b-7a1e96ac9b08">
</p>

* Click the ellipsis (**…**) above the column **event_time_1** and select **Format** -> **Date-time formats** -> **dd/mm/yyyy**.
<p align="center">
  <img src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/b963c40b-f77b-41cb-a09c-ce3c111b7caf">
</p>

In the **setting tab**, click **Apply**.
<p align="center">
  <img src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/367525a6-0ac6-4b11-bb0a-b6761c6d073a">
</p>

* Click the ellipsis (**…**) above the column **event_time_1** and select **Rename**.
<p align="center">
  <img src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/4bc8d870-1049-471e-9254-499c68f84d26">
</p>


In the **setting tab**, enter **detection time** for **New column name** then click **Apply**.
<p align="center">
  <img src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/46740867-9986-432c-93cb-87a03bf9a03c">
</p>

10. Once we have done transform the data, next step we will create the **recipe** of all data transformation steps in **your project workspace** by following these steps. 

> **What is a recipe**
> 
> A collection of data transformation steps is called a recipe. They are created or edited in an DataBrew project and can be published as a stand-alone entity. <br />
> A published recipe is a template of just the transformations steps without context of the data. Users can publish multiple versions of a recipe from a project as they work on it. A recipe can be downloaded or applied to any other dataset in a project through a recipe job.

* open your recipe by clicking **RECIPE** on most right of the top menu and verify that your recipe contains 4 steps that look like the ones below.
<p align="center">
  <img src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/c54c6f47-e38d-4a64-8f75-4822277155ff">
</p>

* In the **Recipe tab**, click **Publish**
<p align="center">
  <img src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/a6126bc9-d5d7-47d3-8ae0-80f8b4e0d7a2">
</p>

* When finally created, click **RECIPES** view from left navigation , choose **All recipes** or **Published** from the filter option and select **your recipe** to validate the steps.
<p align="center">
  <img src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/193138c7-f1bb-4d57-a076-1efc50652b63">
</p>

11. Once we have created the recipe, next step we will create the **recipe job** for **your project workspace** by following these steps.

> **What is a recipe job**
> 
> DataBrew takes on the job of transforming your data by running the instructions that you set up when you made a recipe. The process of running these instructions is called a job. A job can put your data recipes into action according to a preset schedule. But you aren’t confined to a schedule. You can also run jobs on demand. If you want to profile some data, you don’t need a recipe. In that case, you can just set up a profile job to create a data profile.

* Click **PROJECTS** view from left navigation and open **your project**.
<p align="center">
  <img src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/94962530-1179-4ff4-9731-abd99c33df42">
</p>

* In **your project workspace**, click **Create job**.
<p align="center">
  <img src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/2c577cf4-0dc1-40fc-bb6e-71be49c48556">
</p>

* Enter a unique name for the **Job name** (Follow this pattern **"bigdata-firstname-recipe job"**) and select **Full dataset**.
<p align="center">
  <img src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/e87a51c5-4694-4066-8f04-328a88ce1b44">
</p>

* In **job output settings**,
- Select **Data Catalog S3 tables** for **Output to**.
- Select **your glue database** for **Database name**.
- Select **your glue table** for **Table name**.
- Select **Use default source location** for **Table name prefix**.

<p align="center">
  <img src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/05ab971a-3b91-4c7c-87c5-5049acf873d3">
</p>

* In **Permission** click Choose an existing IAM role and pick the role **AWSGlueDataBrewServiceRole-default**, then click **Create and run job**. It will take a minute or two for the recipe job to finish.
<p align="center">
  <img src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/2ca15395-bc27-451c-97b5-71521ad39886">
</p>

* You can monitor running process in the **JOBS** view to which you can navigate via left navigation. Once the recipe job finish running, the status will change from **Running** to **Succeeded**.
<p align="center">
  <img src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/4920bb25-f8c7-4e43-8072-e0fcdefbe6bd">
</p>

* Select **your recipe job**, click **1 output** in **Job output tab** will show the location of the output file then click on **destination link**. This will take you to **AWS Glue table** console.
<p align="center">
  <img src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/5e413a5c-53cb-4b6b-a039-5730a6386910">
</p>


* Click on **your glue table**. In **Schema** tab, You should see that the data has changed from **event_time** to **detection time**.
![image](https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/e6a16a77-52c2-4d68-ab17-26eef920804d)

##

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/3ba5cdb6-d1be-47c3-b33b-309011d1ce3c">

### LAB Part 4 : Querying Data Using AWS Athena
##
### Launch query editor and connect to the data

1. Using the AWS Console, navigate to the **Aws Athena**. In the search bar, search for **AWS Athena** and click on it.
<p align="center">
  <img src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/13d05f2a-26cc-42f7-9bcb-2c0270c596b8">
</p>

2. Make sure you are using the **Asia Pacific (Singapore) ap-southeast-1** region.
<p align="center">
  <img src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/f2452077-74bf-445b-912f-50f9e6c13445">
</p>

3. In **Get started** menu, select **Query your data** then click **Launch query editor**.

<p align="center">
  <img src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/0225bb36-367f-4802-848b-3c1d4ab98246">
</p>

4. This will take you to **Query editor console** and you will see the text **"Before you run your first query, you need to set up a query result location in Amazon S3."**. Click **Edit settings**.
<p align="center">
  <img src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/de92f356-8d6f-4769-a3a7-11c06db9fd03">
</p>

5. In **Query result location and encryption** browse to **s3://${your bucket}/service output** then click **Save**.
<p align="center">
  <img src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/fd09df75-58f9-4273-9c5f-1e4a73ccf67c">
</p>

6. You should see a text **Settings successfully updated.**. Click **Editor** to go back to **Query editior console**.
<p align="center">
  <img src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/f483875a-4343-46c1-a180-8426f204fd85">
</p>

7. In the **Data** setting tab,
- Select **AwsDataCatalog** for **Data source**.
- Select **your glue database** for **Database**.
- Click icon ![image](https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/eb939f0b-63ec-4621-a05c-1fb1baf9c23c) on **your glue table** then select **Preview Table**.
<p align="center">
  <img src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/e57f608b-7670-4dd2-bd4c-7fb76524e23b">
</p>

8. You will see the preview of your data in **your glue table**.
<p align="center">
  <img src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/13d90ba0-e9bf-4504-8b07-cb620bc7f535">
</p>

9. Click icon ![image](https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/e7165c93-7367-48c0-9762-7810908e1540) to add new query tab.
<p align="center">
  <img src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/7deab762-39cf-4907-8030-c15656332fbf">
</p>

10. In the Query 3 tab, copy this code and paste in **code editor** then click **Run**.
```sql
SELECT * 
FROM "bigdata-parin-glue-database"."parin-sensordata" 
WHERE "status" = 'OK';
```
<p align="center">
  <img src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/14314af4-e406-4a9d-826c-ffd0004fc3f4">
</p>

11. View the query results.
<p align="center">
  <img src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/0b664e93-5024-45ba-b5ec-619041f9283c">
</p>
##
# Congrats! Now you already done AWS Workshop Bigdata Management.




