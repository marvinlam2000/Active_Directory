# Active Directory Project

## Objective
Setting up an Active Directory (home lab) that includes Splunk, Kali Linux & Atomic Red Team. Explore how a domain envirnment works, learn how to ingest events to a SIEM, and generate telemetry related to attack seen in the wild to help understand how to detect them in the future.

### Skills Learned

- Advanced understanding of SIEM concepts and practical application.
- Proficiency in analyzing and interpreting network logs.
- Ability to generate and recognize attack signatures and patterns.
- Enhanced knowledge of network protocols and security vulnerabilities.
- Development of critical thinking and problem-solving skills in cybersecurity.

### Tools Used

- Security Information and Event Management (SIEM) system for log ingestion and analysis. (Splunk)
- Telemetry generation tools to create realistic network traffic and attack scenarios. (Sysmon)
- VirtualBox
- Kali Linux
- Atomic Red Team

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

Step 9. On the Active Directory Server, create users under custom organizational units.
![step 9](https://github.com/user-attachments/assets/8b1db5b5-7a2d-4184-98d3-3f3703a8e897)

Step 10. 

