<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation steps for osTicket, an open-source help desk ticketing system.
This specific guide is designed for a broad audience — from non-technical users to IT professionals — making it accessible regardless of your technical background.
<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b>

<h2>List of Prerequisites</h2>

- IIS
- PHP Manager 
- VC_redistx86 
- MySQL 5.5.62 
- Rewrite Module
- Heidi SQL

<h2>Installation Steps</h2>

<h3> Create a Virtual Machine </h3>
<p>
<b>Disclaimer:</b> Creating a virtual machine is an <i>optional</i> step in this tutorial. osTicket can be installed on a personal desktop. For the purpose of this tutorial, we will be creating a Windows 10 virtual machine.
</p>
<p>
  
- Select "Create a virtual machine" in Azure.

- This will take you to the setup screen shown below:

<img width="1065" height="886" alt="1" src="https://github.com/user-attachments/assets/67ae3377-57d5-41b2-b518-764163ffd657" />

- During the setup process, create a new **resource group** and give it a name of your choice.

- Make sure to name your resource group clearly for easy identification.

- Under the **Image** section, select **Windows 10** as the operating system for your virtual machine.

- Scroll down and choose a **size** that includes at least **2 vCPUs**.

- Under **Administrator account**, enter a **username** and **password** — you'll need this information later to access your VM.

- At the bottom of the page, check the box that says:  
  *“I confirm I have an eligible Windows 10/11 license with multi-tenant hosting rights”* under the **Licensing** section.
</p>

<br />

<h3> Validation </h3>
<p> 
  
- Once all required fields are filled out correctly, click **Review + create** at the bottom of the page.

- You should see a screen like this:
<img width="425" height="881" alt="2" src="https://github.com/user-attachments/assets/1b2e7142-68e2-46d2-8415-3d0017c8ecbb" />

- Azure will automatically create a **virtual network** for your virtual machine.

- Once **validation passes**, you’re good to go — click **Create** to start the deployment.
</p>

<br />

<h3> Get public IP address </h3>
<p>
  
- Here is the **overview** of our virtual machine:
  
<img width="1890" height="875" alt="3" src="https://github.com/user-attachments/assets/095deb0a-34fb-47c2-be48-4f60dd37a914" />
  
- Copy or note down the **Public IP address** — you’ll need it to connect to the VM.

- Make sure you have **Microsoft Remote Desktop** (or the **Windows App**) installed on your desktop.  
  This will allow you to open and access your virtual machine.

  </p>
<br>

<h3> Add PC </h3>
<p>
  
- Add a PC through the **Microsoft Remote Desktop** or **Windows App**.
  
<img width="1410" height="716" alt="4" src="https://github.com/user-attachments/assets/ea478d66-eee2-4298-9c6a-c4df8d2c8022" />

- You will then be prompted to enter a **PC Name** — this is where you input the **IP address** from the previous step.

- In the next prompt, enter the **username and password** you created for the virtual machine.

<img width="1913" height="1072" alt="5" src="https://github.com/user-attachments/assets/b5afde8f-62f0-48d1-b668-0e9aff522025" />

- You should now be connected to your virtual machine!
  
</p>

<br />

<h3></h3>

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
