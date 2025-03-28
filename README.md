# Active Directory Project

## Objective
Setting up an Active Directory (home lab) that includes Splunk, Kali Linux, and an Active Directory. Explore how a domain environment works, learn how to ingest events to a SIEM, and generate telemetry/brute force attack to help understand how to detect them in the future and what to look at in the SIEM.

### Skills Learned
- Creating, managing and assigning users to an active directory.
- Simulate a Brute force attack to understand logs ingested by a SIEM tool.
- Generate and view telemetry via Splunk.
- Understanding basic network configurations concepts.

### Tools Used

<img src="https://img.shields.io/badge/-Splunk-000000?&style=for-the-badge&logo=Splunk&logoColor=white" />
<img src="https://img.shields.io/badge/-Sysmon-8A2BE2?&style=for-the-badge&logo=windows&logoColor=white" />
<img src="https://img.shields.io/badge/-VirtualBox-183A61?&style=for-the-badge&logo=virtualbox&logoColor=white" />
<img src="https://img.shields.io/badge/-Linux-FCC624?&style=for-the-badge&logo=linux&logoColor=black" />
<img src="https://img.shields.io/badge/-Active%20Directory-003366?&style=for-the-badge&logo=microsoft&logoColor=white" />

## Steps
Step 1. Create a diagram of the whole process using Draw.io.
![Activedirectory drawio](https://github.com/user-attachments/assets/43aa888f-d19e-45e4-809b-e6128d7bf504)

Step 2. Download VirtualBox as this will be the place where Virtual machines will be created. Download windows 10 iso file, kali linux, Windows server, and Ubuntu all on VirtualBox.
![step 2](https://github.com/user-attachments/assets/847aa85f-1ea5-4da1-864a-54594b9750c0)

Step 3. Create a NAT network on virtualbox, assign the IPv4 address, and then for each machine assign it to the NAT network just created.
![step3](https://github.com/user-attachments/assets/d2f2baac-24cf-40b8-8852-df7001b19cbb)

Step 4. Set up configurations on Ubuntu and add Splunk in the ubuntu machine.
![step 4](https://github.com/user-attachments/assets/9626319b-ee8c-4e71-8f6a-dd84bb6fdbf6)
Step 5. Download Sysmon and Splunk Universal Forwarder downloads on the targeted machine.
![step 5](https://github.com/user-attachments/assets/b20e0b91-5e64-4702-be69-683edf6078da)

Step 6. On the targeted machine, instruct the Splunk forwarder to push events related to Application, Security, Systems, and Sysmon over to Splunk server. Make sure to restart Splunk services to apply the configuration.
![step 6](https://github.com/user-attachments/assets/11571d76-8f1d-4dd2-bb6b-9fec4a700e58)

Step 7. On the targeted machine, go to Splunk, and create an index called endpoint. I created a config file that allows Application, System, Security, and Sysmon events to go to the index called endpoint.
![step 7](https://github.com/user-attachments/assets/96d71a66-9938-456d-b755-1a5473441494)

Step 8. Repeat steps 6 and 7 on the Microsoft Server Virtual Machine. You should be able to see on Splunk that there are 2 host.
![step 8](https://github.com/user-attachments/assets/63288b6d-83a3-4e56-b781-6d2a98423cbd)

Step 9. On the Active Directory Server, create users under custom organizational units and then on the targeted machine you can login to the users created from the domain.
![step 9](https://github.com/user-attachments/assets/8b1db5b5-7a2d-4184-98d3-3f3703a8e897)

Step 10. On the kali linux machine, configure the ip address, confirm on the terminal by pinging google and as well as the splunk server, then create a new directory in the terminal.
![step10](https://github.com/user-attachments/assets/64692a3a-df57-40cd-a261-23d924f2222b)

Step 11. On the targeted virtual machine, enable RDP and add the users created from the directory.
![step11](https://github.com/user-attachments/assets/708c71b0-d59b-40b1-b4ab-9fea2fb0de86)

Step 12. On the kali linux machine, I simulated a brute force attack and the victim machine was one of the users I created from the active directory.
![step 12](https://github.com/user-attachments/assets/47af8b07-b953-4edb-a7d1-09cd9323a430)

Step 13. Go through Splunk and look through the ingested logs.
![step13](https://github.com/user-attachments/assets/76983f88-ed80-432c-9848-849fddb31067)

