---
title: "Cleanup"
chapter: true
weight: 70
pre: "<b>8. </b>"
---

# Clean your Environment

1. To clean your environment, go to your CloudFormation stack called ```All-in-one-TM-FileStorageSecurity``` and click in delete, this will automatically delete the Scanner and Storage stack all together:

2. After the CloudFormation has finish the deletion process (usually takes up to 5 minutes), you can go back to the File Storage Security console and select your stack and also delete the stack.

3. Delete all objects out of both s3 buckets.

4. Delete both S3 buckets.

5. Delete the ```Serverless-Promote-Quarantine-Plugin``` stack.

6. Delete the ```aspera-client-template``` stack.

Done:tada:! You have successfully cleaned up your environment