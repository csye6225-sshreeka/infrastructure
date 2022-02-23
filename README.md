T
#Task : Infrastructure Setup through Cloud Formation
1. Create a Virtual Private CLoud (VPC)
2. Create 3 subnets according to the requirements in the VPC with each in different availability zones
3. Create a Internet Gateway
4. Attach the Internet Gateway to VPC
5. Create a Public Route-Table and attach all the 3 subnets to the Route-Table
6. Create a public Route in the Public Route-Table with Destination Cidr BLock of 0.0.0.0/0 and connect to internet gateway as well.


#Setup Steps

1. Install AWS Command Line Interface
2. run aws configure command and enter all the credentials for the root user.

#Run 

To verify template: aws cloudformation validate-template  --template-body file://csye6225-infra.yml --region  us-east-1 --profile dev                  
To create stack: aws cloudformation create-stack --stack-name stack_name  --template-body file://csye6225-infra.yml  --region  us-east-1 --profile dev
To delete stack: aws cloudformation delete-stack --stack-name stack_name  --template-body file://csye6225-infra.yml  --region  us-east-1 --profile dev
