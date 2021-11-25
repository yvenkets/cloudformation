# cloudformation

Create the ec2 instance from your cutom ami save the bewlow code as yaml(.yml   file.

```
AWSTemplateFormatVersion: "2010-09-09"
Resources:
  WebInstance:
    Type: AWS::EC2::Instance
    Properties:
      InstanceType: t2.nano
      ImageId: ami-06a627b7e24024728
      KeyName: deep
      SecurityGroupIds:
        - sg-05562793e4c3b2f37
      SubnetId: subnet-e8b7e4a4
```    

create cloudformation stack then upload the yml file in that page.
for more info

https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-instance.html#cfn-ec2-instance-imageid

Run this in AWS CLi
Install aws cli
configure with your iam user credentials
place your yaml file in your pc local location.
validate the template

aws cloudformation validate-template --template-body file://c:/shivam.yml

run the template

aws cloudformation create-stack --stack-name shivamnew --template-body file://c:/shivam.yml


to list aws cloud formation stacks

aws cloudformation list-stacks --stack-status-filter CREATE_COMPLETE

to delete cloudformation stacks

aws cloudformation delete-stack --stack-name myteststack
      
