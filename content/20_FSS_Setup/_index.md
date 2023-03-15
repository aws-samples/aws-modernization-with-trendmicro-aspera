---
title: "Deploy File Storage Security"
chapter: true
weight: 30
pre: "<b>5. </b>"
---


# Deployment

---

![Diagram](/images/aspera/MicrosoftTeams-image.png)

---

### Cloud One - File Storage Security Deployment

**1.** Login to [Cloud One platform](https://cloudone.trendmicro.com). If you don’t have your login information, check the requirements page that has all the details that you will need to create your account.
![Diagram](/images/fss/login.png)

---

**2.** Select the File Storage Security tile
![Diagram](/images/fss/login_2.png)

---

**3.** Click on Stack management in your left side
![Diagram](/images/fss/login_3.png)

---

**4.** Click on "Deploy" 
![Diagram](/images/fss/login_4.png)

---

**5.** Select ```Scanner Stack and Storage Stack```, to deploy the full solution to your AWS account.

![Diagram](/images/fss/fss-deploy-stacks-select.png)

---

**6.** Select the **us-east-1** AWS region and click on ```Launch Stack```, this will redirect you to your AWS account in the region that you choose to deploy the stack. Make sure that you're logged in and have the correct permissions, which you can check the details of the permissions required in the Requirements section.

{{% notice tip %}}
Try to make sure the Cloud One console tab is in the same Window from your browser so the Launch Stack will automatically use the AWS session that you have open already. 
{{% /notice %}}

You can validate the Cloud Formation Template by clicking in ```Review Stack```, to make it easier, you can also verify the Cloud Formation Template by clicking the buttons below:

{{% button href="https://github1s.com/trendmicro/cloudone-filestorage-cloudformation-templates/blob/master/aws/FSS-All-In-One.template" %}}All in One Template{{% /button %}}
{{% button href="https://github1s.com/trendmicro/cloudone-filestorage-cloudformation-templates/blob/master/aws/FSS-Scanner-Stack.template" %}}Scanner Stack{{% /button %}}
{{% button href="https://github1s.com/trendmicro/cloudone-filestorage-cloudformation-templates/blob/master/aws/FSS-Storage-Stack.template" %}}Storage Stack{{% /button %}}

![Diagram](/images/fss/login_5.png)

---

**7.** In the CloudFormation page the <b>only required parameter</b> here is the <b>name of bucket</b> that you choose to be scanned.

- Please use the name from the S3 bucket that was created earlier. The bucket starting with **aspera-transfer**.

- It also supports different parameters to customize your installation, like Resource prefixes and optional KMS integration, for more details about these configurations check our <a href="https://cloudone.trendmicro.com/docs/file-storage-security/gs-deploy-all-in-one-stack/">Documentation</a>.

- After adding the bucket name you will need to acknowledge and click on <b>"Create Stack"</b>

![Diagram](/images/fss/cfdeploy.png)

---

**8.** After deploying the all-in-one stack in your AWS account, you must configure the scanner and storage stack Amazon Resource Names (ARNs) information in Cloud One console. The ARNs map a scanner stack to a storage stack, allowing them to be aware of each other.

Go to CloudFormation > Stacks > your all-in-one stack > Outputs tab and copy the Value with these Key names here ```ScannerStackManagementRoleARN``` and ```StorageStackManagementRoleARN``` and paste the information into Cloud One - File Storage Security console.

![Diagram](/images/fss/fss-arn-aws-info.png)

![Diagram](/images/fss/login_6.png)

---

**9.** Then Click <b>Submit</b>. You see a couple of success messages at the bottom and the stack will show in the Stack Management too. 

![Diagram](/images/fss/login_7.png)

You have now completed the deployment of the All-in-One stack :tada:, so let's test our deployment :laptop:

All new objects uploaded to your bucket that you define to be scanned will now be automatically scanning against malware and tagged as “malicious” or “no issues found”.


---



