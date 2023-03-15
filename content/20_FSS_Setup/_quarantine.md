---
title: "Quarantine Malicious Files"
chapter: false
weight: 31
pre: "<b>5.2 </b>"
---

### Enhance Security workflow with Quarantine functionality.

---

![Diagram](/images/aspera/arch-aws-flow.png)

---

**1.** **Find the 'ScanResultTopic' SNS topic ARN**

- In the AWS console, go to **Services > CloudFormation > your all-in-one stack > Outputs**.
- Scroll down to locate the  **ScanResultTopic** Logical ID.
- Copy the **ScanResultTopic** ARN to a temporary location. It will look like this: `arn:aws:sns:us-east-1:123445678901:FileStorageSecurity-All-In-One-Stack-StorageStack-1IDPU1PZ2W5RN-ScanResultTopic-N8DD2JH1GRKF`

![Diagram](/images/aspera/outputs.jpg)

---

### Deploying Post Scan Action (Functions) - Promote and Quarantine

In this case, let's use the Serverless Application Repository

1. Visit [the app's page on the AWS Lambda Console](https://us-east-1.console.aws.amazon.com/lambda/home?region=us-east-1#/create/app?applicationId=arn:aws:serverlessrepo:us-east-1:415485722356:applications/cloudone-filestorage-plugin-action-promote-or-quarantine).
2. Fill in the parameters:
    * ScanResultTopic
    * ScanningBucketName - **aspera-transfer-01234567890**
    * PromoteBucketName - **Ignore**
    * QuarantineBucketName- **quarantine-01234567890**
    * Optionally, you can customize the name of the Cloud Formation stack that will be created
3. Check the `I acknowledge that this app creates custom IAM roles.` checkbox.
4. Click `Deploy`.

![Diagram](/images/fss/scan_action_1.png)

![Diagram](/images/fss/scan_action_3.png)

----

**2.** After a couple minutes you can click on the tab Deployments and expand the deployment to see if the status shows as complete. Then you can move to the next step to test it.

![Diagram](/images/fss/scan_action_4.png)


---

<b>Awesome, You did it! :tada: </b>
        


