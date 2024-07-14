<p align="center">
<img src="https://imgur.com/7Zrg8KE.png" height="80%" width="80%"/>

</p>

<p align="center">
(IN PROGRESS)
</p>

<h1>AWS Certified Solutions Architect - Associate Training</h1>

<h2>Description</h2>
In this repository, you will be able to follow along as I learn how to navigate through AWS. Not only am I learning the concepts and why things are done a certain way, but I am also gaining hands-on experience at the same time. I've chosen to utlize Adrian Cantill's AWS Certified Solutions Architect - Associate course for my training with the end goal of sitting for the exam and receiving my offical certification. 

<h2>Contents</h2>

- [AWS Root User Accounts (General and Production)](https://github.com/anthonybastone1/AWS-SAA?tab=readme-ov-file#aws-root-user-accounts-general-and-production)
- [IAM User Accounts (iamadmin)](https://github.com/anthonybastone1/AWS-SAA?tab=readme-ov-file#iam-user-accounts-iamadmin)
- [Access Keys](https://github.com/anthonybastone1/AWS-SAA?tab=readme-ov-file#access-keys)
- [Virtual Private Cloud (VPC)](https://github.com/anthonybastone1/AWS-SAA?tab=readme-ov-file#virtual-private-cloud-vpc)
- [Elastic Compute Cloud (EC2)](https://github.com/anthonybastone1/AWS-SAA?tab=readme-ov-file#elastic-compute-cloud-ec2)
- [Simple Storage Service (S3)](https://github.com/anthonybastone1/AWS-SAA?tab=readme-ov-file#simple-storage-service-s3)

<h2>AWS Root User Accounts (General and Production):</h2>

<p align="center">
<br />
First, I created both my AWS General and Production accounts. These are my root user accounts which have permissions and access to everything within them. You must have a root user account in order to move forwards, and it is a simple account setup just like any other website. Just make sure that you name them accordingly to avoid confusion later on.
<br/>
<br/>
However, they will not be used later due to the inherent security risk associated with them. If the login information to those accounts is compromised, then an attacker will have access to my entire console.
<br/>
<br/>
So once the root user accounts have been created, we will create Identity and Access Mangament (IAM) General and Production accounts, and grant them the same permissions as the root user accounts. These two IAM accounts will serve as our administrator accounts for both the General AWS account and Production AWS account.
<br/>
<br/>
In the images below, you will see the General and Production account names in the top right hand corner.
<br/>
<br/>
<img src="https://imgur.com/vvwdzw2.png" height="80%" width="80%"/>
<br />
<br />
<img src="https://imgur.com/3DJNDt3.png" height="80%" width="80%"/>
<br />
<br />
Next, I had to grant user/role access to billing information for the IAM users (IAMADMIN) that I will be creating. 
<br />
<br />
Once again, one image is for the AWS General account, and the other is for the AWS Production account.
<br />
<br />
<img src="https://imgur.com/NselaUN.png" height="80%" width="80%"/>
<br />
<br />
<img src="https://imgur.com/RaKWYgh.png" height="80%" width="80%"/>
<br />
<br />

<h2>IAM User Accounts (iamadmin):</h2>

<p align="center">
<br /> 
Since IAM access has now been enabled, I can create my IAM users. IAM users are neither regionally nor globally specific, they are only specific to that single account. So the same name can be used for multiple accounts.
<br />
<br />
I've named both the General and Production IAM user accounts, "iamadmin"
<br />
<br />
This process is repeated the same exact way in both accounts, so there is no need to continue duplicating screenshots.
<br />
<br />
<img src="https://imgur.com/K9CgU6q.png" height="80%" width="80%"/>
<br />
<br />
After specifying the user details, since I haven't configured any groups or permissions of my own, I just head over to, "Attach policies directly," and select "AdministratorAccess"
<br />
<br />
This will grant the iamadmin users the same permissions as the root accounts, but with less security concern.
<br />
<br />
<img src="https://imgur.com/vWSzVgK.png" height="80%" width="80%"/>
<br />
<br />
Nothing fancy, just learning the basics here, so I can continue and create the user(s).
<br />
<br />
<img src="https://imgur.com/E1oSA5x.png" height="80%" width="80%"/>
<br />
<br />
Once the user has been successfully created, I go to log out and log back in. You'll notice the account ID, iamadmin @ adbjr-aws-general and iamadmin @ adbjr-aws-production is different than the root user accounts of AB-AWS-GENERAL and AB-AWS-PRODUCTION. This is to differentiate between the root users and IAM users.
<br />
<br />
<img src="https://imgur.com/gkuIG8y.png" height="80%" width="80%"/>
<br />
<br />
<img src="https://imgur.com/pkGJm8D.png" height="80%" width="80%"/>
<br />
<br />
<img src="https://imgur.com/DCYxGhR.png" height="80%" width="80%"/>
<br />
<br />

<h2>Access Keys:</h2>

<p align="center">
<br />
Following the creation of the iamadmin user accounts is the creation of the access keys. Since this is just to learn the concepts of AWS, I won't be using all 6. For this, I am only going to use the access keys that I create to enable the AWS Command Line Interface (CLI) to access the AWS accounts.
<br />
<br />
<img src="https://imgur.com/nBqAnbx.png"height="80%" width="80%"/>
<br />
<br />
<img src="https://imgur.com/GVSQf71.png"height="80%" width="80%"/>
<br />
<br />
Now that I've created the access keys, I need to install the AWS CLI. To do so, we can locate the actual page with instructions that AWS has provided for us and follow the directions for your specific operating system. Again, this is simply training to learn the foundational elements of AWS architecture, so when installing the CLI, I will leave all options at the default settings.
<br />
<br />
<img src="https://imgur.com/aoQ9oAV.png"height="80%" width="80%"/>
<br />
<br />
<img src="https://imgur.com/R1aPJvr.png"height="80%" width="80%"/>
<br />
<br />
<img src="https://imgur.com/KvL3A9G.png"height="80%" width="80%"/>
<br />
<br />
After successful installation, I open up my terminal and run the following commands to verify that it has been successfully installed and is running the most current version.
<br />
<br />
<img src="https://imgur.com/rPmrPp4.png"height="80%" width="80%"/>
<br />
<br />
Once verified, I will stay in the terminal and run the next set of commands. For this, I will not provide screenshots as you have to input your AWS Access Key ID and AWS Secret Access Key.
<br/>
<br/>
[START]
<br/>
<br/>
aws configure --profile iamadmin-general
<br/>
<br/>
*ENTER AWS ACCESS KEY ID*
<br/>
<br/>
*ENTER AWS SECRET ACCESS KEY*
<br/>
<br/>
*ENTER DEFAULT REGION* For me this is, us-east-1, which is the Northern Virginia region.
<br/>
<br/>
*LEAVE DEFAULT OUTPUT BLANK AND PRESS ENTER*
<br/>
<br/>
aws s3 ls --profile iamadmin-general
<br/>
<br/>
I REPEAT THE SAME EXACT PROCESS FOR THE PRODUCTION ACCOUNT AND TYPE iamadmin-production instead of iamadmin-general.
[END]
<br/>
<br/>
 
<h2>Virtual Private Cloud (VPC):</h2>

<p align="center">
<br />
After configuring the AWS CLI, I head back into my iamadmin general account and go to my virtual private cloud. The default VPC has been created, and every AWS default VPC, no matter where you are, will have the same IPv4 address of 172.31.0.0/16. Going back to our networking fundamentals, we know that this IPv4 address is an RFC 1918 private address.
<br/>
<br/>
<img src="https://imgur.com/zsQoiiV.png" height="80%" width="80%"/>
<br />
<br />
While learning how to navigate through the different areas within the VPC, I notice there are 6 subnets within the default IPv4 address.
<br/>
<br/>
<img src="https://imgur.com/ZP4T5rO.png" height="80%" width="80%"/>
<br/>
<br/>
As I scroll over, I come to understand that there are 6 subnets because there are 6 availability zones within us-east-1. However, not every region has the same number of availability zones, therefore, they all have different numbers of subnets as well.
<br/>
<br/>
<img src="https://imgur.com/9n3Gfxe.png" height="80%" width="80%"/>
<br />
<br />

<h2>Elastic Compute Cloud (EC2) Key Pairs, Instances, and Security Groups:</h2>

<p align="center">
<br />
After exploring VPC a bit, I head over to the Elastic Compute Cloud (EC2) section to create a new key pair within the iamadmin general account.
<br />
<br />
<img src="https://imgur.com/JPEvHSR.png" height="80%" width="80%"/>
<br />
<br />
I then learn how to launch a new EC2 instance
<br />
<br />
<img src="https://imgur.com/gZTaccl.png" height="80%" width="80%"/>
<br />
<br />
<img src="https://imgur.com/Ybdq4bF.png" height="80%" width="80%"/>
<br />
<br />
<img src="https://imgur.com/EXnwPW1.png" height="80%" width="80%"/>
<br />
<br />
<img src="https://imgur.com/hrOozWg.png" height="80%" width="80%"/>
<br />
<br />
After successfully launching my first EC2 instance, I right click on the instance, and click connect.
<br />
<br />
<img src="https://imgur.com/uIBX56k.png" height="80%" width="80%"/>
<br />
<br />
I then choose to connect via SSH client and use the following commands provided to me by AWS.
<br />
<br />
<img src="https://imgur.com/vsGxIfY.png" height="80%" width="80%"/>
<br />
<br />
Now that I've launched and EC2 instance and connected to it via SSH client, I can now terminate the instance and security group because it isn't needed. This was simply to learn how to launch one and how to terminate one. If not terminated completely, charges will still accrue, so we need to be mindful of that when working in the cloud.
<br />
<br />
<img src="https://imgur.com/l7k9xsB.png" height="80%" width="80%"/>
<br />
<br />
<img src="https://imgur.com/bEfESKX.png" height="80%" width="80%"/>
<br />
<br />
<img src="https://imgur.com/jn9J3Hn.png" height="80%" width="80%"/>
<br />
<br />
 
<h2>Simple Storage Service (S3):</h2>

<p align="center">
<br />
Here I begin learning about Simple Storage Service (S3) and create my first bucket.
<br />
<br />
Bucket names must be globally unique since S3 campaigns do not specify regions. There is also a more specific set of rules for naming buckets that can be found within the AWS platform.
<br />
<br />
You do, however, have to specify a region for your bucket to be placed in. This is different from S3 campaigns not specifying regions.
<br />
<br />
<img src="https://imgur.com/8UNlwu9.png" height="80%" width="80%"/>
<br />
<br />
<img src="https://imgur.com/Lz45eBJ.png" height="80%" width="80%"/>
<br />
<br />
<img src="https://imgur.com/dZ1hbzd.png" height="80%" width="80%"/>
<br />
<br />
Now that I've created my first bucket, I will upload objects to the bucket. Once uploaded, I can go back to the bucket, click inside the bucket, and see the 3 objects that I've placed within it.
<br />
<br />
<img src="https://imgur.com/M0X1GXk.png" height="80%" width="80%"/>
<br />
<br />
<img src="https://imgur.com/kIKCazI.png" height="80%" width="80%"/>
<br />
<br />
Next, I create a folder within the bucket, which I've named archive. 
<br />
<br />
It doesn't actually create a folder named archive, but it creates an object with the name archive/ that AWS labels as a folder. Folders are emulated using prefixes. I can go inside that folder and upload objects to it, which I show in the images below.
<br />
<br />
<img src="https://imgur.com/sTUM4Sv.png" height="80%" width="80%"/>
<br />
<br />
<img src="https://imgur.com/7GBl18r.png" height="80%" width="80%"/>
<br />
<br />
Now if I go back to the main bucket and open one of the objects, I'm presented with an overview screen.
<br />
<br />
If I try to open the Object URL by just the link, it will return an access denied error as shown below.
<br/>
<br/>
<img src="https://imgur.com/y9URLdC.png" height="80%" width="80%"/>
<br />
<br />
<img src="https://imgur.com/J8iuPO4.png" height="80%" width="80%"/>
<br />
<br />
But if I select the open tab in the top right of the overview screen, it will open. This is because by using just the link, I am trying to access the object with no authentication. But by using the button within the bucket, I have been authenticated.
<br />
<br />
<img src="https://imgur.com/cex95L9.png" height="80%" width="80%"/>
<br />
<br />
Just like my EC2 instance, I am now going to delete the bucket that I've created as this was just a high level overview of S3.
<br />
<br />
So first, I will select the bucket, then click empty, to remove the contents of the bucket.
<br />
<br />
Once that's been completed, I will return to the bucket, select it again, and click delete to permanently delete the bucket.
<br />
<br />
<img src="https://imgur.com/D6mqBhq.png" height="80%" width="80%"/>
<br />
<br />


<p align="center">
<br />

</p>

<br />
<br />


<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
