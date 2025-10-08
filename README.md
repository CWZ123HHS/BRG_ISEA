Reflective Learning Journal Template – BRG28-ISEA 

Student Name: Chai Wei Zhe 

Student ID: CT0388103, 35900251 

GitHub Repository Link: https://github.com/CWZ123HHS/BRG_ISEA/blob/main/README.md 

Video Walkthrough Link:  


===========================================================================================

1. Introduction 


This reflection journal is about my learning experience in the course "Introduction to Server Environments and Architectures" (ISEA). 

Throughout the 4 lessons of this course, I was introduced to the foundational concepts in relation to the server infrastructure, deployment models, and the role of servers in supporting web and network-based applications. 

After going through the 4 days of lessons and lab activities, I have gained practical insights and deeper understanding of how server environments operate in real-world scenarios. 

This reflection journal will highlight the lab activities that I have done, challenges faced, and knowledge learnt. 

===========================================================================================


2. Linux Environment Setup and GitHub Integration

Lab 1a-1 Virtualisation and Linux Setup:  

First, I have installed VMware Workstation Pro. Next, I download the disc image provided, `ubuntu-24.04.3-desktop-amd64.iso`. 
Use the Ubuntu image for setup, then set name, the rest remains default, click the finish button, the VM will start to set up. 

<img width="372" height="252" alt="1a VMware WS PRO installed" src="https://github.com/user-attachments/assets/f27cc1ef-0d5a-48fd-993a-214c33ce32b0" />

<img width="1158" height="384" alt="1a ubuntu image downloaded" src="https://github.com/user-attachments/assets/b2653922-a539-43a7-988f-9b54a3772de5" />

<img width="834" height="266" alt="choose image" src="https://github.com/user-attachments/assets/6cbdbe8f-2b91-4415-9d12-16a07e732a76" />

<img width="876" height="748" alt="1a setup" src="https://github.com/user-attachments/assets/748173da-2180-410b-8e00-1e9b29c62fdd" />


Once VM is set up, complete ubuntu installation set up process, installation will then proceed and prompted to reboot the system. Then login as the user. 

<img width="952" height="668" alt="1a ubuntu install" src="https://github.com/user-attachments/assets/78d9e22d-8901-4db6-bd9f-cfe64871b55a" />


Input command `sudo apt update` to update the list of available packages. 
Then I continue to install virtual box guest, `sudo apt install virtualbox-guest-utils virtualbox-guest-x11` to allow better performance when using VM. 


<img width="886" height="466" alt="1a sudo app update" src="https://github.com/user-attachments/assets/c6fa7ce6-a1ce-461d-a978-b7fc4af3446c" />

<img width="1726" height="936" alt="1a install virtual box guest" src="https://github.com/user-attachments/assets/96986138-55f8-4ae9-a936-08bf6952efbe" />


Install SSH with`sudo apt install openssh-server –y`, followed by `sudo systemctl start ssh`,`sudo systemctl status ssh` to enable SSH and ensure it is running. 

<img width="948" height="372" alt="1a install openssh" src="https://github.com/user-attachments/assets/086b3fbd-c4e8-4188-bd17-aa4986b11318" />

<img width="1248" height="784" alt="1a ssh enable running" src="https://github.com/user-attachments/assets/57a868c9-0668-448d-b464-8231654a77d2" />



When setting up the Linux environment, we were told to use virtualisation software like VirtualBox or VMware Workstation Pro to set up the Ubuntu image. However, the VM could not run properly with VirtualBox. After completing the default setup, I am able to log in to the installation page. Once the settings are configured and installation starts, I then encounter a problem. The installation of Ubuntu starts to lag, then the progress status stops and stays there. The first half of the lesson was just trying to resolve this issue. Then before lunch, I changed to using VMware Workstation Pro instead. The whole process was smooth, Ubuntu managed to install, and I can continue with the lab activities. 

I have learnt that Virtualisation tools is a type of software that simulates a virtualised environment to run an operating system on a machine-like servers or computers. It can allow things like running Ubuntu Linux in the Windows environment. The environment configured is based on the performance of the physical system, meaning that the maximum output of the environment will not exceed the physical system as they are sharing the same storage. 

If the disk size that I am using has a maximum storage of 600GB, the maximum available size for the current VM will not exceed 600GB unless I upgrade the disk size to a larger one, like installing a larger solid-state drive (SSD). 

There are a few types of virtualisation tools, such as VMware Workstation and VirtualBox: 

VMware Workstation provides more features as compared to VirtualBox and higher performance.
VirtualBox, free and open source, supports Windows, Linux, macOS, Solaris.

After completing this lab, I would say that although I have gotten some hands-on experience in using Ubuntu, my level of understanding and skills are still not up to the standard of where I can say I am confident to using it. I will require more practice and studying in this field to be more familiarised with it. 


GitHub Usage

GitHub is a cloud-based platform that enables the developers to store, manage, collaborate on code and other projects. In addition, it can also be used as a place to store notes. In GitHub, I have created a public repository that allows anyone to access it.  
 
===========================================================================================


3. Linux Services, Permissions, and Bash Scripting 

Service Configuration and User Permissions 

Services installed (e.g., NGINX, SSH). 

Permission controls (e.g., chmod, chown, usermod). 

Lessons learned on least privilege and access control. 

Scripting and Automation 

Purpose of your script (e.g., log backup). 

Cron job setup and testing process. 

Reflection on debugging and improvements. 


===========================================================================================

**4. Cloud Infrastructure and TCO Analysis**

*Cloud Deployment*

 * Which platform you used (AWS/Azure/DO). 
 * Steps taken to configure your cloud VM securely. 
 * Reflection on cloud infrastructure provisioning. 

