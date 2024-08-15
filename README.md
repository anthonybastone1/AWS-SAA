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

- AWS Fundamentals
<br/>[AWS Root User Accounts (General and Production)](https://github.com/anthonybastone1/AWS-SAA?tab=readme-ov-file#aws-root-user-accounts-general-and-production), [IAM User Accounts (iamadmin)](https://github.com/anthonybastone1/AWS-SAA?tab=readme-ov-file#iam-user-accounts-iamadmin), [Access Keys](https://github.com/anthonybastone1/AWS-SAA?tab=readme-ov-file#access-keys), [Virtual Private Cloud (VPC)](https://github.com/anthonybastone1/AWS-SAA?tab=readme-ov-file#virtual-private-cloud-vpc), [Elastic Compute Cloud (EC2)](https://github.com/anthonybastone1/AWS-SAA?tab=readme-ov-file#elastic-compute-cloud-ec2-key-pairs-instances-and-security-groups), [Simple Storage Service (S3)](https://github.com/anthonybastone1/AWS-SAA?tab=readme-ov-file#simple-storage-service-s3), [CloudFormation (CFN) Basics](https://github.com/anthonybastone1/AWS-SAA?tab=readme-ov-file#cloudformation-basics), [CloudWatch (CW) Basics](https://github.com/anthonybastone1/AWS-SAA?tab=readme-ov-file#cloudwatch-cw-basics)

- IAM, Accounts, and AWS Organizations
<br/>[Simple Identity Permissions](https://github.com/anthonybastone1/AWS-SAA?tab=readme-ov-file#simple-identity-permissions), [IAM Groups](https://github.com/anthonybastone1/AWS-SAA?tab=readme-ov-file#iam-groups), [AWS Organizations](https://github.com/anthonybastone1/AWS-SAA?tab=readme-ov-file#aws-organizations)

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

<h2>CloudFormation Basics:</h2>

<p align="center">
<br />
In this section, I learned the CloudFormation basics, and how to use a CloudFormation template to create and delete an EC2 instance within AWS. 
<br />
<br />
First, I created a stack uploading the ready made template that is pictured below.
<br />
<br />
<img src="https://imgur.com/MWyPt39.png" height="80%" width="80%"/>
<br />
<br />
When uploading a template to CloudFormation, it is actually uploading the template directly to an S3 bucket that it creates automatically.
<br />
<br />
<img src="https://imgur.com/P3fttKV.png" height="80%" width="80%"/>
<br />
<br />
Naming the stack. You'll see, the LatestAmiID and SSHandWebLocation are set to default at those values because that is what's set in the template.
<br />
<br />
<img src="https://imgur.com/DtYxWcI.png" height="80%" width="80%"/>
<br />
<br />
I am not changing any of the advanced options in this because it's just a basic overview.
<br />
<br />
<img src="https://imgur.com/2TSYaYv.png" height="80%" width="80%"/>
<br />
<br />
By using CloudFormation, I am actually creating an IAM role, so I need to check the box within Capabilities.
<br />
<br />
<img src="https://imgur.com/K28ybgW.png" height="80%" width="80%"/>
<br />
<br />
After creating the stack, it took me to inside the stack. By clicking on events, I could watch the actual creation in progess for each resource.
<br />
<br />
<img src="https://imgur.com/aCgyKpl.png" height="80%" width="80%"/>
<br />
<br />
By clicking on outputs tab, I could also see a list of all of the outputs that were generated from the stack.
<br />
<br />
They match the outputs that are listed inside the CloudFormation template that I uploaded. Same goes for the resources tab.
<br />
<br />
<img src="https://imgur.com/DakM7CG.png" height="80%" width="80%"/>
<br />
<br />
From the resources tab, you can see the EC2 instance that was created. By clicking on it, it'll take you to the actual resource inside AWS.
<br />
<br />
Once there, I right clicked on the instance and clicked connect. Earlier I connected to my instance via a key pair and SSH, but this time I am connecting to it via Session Manager.
<br />
<br />
It is a lot quicker this way and if I type the command, bash, it allows me to run normal linux commands.
<br />
<br />
<img src="https://imgur.com/XJkWQrK.png" height="80%" width="80%"/>
<br />
<br />
<img src="https://imgur.com/rkN9BcX.png" height="80%" width="80%"/>
<br />
<br />
Lastly, I will go back to the CloudFormation console to delete the stack along with all of its resources.
<br />
<br />
The stack will delete all of the logical resources and then all of the corresponding physical resources. It cleans up after itself.
<br />
<br />
I can watch it delete the resources just like how I watched it create the resources.
<br />
<br />
<img src="https://imgur.com/VRzb5Yp.png" height="80%" width="80%"/>
<br />
<br />
<img src="https://imgur.com/tcCpLEo.png" height="80%" width="80%"/>
<br />
<br />
<img src="https://imgur.com/BurYSC3.png" height="80%" width="80%"/>
<br />
<br />
 
<h2>CloudWatch (CW) Basics:</h2>

<p align="center">
<br />
Getting experience interacting with CloudWatch.
<br />
<br />
Launched a new instance named CloudwatchTest and used an Amazon Linux machine image. Will connect to this instance using EC2 instance connect intead of SSH Client, so we will proceed without a key pair.
<br />
<br />
<img src="https://imgur.com/DyXf4qz.png" height="80%" width="80%"/>
<br />
<br />
<img src="https://imgur.com/ISXT9G4.png" height="80%" width="80%"/>
<br />
<br />
Named the security group and security group description to CloudwatchSG.
<br />
<br />
<img src="https://imgur.com/OKB4kXT.png" height="80%" width="80%"/>
<br />
<br />
Launched the instance.
<br />
<br />
<img src="https://imgur.com/NzbFcc3.png" height="80%" width="80%"/>
<br />
<br />
Opened the CloudWatch service in a new tab to create an alarm.
<br />
<br />
<img src="https://imgur.com/LxwhbYC.png" height="80%" width="80%"/>
<br />
<br />
Clicked Create Alarm > Select Metric > EC2 > Per-Instance Metrics
<br />
<br />
<img src="https://imgur.com/LxwhbYC.png" height="80%" width="80%"/>
<br />
<br />
<img src="https://imgur.com/bf3AL5r.png" height="80%" width="80%"/>
<br />
<br />
<img src="https://imgur.com/Nsn8dtr.png" height="80%" width="80%"/>
<br />
<br />
Then located the CloudwatchTest instance ID and found and selected CPUUtilization.
<br />
<br />
<img src="https://imgur.com/TiPzrI3.png" height="80%" width="80%"/>
<br />
<br />
The conditions that were selected were Static for the threshold type, and Greater/Equal to 15% for the CPUUtilization.
<br />
<br />
<img src="https://imgur.com/iX9f0AN.png" height="80%" width="80%"/>
<br />
<br />
Since this is not in production usage, we can remove the alarm state trigger.
<br />
<br />
<img src="https://imgur.com/YrN63Pb.png" height="80%" width="80%"/>
<br />
<br />
Named the alarm CloudwatchTestHighCPU, left everything else as is, then created the alarm.
<br />
<br />
<img src="https://imgur.com/StYXso7.png" height="80%" width="80%"/>
<br />
<br />
<img src="https://imgur.com/c2wmF7Z.png" height="80%" width="80%"/>
<br />
<br />
While CloudWatch is gathering CPU data, we can go back to the instance and connect to it via EC2 Instance Connect.
<br />
<br />
<img src="https://imgur.com/eapmdYl.png" height="80%" width="80%"/>
<br />
<br />
<img src="https://imgur.com/axch7MK.png" height="80%" width="80%"/>
<br />
<br />
<img src="https://imgur.com/AY4TEat.png" height="80%" width="80%"/>
<br />
<br />
Installed the application, stress, on this EC2 instance to put artificial CPU load on the system in order to see how CloudWatch reacts.
<br />
<br />
To install stress, run the following command: sudo yum install stress -y
<br />
<br />
<img src="https://imgur.com/tRS8o1v.png" height="80%" width="80%"/>
<br />
<br />
To run the stress application, you type stress. You can also pull up the help menu by running the command stress --help
<br />
<br />
<img src="https://imgur.com/w60BQQC.png" height="80%" width="80%"/>
<br />
<br />
Now we'll run stress and specify the number of CPUs to use. To do this, type stress -c 1 -t 3600
<br />
<br />
This will run the stress for 3,600 seconds so we can see the metrics that are being monitored by CloudWatch.
<br />
<br />
<img src="https://imgur.com/wiK23UJ.png" height="80%" width="80%"/>
<br />
<br />
<img src="https://imgur.com/wiK23UJ.png" height="80%" width="80%"/>
<br />
<br />
Now we can go back to the CloudWatch console where the alarm that we've is, and create and click into it to view the metrics.
<br />
<br />
<img src="https://imgur.com/qPbE4vg.png" height="80%" width="80%"/>
<br />
<br />
<img src="https://imgur.com/LamDs0B.png" height="80%" width="80%"/>
<br />
<br />
Once CloudWatch detects the additional CPU load and the CPUUtilization is greather than or equal to the 15% threshold that we've set, the alarm state will change from OK to In Alarm.
<br />
<br />
The reason we don't see the alarm state change in the screenshot below is because it takes a few minutes between when the graph shows the CPUUtilization change and the actual alarm state change. However, it did in fact change to In Alarm in bright red letters.
<br />
<br />
<img src="https://imgur.com/Z5Q0D3J.png" height="80%" width="80%"/>
<br />
<br />
Now we can go back to the EC2 instance and exit out of the stress utility by pressing COMMAND+C.
<br />
<br />
By doing this, the artificial CPU load will be removed and the instance will gradually move back down to its normal levels.
<br />
<br />
<img src="https://imgur.com/3QVaW3x.png" height="80%" width="80%"/>
<br />
<br />
<img src="https://imgur.com/J2KFoFR.png" height="80%" width="80%"/>
<br />
<br />
As always, we will now clean up our work by deleting the alarm, terminating the instance, and deleting the CloudwatchSG security group.
<br />
<br />
<img src="https://imgur.com/WvvTK8S.png" height="80%" width="80%"/>
<br />
<br />
<img src="https://imgur.com/eFZjOI3.png" height="80%" width="80%"/>
<br />
<br />
<img src="https://imgur.com/dFqyDvt.png" height="80%" width="80%"/>
<br />
<br />
<img src="https://imgur.com/VwZpaZ7.png" height="80%" width="80%"/>
<br />
<br />
 
<h2>Simple Identity Permissions:</h2>

<p align="center">
<br />
Learning how to assign permissions to IAM users within.
<br />
<br />
The study material that I am using included some demo files to download that will be used later on, and a 1-Click Deployment.
<br />
<br />
The 1-Click Deployment will allow us to use CloudFormation to apply a template that will create an IAM named Sally. It will also create two S3 buckets and a managed policy.
<br />
<br />
<img src="https://imgur.com/cXUJGUy.png" height="80%" width="80%"/>
<br />
<br />
After creating the stack, we'll open up the demo yaml file inside Visual Studio to see what it does and the resources that it will create, along with the managed policy.
<br />
<br />
<img src="https://imgur.com/yUNXXKR.png" height="80%" width="80%"/>
<br />
<br />
Now we can go back to CloudFormation and see that the resources have been created within the stack.
<br />
<br />
<img src="https://imgur.com/xqvlliB.png" height="80%" width="80%"/>
<br />
<br />
Now if we open up the sally IAM user by clicking the link within the resources, we'll see that the IAM user, sally, has an attached managed policy which we'll utitlize next. This is the policy that was created with our deployment.
<br />
<br />
<img src="https://imgur.com/GkelLBq.png" height="80%" width="80%"/>
<br />
<br />
If we click on dashboard from our menu on the left, we can copy the IAM user sign-in link and then open up a private browser window to paste the link and go to it. This is so we aren't logged out of our current account when attempting to sign into the sally account.
<br />
<br />
<img src="https://imgur.com/q0xBmk9.png" height="80%" width="80%"/>
<br />
<br />
We need to get the username for Sally now. To do this, go back to CloudFormation > Outputs, and copy the username for sally.
<br />
<br />
<img src="https://imgur.com/YFyqu3C.png" height="80%" width="80%"/>
<br />
<br />
Paste the username and password, then we see we're prompted to create a new password. This is because of the managed policy attached to the IAM user.
<br />
<br />
<img src="https://imgur.com/q0xBmk9.png" height="80%" width="80%"/>
<br />
<br />
<img src="https://imgur.com/4Q0Mt5i.png" height="80%" width="80%"/>
<br />
<br />
Now that we're logged into the sally IAM user, we can maneuver around and see by the error messages that sally currently does not have any permissions assigned.
<br />
<br />
This just proves that an IAM user has no permissions when they first get created in an AWS account.
<br />
<br />
<img src="https://imgur.com/s6lf3CR.png" height="80%" width="80%"/>
<br />
<br />
<img src="https://imgur.com/EzGOTnY.png" height="80%" width="80%"/>
<br />
<br />
Since we now understand that, we'll open up one of our demo files than contains the file s3_fulladmin.json.
<br />
<br />
This is a JSON policy document that grants full access to any S3 actions on any S3 resource.
<br />
<br />
<img src="https://imgur.com/hMSijb5.png" height="80%" width="80%"/>
<br />
<br />
In order to assign this policy to our sally user as an inline policy, we will do the following:
<br />
<br />
Copy the text within the file > Go back to the IAM console > Select users on the left > Open the sally IAM users > Add permissions > Create inline policy
<br />
<br />
<img src="https://imgur.com/vUVd2OC.png" height="80%" width="80%"/>
<br />
<br />
<img src="https://imgur.com/SmGTNjY.png" height="80%" width="80%"/>
<br />
<br />
Next, select the JSON tab, delete the text that is already present and paste the text that was copied from our own JSON file.
<br />
<br />
Click review policy, name it (s3admininline), and create.
<br />
<br />
<img src="https://imgur.com/6s140DR.png" height="80%" width="80%"/>
<br />
<br />
<img src="https://imgur.com/xX7BADo.png" height="80%" width="80%"/>
<br />
<br />
Now if we go back to the private browser and click refresh, we can see that sally now has access to the S3 buckets.
<br />
<br />
<img src="https://imgur.com/KLxOi5V.png" height="80%" width="80%"/>
<br />
<br />
To demonstrate that we have full access to the buckets, we'll go into both the animalpics bucket and catpics bucket and upload one of the demo files that we downloaded at the beginning.
<br />
<br />
<img src="https://imgur.com/qLyiuzJ.png" height="80%" width="80%"/>
<br />
<br />
<img src="https://imgur.com/YDV98nQ.png" height="80%" width="80%"/>
<br />
<br />
<img src="https://imgur.com/aLNckdy.png" height="80%" width="80%"/>
<br />
<br />
<img src="https://imgur.com/GIwPH4d.png" height="80%" width="80%"/>
<br />
<br />
From here I'll focus on the catpics bucket, since it will be the same for each, just a different image.
<br />
<br />
We can click into the bucket, and click the open tab in the top right. This will open a new tab with the file that we uploaded into the bucket.
<br />
<br />
<img src="https://imgur.com/o269Y62.png" height="80%" width="80%"/>
<br />
<br />
The same process can be repeated in the animalpics bucket, and an image of a dog will appear. So now we have confirmed that we have full access to these buckets.
<br />
<br />
Next, we'll go back to the IAM console in the other browser, open up the sally user, and delete the s3admineinline inline policy that we added.
<br />
<br />
After doing so, we can see that we lose access to the S3 buckets that we previously had full access to.
<br />
<br />
<img src="https://imgur.com/R8KYZdH.png" height="80%" width="80%"/>
<br />
<br />
<img src="https://imgur.com/BB3bQRF.png" height="80%" width="80%"/>
<br />
<br />
Since our sally user has been returned to its previous state, we will attach a managed policy this time, specifically AllowALLS3ExceptCats.
<br />
<br />
This managed policy was created by the CloudFormation template we used at the beginning.
<br />
<br />
<img src="https://imgur.com/tMk8DMi.png" height="80%" width="80%"/>
<br />
<br />
<img src="https://imgur.com/VTpF11j.png" height="80%" width="80%"/>
<br />
<br />
<img src="https://imgur.com/RlLlrNA.png" height="80%" width="80%"/>
<br />
<br />
Once we've added that managed policy, we can see exactly what it does by clicking on it.
<br />
<br />
This particular policy allows any S3 actions on any resource, and denies any S3 actions on the catpics bucket and any objects in the catpics bucket.
<br />
<br />
<img src="https://imgur.com/ZMyUmNc.png" height="80%" width="80%"/>
<br />
<br />
If we go back to the sally user in the private browser, we will be able to interact with any of the buckets in S3 apart from the catpics bucket and anything that's inside the catpics bucket.
<br />
<br />
<img src="https://imgur.com/2fgIAjJ.png" height="80%" width="80%"/>
<br />
<br />
<img src="https://imgur.com/T4fBm3M.png" height="80%" width="80%"/>
<br />
<br />
If we go back to buckets and open the animalpics bucket, we are able to access it and can open the object thor.jpg, where we are able to see the photo of a dog.
<br />
<br />
<img src="https://imgur.com/7zYds5R.png" height="80%" width="80%"/>
<br />
<br />
<img src="https://imgur.com/MT8YrBa.png" height="80%" width="80%"/>
<br />
<br />
<img src="https://imgur.com/ryPjNLy.png" height="80%" width="80%"/>
<br />
<br />
Now we'll delete everything that we've created in this lesson just to gain experience with cleaning up resources.
<br />
<br />
First we'll delete the managed policy from the sally IAM user.
<br />
<br />
<img src="https://imgur.com/PROB81y.png" height="80%" width="80%"/>
<br />
<br />
Second, as the IAM admin user, empty the catpics and animalpics buckets in S3.
<br />
<br />
<img src="https://imgur.com/FI4cG3z.png" height="80%" width="80%"/>
<br />
<br />
Third, go back to our CloudFormation tab, select the IAM stack, and click delete.
<br />
<br />
<img src="https://imgur.com/ggylSUk.png" height="80%" width="80%"/>
<br />
<br />
 
<h2>IAM Groups:</h2>

<p align="center">
<br />
In this section, we'll use the same architecture that we had in the sally IAM user demonstration prior to this. But we'll migrate the permissions that the sally IAM user has from the user to a group that sally is a member of.
<br />
<br />
So once again, we'll use the 1-Click Deployment that was provided to us and create the new stack.
<br />
<br />
<img src="https://imgur.com/45DIzHr.png" height="80%" width="80%"/>
<br />
<br />
Now we'll go to the S3 console, click on the catpics bucket, and upload one of our demo files.
<br />
<br />
<img src="https://imgur.com/pHzqmNM.png" height="80%" width="80%"/>
<br />
<br />
We'll now do the same in the animalpics bucket.
<br />
<br />
<img src="https://imgur.com/yE4TRxd.png" height="80%" width="80%"/>
<br />
<br />
Once that's done, we'll go back to CloudFormation and do the following:
<br />
<br />
Click on Resources > Click on the sally user > Add permissions > Select AllowAllS3ExceptCats > Next > Add permissions
<br />
<br />
<img src="https://imgur.com/UdpVGaG.png" height="80%" width="80%"/>
<br />
<br />
<img src="https://imgur.com/BAAu8L1.png" height="80%" width="80%"/>
<br />
<br />
<img src="https://imgur.com/9uYHzqZ.png" height="80%" width="80%"/>
<br />
<br />
Navigate to the IAM dashboard, copy the IAM sign-in link for the general account, and open up a private browser window again.
<br />
<br />
<img src="https://imgur.com/pWDj8k0.png" height="80%" width="80%"/>
<br />
<br />
Return to CloudFormation, select Outputs, and copy the sallyusername.
<br />
<br />
<img src="https://imgur.com/UhLokfv.png" height="80%" width="80%"/>
<br />
<br />
Paste the username in the designated box in the private browser.
<br />
<br />
Return to CloudFormation again, select Parameters, and copy the sallypassword.
<br />
<br />
<img src="https://imgur.com/DdtjcAr.png" height="80%" width="80%"/>
<br />
<br />
Paste the password in the designated box in the private browser and sign-in.
<br />
<br />
<img src="https://imgur.com/syUG1xD.png" height="80%" width="80%"/>
<br />
<br />
We can navigate over to the S3 console to verify that sally has access to the buckets.
<br />
<br />
We see sally has access to the animalpics bucket, but not the catpics bucket, which was intentional.
<br />
<br />
<img src="https://imgur.com/hJttyh0.png" height="80%" width="80%"/>
<br />
<br />
<img src="https://imgur.com/8K6i1aQ.png" height="80%" width="80%"/>
<br />
<br />
Now we can go back to the other browser window where we logged into the general account as the IAM admin user and make the modifications to the permissions.
<br />
<br />
We'll change the permissions over to the using group rather than directly on the sally user.
<br />
<br />
So we will navigate over to the sally user. Remember this can be done by clicking on the resources tab in the CloudFormation stack, and following the sally user link.
<br />
<br />
Once there, we will remove the AllowAllS3ExceptCats managed policy from sally. This will remove all permissions sally had within S3.
<br />
<br />
Click user groups on the left hand side of the screen, then create group.
<br />
<br />
Name the group and attach the same managed policy that sally had directly on her user (AllowAllS3ExceptCats).
<br />
<br />
<img src="https://imgur.com/0Oui6bv.png" height="80%" width="80%"/>
<br />
<br />
<img src="https://imgur.com/EbLNv3x.png" height="80%" width="80%"/>
<br />
<br />
From here, we'll click add users, and add the sally IAM user to the group.
<br />
<br />
<img src="https://imgur.com/NS6U5Mk.png" height="80%" width="80%"/>
<br />
<br />
So now sally has been added to the developers group, and the developers group has an attached managed policy that allows them to access everything on S3 except the catpics bucket.
<br />
<br />
This can be verified just like before where we navigate over to the private browser where we're logged into the sally IAM user account, and confirm sally's access.
<br />
<br />
Lastly, it's time to clean up our account. In the developers group, we'll navigate to permissions and remove the AllowAllS3ExceptCats managed policy, empty the buckets in the S3 console, and delete the IAM stack in CloudFormation.
<br />
<br />

<h2>AWS Organizations:</h2>

<p align="center">
<br />
Here, we will create the AWS account structure that we'll be using for the rest of the study.
<br />
<br />
Login as the IAM admin user for the general AWS account. 
<br />
<br />
<img src="https://imgur.com/0Vwivue.png" height="80%" width="80%"/>
<br />
<br />
Move to the AWS Organizations part of the console and create an organization.
<br />
<br />
It will convert the standard AWS general account to be the management account of the organization.
<br />
<br />
<img src="https://imgur.com/zNgMnYg.png" height="80%" width="80%"/>
<br />
<br />
Now open a new web browser and login to the production AWS that we created at the beginning of this study.
<br />
<br />
Click the account dropdown in the top right corner and copy the Account ID for the production account.
<br />
<br />
Go back to the AWS general account, click Add an AWS account, Invite an existing AWS account, and paste the Account ID of the production account. Lastly, click Send invitation at the bottom of the page.
<br />
<br />
Go back to the production account and go to the AWS Organizations console.
<br />
<br />
<img src="https://imgur.com/3VL1SH2.png" height="80%" width="80%"/>
<br />
<br />
Select invitations from the toolbar on the left.
<br />
<br />
<img src="https://imgur.com/3V3w57k.png" height="80%" width="80%"/>
<br />
<br />
Accept the invitation.
<br />
<br />
<img src="https://imgur.com/ph3Sjp1.png" height="80%" width="80%"/>
<br />
<br />
Now the production account is a member of the AWS organization.
<br />
<br />
<img src="https://imgur.com/wbZ7NK4.png" height="80%" width="80%"/>
<br />
<br />
We can verify this by returning to AWS accounts within the AWS Organizations console, refreshing the page, and seeing both the general and production accounts.
<br />
<br />
Now let's role switch into the production account from the general account and vice versa.
<br />
<br />
We will need to manually add the role since we invited an existing account into the organization. You do not have to do this if you created a new account from within the organization.
<br />
<br />
<img src="https://imgur.com/qwbDIUW.png" height="80%" width="80%"/>
<br />
<br />
Go back to the production account window, navigate to the IAM console, select Roles, and we're going to create a role that can be assumed from the general account.
<br />
<br />
<img src="https://imgur.com/qQh9bQd.png" height="80%" width="80%"/>
<br />
<br />
<img src="https://imgur.com/flJwQ36.png" height="80%" width="80%"/>
<br />
<br />
<img src="https://imgur.com/lZOoGol.png" height="80%" width="80%"/>
<br />
<br />
<img src="https://imgur.com/HAq3aqq.png" height="80%" width="80%"/>
<br />
<br />
<img src="https://imgur.com/hskIXmR.png" height="80%" width="80%"/>
<br />
<br />
<img src="https://imgur.com/WqdBhIX.png" height="80%" width="80%"/>
<br />
<br />
<img src="https://imgur.com/JqZUtXz.png" height="80%" width="80%"/>
<br />
<br />
<img src="https://imgur.com/W05pk2W.png" height="80%" width="80%"/>
<br />
<br />
<img src="https://imgur.com/gmMnNY7.png" height="80%" width="80%"/>
<br />
<br />
<img src="https://imgur.com/0Hsx1QK.png" height="80%" width="80%"/>
<br />
<br />
<img src="https://imgur.com/bBFp9yO.png" height="80%" width="80%"/>
<br />
<br />
<img src="https://imgur.com/yQYTzZt.png" height="80%" width="80%"/>
<br />
<br />
<img src="https://imgur.com/aJlHx3y.png" height="80%" width="80%"/>
<br />
<br />
<img src="https://imgur.com/9auqWTw.png" height="80%" width="80%"/>
<br />
<br />
<img src="https://imgur.com/DF2mtOM.png" height="80%" width="80%"/>
<br />
<br />
<img src="https://imgur.com/jJydFH4.png" height="80%" width="80%"/>
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
