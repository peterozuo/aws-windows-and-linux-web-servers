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

#### Backend Configuration Proof:
[DELETE THIS LINE AND DRAG/DROP YOUR IIS DASHBOARD SCREENSHOT HERE]
Figure 1: The backend Internet Information Services (IIS) Manager console running inside the Windows Server.

#### Live Public Webpage Proof:
[DELETE THIS LINE AND DRAG/DROP YOUR WINDOWS BROWSER WEBPAGE SCREENSHOT HERE]
Figure 2: The live public-facing website running successfully on the Windows IIS Server.

---

### 2. Ubuntu Linux (Apache) Deployment
*   *Operating System:* Ubuntu Server
*   *Web Server software:* Apache2

#### Linux Terminal Execution Proof:
[DELETE THIS LINE AND DRAG/DROP YOUR LINUX TERMINAL SCREENSHOT HERE]
Figure 3: Command execution inside the EC2 Instance Connect Linux terminal setting up the custom server message.

#### Live Public Webpage Proof:
[DELETE THIS LINE AND DRAG/DROP YOUR UBUNTU BROWSER WEBPAGE SCREENSHOT HERE]
Figure 4: The live public-facing website running successfully on the Ubuntu Apache Server.

---

## Key Engineering Takeaways
*   *Dynamic vs. Static IP Behaviors:* Stopping and restarting an EC2 instance causes AWS to assign a new public IPv4 address. For production environments, an *Elastic IP* (Static IP) is used to keep the web address permanent.
*   *Network Security:* Strict inbound rules were maintained so administrative entry points (SSH/RDP) remained isolated while keeping the web port (HTTP 80) open to the world