*Cost Analysis*

 * Summary of TCO comparison across providers. 
 * Criteria considered (cost, flexibility, scalability). 

Your platform recommendation and why. 

===========================================================================================
	
**5. DNS Setup and SSL Configuration**

DNS Management 

Domain used and DNS record configuration. 

Tools used to verify DNS propagation. 

I have used the website https://www.whatsmydns.net to verify DNS propagation.

SSL Certificate with Let’s Encrypt 

Certbot usage and challenges. 

During the first time I have tried to run the certbot command, the process failed, showing "Hint: The Certificate Authority failed to verify the temporary Apache configuration changes made by Certbot. Ensure that the listed domains point to this Apache server and that it is accessible from the internet."
Then with the help of the lecturer, we manage to find out that it is A record that are named using "cweizhe22334455.online" have caused the problem.
Therefore, I deleted it and test the certbot again. This time it manage to work.
Next, I used the this link https://www.whatsmydns.net to check on the dns propagation, most of the cities have successfully recorded but some cities like Mexico City, Diemen and Antalya have failed to record. 

HTTPS redirection and security headers. 
Reflection on the importance of encrypted traffic. 

===========================================================================================

 **$${\color{blue}6. \space Automation \space and \space Cron \space Jobs}$$**

 * Describe cron jobs configured. 
 * Script improvements and error handling. 
 * Importance of automation in real-world environments. 

A cron job is a scheduled task that can be used to run a command or script at a specific time, it can be scheduled to run at a selected time or selected day of the week. (Cron - Wikipedia, n.d.) 

Automation helps to reduce human intervention to complete repetitive jobs, it also allows resources to be put to use in other areas that require more resources. Automation is important as it can help to handle repetitive tasks and not require human intervention too frequently.   

===========================================================================================

**$${\color{blue}7. \space Consulting \space Simulation \space and \space Additional \space Server \space Service}$$**

*Peer Consultation Reflection*
 * Overview of your proposed solution (stack, budget, security). 
 * Feedback received and how you incorporated it. 

*Optional Lab (Your Chosen Service)*
 * Service deployed (e.g., MariaDB, vsftpd, Docker). 
 * Configuration steps and security considerations. 
 * Reflection on learning a new service independently. 

For the additional server service, I have decided to do the research on the `htop` service. `htop` allows users to see all the system processes and determine the cause of the load by each process, like what Task Manager can do for Windows. It can be used to show both processes and their threads by default, and kill processes, which means that it can terminate a program or a task that is running in Linux. (How to Manage Linux Processes With htop, n.d.) 

 

`htop` can be installed on Ubuntu. First, use `sudo apt update`, to update the system, and `sudo apt upgrade`, to install the newest package version. 

 <img width="950" height="524" alt="ensure apt updated" src="https://github.com/user-attachments/assets/bbdaf30e-17ec-4530-aeec-31704b8ad8bc" />

 

Install `htop` using `sudo apt install htop`: 

<img width="896" height="542" alt="htop install" src="https://github.com/user-attachments/assets/5f20388d-d33f-4267-98ed-d0fe431cda48" />

 

Input `htop` in the terminal to use it: 

<img width="1286" height="774" alt="htop output" src="https://github.com/user-attachments/assets/0101678b-83b7-4eae-bf1c-28eec9bfe57f" />


 
===========================================================================================

 

**8. Problems Encountered and Solutions**


(Create a table or list format.) | Problem | How You Solved It | |——–|——————-| | Example: SSL failure | Opened firewall and EC2 SG ports | 

| S.No | Problem | Solution |
|---|---|---|
| 1 | Unable to start up VM with VirtualBox. | Switch to VMware Workstation. |
| 2 | Failed to connect public address to domain. | Remove other A records that were added with the Domain name. |

 

===========================================================================================


**9. Industry Relevance**

* Which career roles this lab series relates to (SysAdmin, DevOps, etc.). 

* How this experience helped build confidence in real-world skills. 

* Mention any frameworks referenced (NIST, OWASP, SANS). 

 

These lab series are related to career roles like System Administrator, DevOps Engineer, Linux Engineer as these types of career roles that require a strong foundation on Linux operating system.  

This experience helps me to have a better understanding of how Linux skills is important and demanding as a real-world skill as many careers in the IT field are related to it. 

===========================================================================================


**10. Final Reflection**

	* Summarize your overall learning experience
	* What skills you improved. 
	* How you would approach future server projects differently. 



Overall, the lessons of this course are scheduled fast, 2 weekends in a row and there are only 4 days of lessons. It will be tough to understand that much knowledge and going through the lab activities in this period of time. I would need more time to learn and train on using the Linux commands on Ubuntu to be more familiar with it. 


During these 4 lessons, I have learnt how to use the Linux commands, permission, scripting, understand how to implement TCO to decide on the items needed to be bought, understand the how to use Amazon EC2. 


In future if I were to approach server projects, I will need to be careful on each step to configure. Mistakes like typo error can cause the entire configuration to fail more easily. It will be hard to trace back to see what the problem is, and more time and resources will be wasted on reconfiguring. I also have understood what the server will be used for to ensure the proper packages and setup to be configured. Overall, interacting with servers needs to be careful in each portion and is best to take note of what was configured. 


===========================================================================================


**11. AI Tools Used (if any)**

* List any AI tools (ChatGPT, Copilot) used for grammar, scripting help, etc. 

* Be honest and specific. 

===========================================================================================

**12. Appendix (Add as needed)**

	* Bash scripts 
 * Cron entries 
 * Screenshots 
 * NGINX or service config files 
 * GitHub repo file structure 

 




