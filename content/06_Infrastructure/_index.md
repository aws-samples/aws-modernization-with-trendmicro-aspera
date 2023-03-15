---
title: "Required Infrastructure"
chapter: true
weight: 6
pre: "<b>2. </b>"
---


# Workshop Client Setup

---
 **1** Create an EC2 Keypair.

- **AWS Console -> EC2 -> Key Pairs -> Create key pair**

![DEPLOY](/images/aspera/kp.jpg) 
![DEPLOY](/images/aspera/kp2.jpg)

 ---

  **2.** Launch the CloudFormation template in a new tab. The template deploys the IBM Aspera Connect client package and mock data to use for testing. 

[![Launch Stack](https://cdn.rawgit.com/buildkite/cloudformation-launch-stack-button-svg/master/launch-stack.svg)](https://console.aws.amazon.com/cloudformation/home#/stacks/new?stackName=c1fss-aspera-workshop-instance&templateURL=https://immersionday-workshops-trendmicro.s3.amazonaws.com/aspera/templates/aspera_instance.yml)

 - Click the **Launch Stack** button.
 - Select your **KeyPair** created in the previous step.
 - Click **Next**.
 - Click **Next**.
 - Check the box for IAM acknowledgement.
 - Click **Submit**.

![DEPLOY](/images/aspera/cft.jpg) 
![DEPLOY](/images/aspera/cft2.jpg)

{{% notice info %}}
<p style='text-align: left;'>
A Key Pair is required before continuing this CloudFormation deployment. If you need help creating a Key Pair -> <a href="https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-key-pairs.html#having-ec2-create-your-key-pair" target="_top">Create a key pair</a>
</p>
{{% /notice %}}

---

**3. This machine will be used later.**

![DEPLOY](/images/aspera/ec2.jpg)
![DEPLOY](/images/aspera/ec2-outputs.jpg)
---

### S3 Bucket Creation

---

{{% notice warning %}}
<p style='text-align: left;'>
If attending this workshop with Trend Micro. The S3 buckets have already been deployed for you in the Event Engine Account provided. Skip over this launch stack button below.
</p>
{{% /notice %}}

This template creates two S3 buckets. A source S3 bucket to configure with Aspera and FSS. The other to quarantine files marked by FSS.

[![Launch Stack](https://cdn.rawgit.com/buildkite/cloudformation-launch-stack-button-svg/master/launch-stack.svg)](https://console.aws.amazon.com/cloudformation/home#/stacks/new?stackName=c1fss-aspera-buckets&templateURL=https://immersionday-workshops-trendmicro.s3.amazonaws.com/aspera/templates/aspera_lab_buckets.yml)

<details>
  <summary> -> <code>CLICK HERE</code> to see steps to create the Stack above.</summary>

**1.** Clicking Launch Stack will direct you to AWS Cloudformation.
- Accept all the defaults.
- Click **Next**
- Create Stack.

![DEPLOY](/images/aspera/lab_buckets.jpg)
![DEPLOY](/images/aspera/lab_buckets_outputs.jpg)

---


</details>
<br>

---
