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



      
