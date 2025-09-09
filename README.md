<p align="center">
  <img src="https://logo.svgcdn.com/l/microsoft-azure.svg" alt="Microsoft Azure Logo" width="150"/>
</p>

<h1>Azure Website Deployment & DevTest Lab Project</h1>
This project demonstrates deploying Linux web servers in multiple regions on Microsoft Azure and creating a DevTest Lab with virtual machines. The goal is to gain hands-on experience with Azure VM deployment, networking, web server setup, and test lab automation.

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute, DevTest Labs)
- PuTTY (SSH Client)
- Apache Web Server
- Linux (Ubuntu Server)
- HTML Webpage deployment

---

<h2>Operating Systems Used</h2>

- Ubuntu Server 20.04 LTS

---

<h2>Project Overview</h2>

1. **Deploy multi-region Linux web servers**
   - Two servers in Canada region
   - Two servers in U.S. region
   - Configured Apache web server
   - Created custom HTML webpage displaying student info

2. **Configure networking and security**
   - Opened inbound HTTP (80) and HTTPS (443) ports
   - Configured firewall rules
   - Verified public IP connectivity

3. **DevTest Lab setup**
   - Created DevTest Lab in Azure
   - Added Windows Server 2022 VM
   - Demonstrated lab automation (start/stop scheduling)

---

<h2>Azure VM Deployment Steps</h2>

<h2>Task 1: Deploy Website using Azure</h2>
<p>As the Azure administrator, your company has requested you deploy a website using Azure. You are to deploy two (2) Linux servers in the U.S. region and two (2) Linux servers in the Canada region.</p>

<h3>Step 1: Use the Azure Pricing Calculator</h3>
<p>Before you begin, ensure that you have reviewed the Azure for students’ registration document and signed up for the Azure for Students Credit.</p>

<h4>Virtual Machines (VMs)</h4>
<p>A Virtual Machine is like a pretend computer that lives inside the cloud. You don’t need real hardware; Azure provides one that works online.</p>
<div class="example"><strong>Example:</strong> Run a website without buying a physical server.</div>

<h4>App Service</h4>
<p>Azure App Service hosts your web or mobile apps and scales automatically based on traffic.</p>
<div class="example"><strong>Example:</strong> Host a blog or online shop with automatic updates.</div>

<h4>Azure Functions</h4>
<p>Serverless compute service that executes code on-demand.</p>
<div class="example"><strong>Example:</strong> Send an email when a user signs up without running a full server.</div>

<h4>Storage Accounts</h4>
<p>Online storage for files, backups, and data.</p>
<div class="example"><strong>Example:</strong> Store thousands of photos securely.</div>

<h4>Azure Cosmos DB</h4>
<p>Global, fast, and scalable database.</p>
<div class="example"><strong>Example:</strong> Multiplayer game with data synchronized worldwide.</div>

<h4>Azure SQL Database</h4>
<p>Cloud version of SQL Server for structured data.</p>
<div class="example"><strong>Example:</strong> Online store keeping track of products and orders.</div>

<img src="<img width="975" height="530" alt="image" src="https://github.com/user-attachments/assets/ebc49cb2-d153-4881-8850-0907dfb4c4ed" />
" alt="Azure Pricing Calculator">

<h3>Step 2: Sign in to Azure</h3>
<p>Sign in with your triOS student ID at <a href="https://portal.azure.com" target="_blank">Azure Portal</a></p>
<img width="975" height="524" alt="image" src="https://github.com/user-attachments/assets/ba613e33-84d9-4937-a2a6-3ab278df648e" />
" alt="Azure Sign-in">

<h3>Step 3: Create Resource Groups and Virtual Machines</h3>

<h4>Canada Region VMs</h4>
<ul>
    <li>Subscription: Azure for Students</li>
    <li>Resource group: Palv913814-Canada-Resource-Group</li>
    <li>VM Names: Palv913814-ca-server1, Palv913814-ca-server2</li>
    <li>Region: Canada</li>
    <li>OS: Ubuntu Server</li>
    <li>Ports: SSH (22)</li>
    <li>Disk: Standard SSD</li>
    <li>Networking/Management/Monitoring: Default</li>
</ul>
<img width="975" height="531" alt="image" src="https://github.com/user-attachments/assets/08711d96-bb59-4f3d-8b5b-b24d38afbb3e" />

" alt="Canada VMs">

