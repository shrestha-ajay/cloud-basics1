## Tutorial on different ways of interacting with AWS (APIs) to create resources

This Cloudformation template creates an Amazon EC2 instance running the Amazon Linux AMI. The AMI is chosen based on the region in which the stack is run. This example creates an EC2 security group for the instance to give you SSH access. 

**WARNING** This template creates an Amazon EC2 instance. You will be billed for the AWS resources used if you create a stack from this template.


### Steps:
1. Fork this repository by clicking on "Fork". 
2. Clone this repository to your local computer by running following:

   ```$ git clone git@github.com:YOUR-USERNAME/YOUR-REPOSITORY.git```
3. Configure AWS CLI in your local machine
4. Run the following command to create the ec2 instance and security group in your AWS account


```
 aws cloudformation deploy \
  --stack-name my-cloudbasic-ec2 \
  --template-file ec2_securitygroup.template \
  --parameter-overrides KeyName=YOUR-EC2-KEYPAIR-NAME
  ```

  Note: Replace "YOUR-EC2-KEYPAIR-NAME" KeyName with your EC2 KeyPair name


### Related Resources: 
1. https://towardsdatascience.com/cloud-basics-interacting-with-aws-da179d3f5829
2. https://s3.us-west-2.amazonaws.com/cloudformation-templates-us-west-2/EC2InstanceWithSecurityGroupSample.template
