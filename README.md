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

1. **Create Resource Groups**
   - Canada: `Palv913814-Canada-Resource-Group`
   - U.S.: `Palv913814-US-Resource-Group`

2. **Create Virtual Machines**
   - VM Names: `Palv913814-ca-server1`, `Palv913814-ca-server2`
   - VM Names: `Palv913814-us-server1`, `Palv913814-us-server2`
   - Ubuntu Server image, SSH enabled, default size
   - Public IP addresses assigned

3. **Connect via SSH**
   - Use PuTTY to connect to each VM using public IP
   - Username: `xx-user`, Password: your password

4. **Install Apache Web Server**
   ```bash
   sudo apt update
   sudo apt install apache2 -y
   sudo systemctl start apache2
   sudo systemctl enable apache2
