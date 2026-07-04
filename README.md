# AWS Windows and Linux Web Servers Deployment

## Project Overview
This project demonstrates the setup, configuration, and verification of public-facing web servers on both Windows and Linux operating systems within Amazon Web Services (AWS) EC2. 

I deployed a Windows Server instance running Internet Information Services (IIS) and an Ubuntu Linux instance running Apache. Both environments were successfully configured via their respective backend administrative utilities and verified to serve web traffic over the public internet.

---

## Technical Skills Demonstrated
*   *Cloud Infrastructure:* AWS EC2 deployment, Security Group configuration, Public IPv4 addressing.
*   *Windows Server Administration:* Remote Desktop Protocol (RDP), Internet Information Services (IIS) Manager configuration.
*   *Linux System Administration:* Command Line Interface (CLI), Apache2 web server deployment, package management.

---

## Deployment Breakdown

### 1. Windows Server (IIS) Deployment
*   *Operating System:* Windows Server 2022
*   *Web Server software:* Internet Information Services (IIS)

#### 🔹 Backend Configuration Verification:
<img width="959" height="421" alt="window-rd-IIS" src="https://github.com/user-attachments/assets/426c2f84-13ac-42de-a1c9-a1c791a7ba41" />

Figure 1: The backend Internet Information Services (IIS) Manager console running inside the Windows Server.

#### 🔹 Live Public Webpage Verification:
<img width="953" height="437" alt="window-ec2-localhost" src="https://github.com/user-attachments/assets/6a26f639-f8f3-4c4a-a875-66a01d55c426" />

Figure 2: The live public-facing website running successfully on the Windows IIS Server.

---

### 2. Ubuntu Linux (Apache) Deployment
*   *Operating System:* Ubuntu Server
*   *Web Server software:* Apache2

#### 🔹 Linux Terminal Execution Verification:
<img width="959" height="422" alt="ubuntu-launch-web-server" src="https://github.com/user-attachments/assets/2e4e8a30-34d7-420e-93ba-961f5aa14758" />

Figure 3: Command execution inside the EC2 Instance Connect Linux terminal setting up the custom server message.

#### 🔹 Live Public Webpage Verification:
<img width="953" height="471" alt="ubuntu-main-page-server" src="https://github.com/user-attachments/assets/1bfa9463-1fdd-475f-a403-9e4d9c065b36" />

Figure 4: The live public-facing website running successfully on the Ubuntu Apache Server.

---

## Key Engineering Takeaways
*   *Dynamic vs. Static IP Behaviors:* Stopping and restarting an EC2 instance causes AWS to assign a new public IPv4 address. For production environments, an Elastic IP (Static IP) is used to keep the web address permanent.
*   *Network Security:* Strict inbound rules were maintained so administrative entry points (SSH/RDP) remained isolated while keeping the web port (HTTP 80) open to the world.