<h4>U.S. Region VMs</h4>
<ul>
    <li>Subscription: Azure for Students</li>
    <li>Resource group: Palv913814-US-Resource-Group</li>
    <li>VM Names: Palv913814-us-server1, Palv913814-us-server2</li>
    <li>Region: U.S.</li>
    <li>OS: Ubuntu Server</li>
    <li>Ports: SSH (22)</li>
    <li>Disk: Standard SSD</li>
    <li>Networking/Management/Monitoring: Default</li>
</ul>
<img width="975" height="526" alt="image" src="https://github.com/user-attachments/assets/0dc4c45a-fec2-44fa-abec-b93302f63797" />

" alt="US VMs">

<h3>Step 4: Configure the Servers</h3>

<h4>Canada Servers</h4>
<ul>
    <li>Note Public IP addresses</li>
    <li>Open firewall for HTTP port 80</li>
  <img width="975" height="526" alt="image" src="https://github.com/user-attachments/assets/abd3cb02-f883-4ab5-8df5-5ae17c62eb8d" />
  " alt="Firewall http 80">
    <li>Connect using SSH (PuTTY)</li>
    <li>Install Apache</li>
   <img width="975" height="528" alt="image" src="https://github.com/user-attachments/assets/783389b8-48d0-4680-994b-22d94ac6985c" />

" alt="Install Apache">
    <li>Create a webpage with your name and student ID (text red)</li>
    <img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/0c6547c5-8498-4561-95a2-7151f818f2a5" />
    <img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/09f200b4-bc9c-4e54-9cd9-452e0e4641f8" />
     <li>Refresh the webpage in your web browser and provide the result.</li>
     <img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/1b19386c-91b5-467f-a522-9eaa37dbccf9" />
     <li>Open firewall for HTTPS port 443.</li>
     <img width="975" height="529" alt="image" src="https://github.com/user-attachments/assets/193298d1-c498-4ebe-b79c-de6d0d16b066" />
    <img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/96d7829f-b93c-40ac-80e0-3a12a380ceef" />


</ul>

<h4>U.S. Servers</h4>
<ul>
    <li>Note Public IP addresses</li>
  <img width="975" height="531" alt="image" src="https://github.com/user-attachments/assets/86674600-ad7a-4dcb-9559-41c98a9fd831" />

    <li>Open firewall for HTTP port 80</li>
  <img width="975" height="527" alt="image" src="https://github.com/user-attachments/assets/f465e088-c171-45f8-a63e-228d3d65981b" />

    <li>Connect using SSH (PuTTY)</li>
   <img width="975" height="528" alt="image" src="https://github.com/user-attachments/assets/736f0832-073f-4a1c-b07e-0c339ef69a66" />

    <li>Install Apache</li>
  <img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/c46aaad6-db45-4e3d-8d03-cd03af63c067" />

    <li>Create a webpage with your name and student ID (text green)</li>
  <img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/4f10f73d-a81f-4cea-9ebb-93b8eee89e8f" />
    <li>Refresh the webpage in your web browser and provide the result.</li>
    <img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/314bd99d-b8fe-4fb3-8cda-03eccbd3d0a6" />

    <li>Open firewall for HTTPS port 443</li>
  <img width="975" height="530" alt="image" src="https://github.com/user-attachments/assets/1d231050-3196-4e3c-90af-726b51f47a48" />

</ul>

<h2>Task 2: Create DevTest Labs and Add VM</h2>
<p>Create a solution for testing applications using Windows and Linux VMs with scheduled start/shutdown.</p>

<h3>Step 1: Create DevTest Lab</h3>
<ul>
    <li>Subscription: Azure for Students</li>
    <li>Resource group: Palv913814-devtest-resource-group</li>
    <li>Lab name: Palv913814-lab</li>
    <li>Auto-shutdown: Off</li>
</ul>
<img width="975" height="529" alt="image" src="https://github.com/user-attachments/assets/c9bc652a-3d8d-4c3a-8f58-30877b342fc7" />
<img width="975" height="526" alt="image" src="https://github.com/user-attachments/assets/16018b38-74c0-4377-ae93-0b81fb895aba" />



<h3>Step 2: Add Azure VM to Lab</h3>
<ul>
    <li>Base VM: Windows Server 2022 Datacenter</li>
    <li>VM Name: Palv913814-VM</li>
</ul>
<img width="975" height="527" alt="image" src="https://github.com/user-attachments/assets/4ac89657-642a-429e-8276-6307366c91a6" />


<h3>Step 3: Connect to VM</h3>
<p>Login using RDP or portal access to verify VM availability.</p>
<img width="975" height="527" alt="image" src="https://github.com/user-attachments/assets/7906567b-d4b3-4501-8fbb-ebe8e575a2dc" />


