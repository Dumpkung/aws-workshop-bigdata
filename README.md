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
1. Using the AWS Console, navigate to the Amazon S3 Storage. In the search bar, search for **AWS S3** and click on it.

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/b76bc75d-7b54-4a52-94d7-2ad31b30f7be">


2. Select **Create bucket** to navigate to the Amazon S3 create bucket menu.

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/6f63f23b-3e0c-49c1-a8bf-1cbc6b372b7b">


3. Enter a unique name for the **Bucket name** (Follow this pattern "bigdata-firstname-bucket"). Select “Asia Pacific (Singapore) ap-southeast-1”  for Aws Region.

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/b112b1d1-6c64-49a8-b25b-d127b41df5a1">

Scroll down to the bottom and click on **Create bucket**.
   
<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/307e406f-6bcd-4946-be86-6e8b6b7de7c1">

When finally created, you should see a text **successfully created bucket "yourbucketname"** and your bucket will appear in the **Buckets** menu.

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/3c66cbcb-e41a-4f76-8c99-b3d5b3513f1b">


4. Using this link https://drive.google.com/drive/folders/1kJTRMb60gHQmg78InAwgsSgwCeGukVY1?usp=share_link to obtain a data. (download file in this link to your computer)
 
 <img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/0f8f1f18-dc38-4a5a-9fb8-abe29271c53b">

Click on your bucket and click on **Upload**.

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/9c20c899-a7ab-44c9-87b7-4c416f2d8697">

In upload menu click on **Add files** and Select file **sensor_data.parquet** from your local directory then click on **Upload**.

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/a65511a2-c3c4-4d83-b882-7ff2f10e6b84">

When finally uploaded, you should see a text **Upload Succeeded** and your file will appear in the **File and folders** menu.

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/f77f1cf0-d963-405e-bd23-fde5b78ee62f">

And when you go back to your bucket you will see **sensor_data.parquet** in the Ojects menu.

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/0fb653f6-5186-4bf4-a1ce-f2a3e36c3581">

##

<img align="center" src="https://github.com/Dumpkung/aws-workshop-bigdata/assets/31465515/5e69f00a-fdf1-4e19-b7b5-1b4b7f82f75a">

### LAB Part 2 : Working with Aws Glue for Data Movement, Ingestion
##


