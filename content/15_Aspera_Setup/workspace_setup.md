---
title: "Configure Client Workspace"
chapter: true
weight: 22
pre: "<b>4.3 </b>"
---

# Configure Aspera Workspace

**1.** Navigate to EC2 and establish an RDP connection.


- **AWS Console -> EC2 -> Instances -> Select the EC2 Aspera instance**
- Click **Connect**.
- Select the **RDP tab**.
- Download the RDP client.
- Decrypt your password using the KeyPair file download earlier.

![DEPLOY](/images/aspera/rdp.jpg) 
![DEPLOY](/images/aspera/rdp2.jpg)
![DEPLOY](/images/aspera/rdp3.jpg)


---

**2.** In the RDP session, use Firefox to sign into your IBM Aspera Account.

- IBM Aspera sign in url: ```https://myibm.ibm.com/?lnk=mmi```

![DEPLOY](/images/aspera/agent.jpg)

**1.** Launch Aspera on Cloud.

- Click **Launch** to be directed to IBM Aspera on Cloud.

![Aspera](/images/aspera/account.jpg)

**3.** Authenticate to IBM Aspera on Cloud.

- Click on **Log in with IBMid**.
- Click On **Files**.

![Aspera](/images/aspera/aspera.jpg)
![Aspera](/images/aspera/aspera2.jpg)

---

**3.** Install Aspera Browser Extension.
- Click **Install Extension**.

![DEPLOY](/images/aspera/agent2.jpg)
![DEPLOY](/images/aspera/agent3.jpg)
![DEPLOY](/images/aspera/agent4.jpg)

---

**4.** Install the Aspera Connect Client.
- The **Aspera MSI Package is already provided on the Desktop**. Double click to start the wizard.

<details>
  <summary> -> <code>CLICK HERE</code> to wizard install image walkthrough.</summary>

**Accept all defaults**

![DEPLOY](/images/aspera/wiz.jpg) 
![DEPLOY](/images/aspera/wiz2.jpg)
![DEPLOY](/images/aspera/wiz3.jpg)
![DEPLOY](/images/aspera/wiz4.jpg) 
![DEPLOY](/images/aspera/wiz5.jpg)
![DEPLOY](/images/aspera/wiz6.jpg)

</details>
<br>

---

## Set up Transfer Workspace
---

**1.**  In the Aspera portal, navigate to **Admin page > Workspaces**.
- Click **Create New**.

![DEPLOY](/images/aspera/ws.jpg)

---

**2.** Create a new workspace!
- Name: ```immersion-workspace```
- Storage location: ```select your s3 bucket```
- Leave the rest as deafult.
- **Create**.
![DEPLOY](/images/aspera/ws2.jpg)

---

3. Add a member.
- Click the **members tab**.
- Click **Add members**.
- Type your email and select yourself.

![DEPLOY](/images/aspera/ws3.jpg)
![DEPLOY](/images/aspera/ws4.jpg) 
![DEPLOY](/images/aspera/ws5.jpg)


---

Let's start the File Storage Security deployment now. :laptop::cloud::rocket: