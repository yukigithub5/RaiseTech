# 第10回講義  
## 講義内容  
* インフラ自動化  
* 自動化のメリット  
* 全自動と半自動  
* 自動化の範囲  
* Cloudformation  
* CloudFormationテンプレートの解説  
## 課題内容  
* CloudFormationを利用して現在まで作った環境をコード化する  

 | Stacks | リソース | Export情報 |
 | --- | --- | --- |
 | CloudFormationVPC | VPC | VPC-ID |
 | | PublicSubnet1 | PublicSubnet1ーID |
 | | PublicSubnet2 | PublicSubnet2ーID |
 | | PrivateSubnet1 | PrivateSubnet1ーID |
 | | PrivateSubnet2 | PrivateSubnet2ーID |
 | | IGW | |
 | | RouteTable | |
 | | Route | |
 | | VPCENDpoint | MyVPCENDpoint‐ID |
 | CloudFormationSecurityGroup | EC2securityGroup | EC2securityGroupーID |
 | | RDSsecurityGroup | RDSsecurityGroupーID |
 | | ALBsecurityGroup | ALBsecurityGroupーID |
 | CloudFormationIAMRole | IAMRole | S3AccessInstanceProfile-ID |
 | | Instanceprofile | |
 | CloudFormationEC2 | EC2Instance | MyEC2-ID |
 | | Keypair | |
 | CloudFormationRDS | DBinstance | |
 | | DBSubnetGroup | |
 | S3 | S3Bucket | MyS3bucket-ID |
 
* 作成済みのStacks  
 ![Stacks](IMG/stacks.png)  
* VPC構成  
 ![VPC](IMG/CFNVPC.png)  
* EC2Login＆MySQLLogin  
 ![Log](IMG/CFNMySQLlogin.png)  
* ALB接続確認  
 ![Nginx](IMG/CFNNginx.png)  
* S3作成済み  
 ![S3](IMG/CFNS3.png)  
## 構成図  
 ![AWSbuild](IMG/AWS.CFNdrawio.png)  