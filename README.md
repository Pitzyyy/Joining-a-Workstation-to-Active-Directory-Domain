# Windows Server 2022 — Installation & Initial Setup

## Description

A step-by-step walk-through of configuring network interface settings, verifying DNS resolution, and joining a Windows 10 workstation to an Active Directory domain (homelabactivity.local). This procedure ensures proper communication between client machines and the domain controller within the virtual lab environment.

## Environment Used

- Windows Server 2022
- Windows Server 2022 (Domain Controller / DNS Server)
- VMware Workstation

## Lab walk-through


<p align="center">
Navigate to Network & Internet settings to view connection status and access network configuration options.
  <img src="./assets/images/1.png" alt="Create new user"
       style="width:80%;height:80%;display:block;margin:0 auto;" />
</p>


<p align="center">
Open the Network Connections window to view available network adapters.
  <img src="./assets/images/2.png" alt="Create new user"
       style="width:80%;height:80%;display:block;margin:0 auto;" />
</p>

<p align="center">
Select the Ethernet adapter to configure properties for domain connectivity.
  <img src="./assets/images/3.png" alt="Create new user"
       style="width:80%;height:80%;display:block;margin:0 auto;" />
</p>

<p align="center">
Access the Ethernet properties menu and select Internet Protocol Version 4 (TCP/IPv4).
  <img src="./assets/images/4.png" alt="Create new user"
       style="width:80%;height:80%;display:block;margin:0 auto;" />
</p>

<p align="center">
Execute ipconfig in Command Prompt to verify current IP address configuration and default gateway details.
  <img src="./assets/images/5.png" alt="Create new user"
       style="width:80%;height:80%;display:block;margin:0 auto;" />
</p>

<p align="center">
Configure static IP settings, setting the Preferred DNS server to loopback or local server IP for testing.
  <img src="./assets/images/6.png" alt="Create new user"
       style="width:80%;height:80%;display:block;margin:0 auto;" />
</p>

<p align="center">
Verify network status reflecting private network connection established on Ethernet0.
  <img src="./assets/images/7.png" alt="Create new user"
       style="width:80%;height:80%;display:block;margin:0 auto;" />
</p>

<p align="center">
Update IPv4 DNS settings to point directly to the Active Directory Domain Controller IP address in Client Account
  <img src="./assets/images/8.png" alt="Create new user"
       style="width:80%;height:80%;display:block;margin:0 auto;" />
</p>

<p align="center">
Test connectivity using ping and perform nslookup to verify domain name resolution for homelabactivity.local.
  <img src="./assets/images/9.png" alt="Create new user"
       style="width:80%;height:80%;display:block;margin:0 auto;" />
</p>

<p align="center">
Open System Properties, enter the domain name homelabactivity.local, <br>and rename the computer to Computer-01 to join the domain.
  <img src="./assets/images/10.png" alt="Create new user"
       style="width:80%;height:80%;display:block;margin:0 auto;" />
</p>

<p align="center">
Authenticate with domain administrator credentials to authorize joining the domain.
  <img src="./assets/images/11.png" alt="Create new user"
       style="width:80%;height:80%;display:block;margin:0 auto;" />
</p>

<p align="center">
Confirm successful domain join upon receiving the welcome message for homelabactivity.local.
  <img src="./assets/images/12.png" alt="Create new user"
       style="width:80%;height:80%;display:block;margin:0 auto;" />
</p>

<p align="center">
Verify the newly added client computer object within the Computers container in Active Directory Users and Computers on the Domain Controller.
  <img src="./assets/images/13.png" alt="Create new user"
       style="width:80%;height:80%;display:block;margin:0 auto;" />
</p>






