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

- Heidi SQL
- MySQL 5.5.62
- osTicket-v1.15.8
- php7.3.8 
- PHP Manager
- Rewrite Module 
- VC_redistx86 

- <i>All of these files can be found in osTicket documentation.</i>

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

<h3>Enable IIS</h3>
<p>
  
- Open the **Control Panel**.

<img width="816" height="885" alt="7" src="https://github.com/user-attachments/assets/c043bb14-c848-404f-b8f8-4d1081d013e1" />

- Select **Uninstall a program** under the **Programs** section.

- On the left-hand side, click **"Turn Windows features on or off."**  
  This should bring you to the following window:

 <img width="412" height="361" alt="8" src="https://github.com/user-attachments/assets/3ad0ac10-9448-4ec2-8389-bc04c7fc026a" />

- Check **Internet Information Services** (click the checkbox until it turns black), then expand it by clicking the **plus (+)** sign next to it.

<img width="378" height="380" alt="9" src="https://github.com/user-attachments/assets/8fcc3cf4-470b-4d06-a1cc-33f50f27a864" />

- Navigate to:  
  **World Wide Web Services** → **Application Development Features** → check **CGI**, then click **OK**.

- To verify that IIS is running correctly, open a web browser and go to `http://127.0.0.1`.  
  If everything was configured properly, you should see a page like this:

<img width="926" height="1010" alt="10" src="https://github.com/user-attachments/assets/ceb962c0-b5ca-49a4-909f-c6b796657788" />

</p>

<br />

<h3> Install PHP Manager </h3>

<img width="1179" height="736" alt="11" src="https://github.com/user-attachments/assets/e3c41eed-24e6-46b6-b3eb-ea1f7f7e2b06" />

<br>

<h3> Install Rewrite Module </h3>

<img width="1190" height="711" alt="12" src="https://github.com/user-attachments/assets/3231fc98-7e83-4b12-8462-e7e1a28557cf" />

<br>

<h3> Create the directory </h3>
<p>
  
- Let's open Windows (C:) and create a new file called "PHP"

<img width="1200" height="707" alt="13" src="https://github.com/user-attachments/assets/bacae6d2-28c7-40d6-a5a4-1aed572bbd1e" />

- Next we will unzip or move our PHP7.3.8 File to the PHP Folder we just created.

<img width="1844" height="661" alt="14" src="https://github.com/user-attachments/assets/62e9922b-b960-4f2d-aab2-59fa9b9368ca" />
<img width="979" height="595" alt="15" src="https://github.com/user-attachments/assets/3a718364-497c-4051-b6a0-57f86d175ee0" />
  
</p>
<br> 

<h3>Install VC_redist</h3>
<img width="1139" height="666" alt="16" src="https://github.com/user-attachments/assets/c9dd65e9-1c58-4ed0-ac08-4a16bb368034" />

<br>

<h3> Install and setup MySQL </h3>
<p>
<img width="1147" height="685" alt="17" src="https://github.com/user-attachments/assets/86f55028-7859-4fd6-89d2-6e9d25fc76f1" />

- Launch the **MySQL Instance Configuration Wizard**.

- Select **"Standard Configuration"**, then click **Next**, and click **Next** again on the following screen.  
  You should now see this page:

  <img width="1148" height="676" alt="18" src="https://github.com/user-attachments/assets/f2b95147-8c7b-467a-bde2-1cb8df1a04f5" />

- Set a **password** and make sure to write it down — you'll need it later.  
  For this tutorial, we’ll use `"root"` as the password.
  
- Click **Next**, then click **Finish** once the configuration process completes.

</p>
<br> 

<h3> Register PHP </h3>
<p>

- Open **IIS (Internet Information Services)**.

<img width="819" height="657" alt="19" src="https://github.com/user-attachments/assets/c961a237-7d9a-43ca-a8be-16eddbfbc834" />

- In the **IIS Manager**, open **PHP Manager**.

