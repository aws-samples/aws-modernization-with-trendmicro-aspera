---
title: "Transfer and Validate"
chapter: true
weight: 50
pre: "<b>6. </b>"
---

# Transfer Files using Aspera

**1.** Return to the RDP connection.

<details>
  <summary> -> <code>CLICK HERE</code> if RDP Session timed out.</summary>

**AWS Console -> EC2 -> Instances -> Select the EC2 Aspera instance**
- Click **Connect**.
- Select the **RDP tab**.
- Download the RDP client.
- Decrypt your password using the KeyPair file download earlier.

![DEPLOY](/images/aspera/rdp.jpg) 
![DEPLOY](/images/aspera/rdp2.jpg)
![DEPLOY](/images/aspera/rdp3.jpg)

</details>
<br>

---

**2.** If needed sign into your IBM Aspera Account.

- IBM Aspera sign in url: ```https://myibm.ibm.com/?lnk=mmi```

---

**3.** Use the App Switch in the top right (9 dot icon top-right).
- Select **Files**.
- If not selected, **select our newly created workspace**.

![DEPLOY](/images/aspera/transfer.jpg) 
![DEPLOY](/images/aspera/transfer2.jpg)

---

**4.** Upload folder..
- Select **New**.
- Select **Upload Folder**.
- Provided on the desktop is a folder called **data**.
- Select the data folder to upload content.

![DEPLOY](/images/aspera/transfer2.jpg)

---

![DEPLOY](/images/aspera/transfer3.jpg)

---

![DEPLOY](/images/aspera/transfer4.jpg)  


---
## Check the S3 bucket for new objects.

- Ensure that the transfer has completed.
![DEPLOY](/images/aspera/bucket.jpg)
![DEPLOY](/images/aspera/files.png) 


---