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
<img src="<img width="975" height="524" alt="image" src="https://github.com/user-attachments/assets/2bf6ef1c-3b97-4ee8-aaf3-225623d4b8ec" />
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
<img src="<img width="975" height="531" alt="image" src="https://github.com/user-attachments/assets/edd2d685-48d9-46ef-a43f-7de7394d85a9" />
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
<img src="<img width="975" height="526" alt="image" src="https://github.com/user-attachments/assets/cad3bbbd-6d54-4f9e-bad8-4cf63fff0c05" />
" alt="US VMs">

<h3>Step 4: Configure the Servers</h3>

<h4>Canada Servers</h4>
<ul>
    <li>Note Public IP addresses</li>
    <li>Open firewall for HTTP port 80</li>
    <li>Connect using SSH (PuTTY)</li>
    <li>Install Apache</li>
   <img src="<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/e78d6c08-dcbc-4f83-ac6a-aee0736f2bff" />
" alt="Install Apache">
    <li>Create a webpage with your name and student ID (text red)</li>
    <li>Open firewall for HTTPS port 443</li>
</ul>
<img src="<img width="975" height="526" alt="image" src="https://github.com/user-attachments/assets/f691e1e7-5619-44e3-905f-b10e46732bc6" />
" alt="Canada Server Configuration">
<img src="<img width="975" height="528" alt="image" src="https://github.com/user-attachments/assets/cab5d8c3-904f-479f-83a5-52032fb4efef" />
" alt="Install putty and connect">
<h4>U.S. Servers</h4>
<ul>
    <li>Note Public IP addresses</li>
    <li>Open firewall for HTTP port 80</li>
    <li>Connect using SSH (PuTTY)</li>
    <li>Install Apache</li>
    <li>Create a webpage with your name and student ID (text green)</li>
    <li>Open firewall for HTTPS port 443</li>
</ul>
<img src="images/us-server-config.png" alt="US Server Configuration">

<h2>Task 2: Create DevTest Labs and Add VM</h2>
<p>Create a solution for testing applications using Windows and Linux VMs with scheduled start/shutdown.</p>

<h3>Step 1: Create DevTest Lab</h3>
<ul>
    <li>Subscription: Azure for Students</li>
    <li>Resource group: Palv913814-devtest-resource-group</li>
    <li>Lab name: Palv913814-lab</li>
    <li>Auto-shutdown: Off</li>
</ul>
<img src="images/devtest-lab.png" alt="DevTest Lab">

<h3>Step 2: Add Azure VM to Lab</h3>
<ul>
    <li>Base VM: Windows Server 2022 Datacenter</li>
    <li>VM Name: Palv913814-VM</li>
</ul>
<img src="images/devtest-vm.png" alt="VM in DevTest Lab">

<h3>Step 3: Connect to VM</h3>
<p>Login using RDP or portal access to verify VM availability.</p>
<img src="images/connect-vm.png" alt="Connect to VM">

