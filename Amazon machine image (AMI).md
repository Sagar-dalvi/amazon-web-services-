## AMI (Amazon machine image)
*AMI:- An Amazon Machine Image (AMI) is used to create virtual servers 
(Amazon Elastic Compute Cloud or EC2 instances) in the Amazon Web Services (AWS) environment.
Different types of instances can be launched from a single AMI to support the hardware of the host computer used for the instance.
- AMIs are a regional resource. Therefore, sharing an image makes it available in that Region.
To make an image available in a different Region, copy the AMI to the Region and then share it.
AMIs with encrypted volumes cannot be made public.

**WHY DO WE NEED AMI?**
-Let us suppose that we want to launch 5 servers with the same configuration.
One way of doing that would be to launch a new EC2 instance every time and install the required packages every time.
The other way of doing it would be to configure your EC2 instance once and then create an image of that instance.
Using that image you can deploy four more EC2 servers. 

##Steps for creating and copying AMI :
-Step 1 :- Create an ec2 instance then connect it with CLI and create some files in it.
-Step 2 :- Go to aws ec2 instances console Select the instance whose ami u want to create.
-Step 3 :- Click on actions image and templates  create image  then create AMI.
           Now you can use that AMI in your instance where u want (u can use it in the same region now).
-Step 4 :- (Copy AMI from one region to another region)  Go to the ec2 console, on the left side u find images  
           AMI  click on AMI then Select  AMI  Actions  Copy AMI  Select the destination (region u want) and copy AMI. 
-Step 5 :- Now go to that region which is u selected above then create a new instance select the AMI that u created and launch an instance.


	**Copy and Access the AMI from one AWS account to another**
Step 1 :- Go to  EC2  AMI then select the AMI u want to share with another account.
Step 2 :- Edit AMI permission  add Volume  Select private  add account ID  select account-id  save changes.
Step 3 :- (On another account whose account-id is added in the above step) At the top right corner of the AMI console on the dropdown select private images then u can see the AMI that is shared.
Step 4 :- you can launch an instance with that AMI and see the file, etc of that instance.