<img width="1451" height="778" alt="20" src="https://github.com/user-attachments/assets/ed552d40-a8b3-4476-8866-951bb092668b" />

- Click **"Register new PHP version."**

- Navigate to your PHP installation folder and select the `php-cgi.exe` file.

<img width="1822" height="753" alt="21" src="https://github.com/user-attachments/assets/c7d9687a-e578-4922-a38a-8d9a46d6f0a3" />

- Now, stop the web server by clicking **"Stop"** in the right-hand pane.

<img width="1425" height="752" alt="22" src="https://github.com/user-attachments/assets/3bd9b872-6b1a-4865-b7cf-cdc5da8e9d49" />

- Wait a few moments, then click **"Start"** to restart the web server.
  
</p>
<br>

<h3> Install osTicket </h3>
<p>

- Extract the `osTicket-v1.15.8` file.  
  If it's already unzipped, you can disregard this step.

<img width="1136" height="790" alt="23" src="https://github.com/user-attachments/assets/0c825eb8-bf5b-4dd3-8926-6a5031943dc0" />

- Open **File Explorer**, go to `Windows (C:)` → open the `inetpub` folder → then the `wwwroot` folder.

- Copy the **`upload`** folder from the osTicket files into the `wwwroot` folder.

<img width="1864" height="661" alt="24" src="https://github.com/user-attachments/assets/4498bfbe-4566-43a8-b519-080f019718ca" />

- Rename the **`upload`** folder to **`osTicket`**  
  *(must be typed exactly as shown — case-sensitive in some systems).*

<img width="825" height="629" alt="25" src="https://github.com/user-attachments/assets/82449312-7602-44eb-b838-522ce050a3d4" />

- Go back to **IIS**, and stop then start the web server again to apply the changes.

<img width="1425" height="746" alt="26" src="https://github.com/user-attachments/assets/fe0da611-360f-4679-94dd-1fb962b4a101" />

</p>
<br>

<h3>Open osTicket in Browser</h3>
<p>
  
- Make sure **IIS** is open and running **as Administrator**.

- In the **Connections** panel on the left, expand the top option — this should be the name of your virtual machine (in this example, it's `osticket-vm`).  
  Click the small arrow to expand it.

- Navigate to:  
  `Sites` → `Default Web Site` → click on the **osTicket** folder.

- On the right-hand side, click **"Browse *:80 (http)"**.

<img width="1425" height="750" alt="27" src="https://github.com/user-attachments/assets/f698aad9-5afe-47cd-9a4c-6bef49fe4177" />

- If everything in the tutorial has been done correctly so far, you should now see the osTicket installer page:

<img width="929" height="1004" alt="28" src="https://github.com/user-attachments/assets/43a5b9e9-2e68-475b-b711-c2382e3006a2" />

- If you **don’t** see this page, I recommend going back and reviewing each step carefully — even a small misconfiguration can prevent this screen from loading.

</p>
<br>

<h3>Enable Extensions</h3>
<p>
  
- Back in **IIS**, while still in the **osTicket** folder, click **PHP Manager**.

<img width="1425" height="750" alt="29" src="https://github.com/user-attachments/assets/39a7c9ce-73e3-4d00-a15f-ec7a305ad631" />

- Under **PHP Extensions**, click **"Enable or disable an extension."**

- Enable the following extensions by selecting and enabling them:

  - `php_imap.dll`  
  - `php_intl.dll`  
  - `php_opcache.dll`

<img width="1918" height="1039" alt="30" src="https://github.com/user-attachments/assets/82ccf110-e26e-4e78-9c0a-840e5690fbcb" />

- Once those are enabled, refresh the osTicket page in your browser.  
  It should now look like this, with fewer warnings and a green check next to required extensions:

<img width="918" height="1007" alt="31" src="https://github.com/user-attachments/assets/b70662b1-dd0d-41f4-ab49-058b595b24aa" />

</p>
<br>

<h3></h3>
<p>
  
</p>
<br>
