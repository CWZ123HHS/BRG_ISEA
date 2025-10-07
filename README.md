# BRG_ISEA
This repository is for the use of ISEA - Introduction to Server Environments and Architectures.


Reflective Learning Journal Template – BRG28-ISEA 

Student Name: Chai Wei Zhe 

Student ID: CT0388103, 35900251 

GitHub Repository Link: https://github.com/CWZ123HHS/BRG_ISEA/blob/main/README.md 

Video Walkthrough Link: https://alfalearn.sharepoint.com/sites/LEARN/Shared%20Documents/Forms/AllItems.aspx?id=%2Fsites%2FLEARN%2FShared%20Documents%2Fe%2DKAPLAN%2FMU%2DISEABRG%2D27%2DIntroServer%2Fstudent%2FVideoUpload&p=true&ga=1 

 
 

1. Introduction 

This reflection journal is about my learning experience in the course "Introduction to Server Environments and Architectures". 

Throughout the 4 lessons of this course, I was introduced to the foundational concepts in relation to the server infrastructure, deployment models, and the role of servers in supporting web and network-based applications. 

 

 

2. Linux Environment Setup and GitHub Integration 

 

During the setup of the Linux environment, we were told to either use virtualisation software like VirtualBox or VMware Workstation Pro to set up the Ubuntu image. However, the VM could not run properly when I was using the VirtualBox. After completing the default setup, I am able to log in to the installation page. Once the settings are configured and installation starts, I then encounter a problem. The installation of Ubuntu starts to lag, then the progress status stops and stays there. The first half of the lesson was just trying to resolve this issue. Then before lunch, I changed to using VMware Workstation Pro instead. The whole process was smooth, Ubuntu managed to be installed and I can continue with the lab activities. 

Virtualisation tools is a type of software that simulates a virtualised environment to run an operating system on a machine-like servers or computers. It can allow things like running Ubuntu Linux in the Windows environment. The environment configured is based on the performance of the physical system, meaning that the maximum output of the environment will not exceed the physical system as they are sharing the same storage. 

For example, the disk size that I am using has a maximum storage of 520GB, there are some other system data and program data that use up 30GB. The maximum available size for the current virtual machine will not exceed 490GB unless I upgrade the disk size to a larger one, like installing a larger solid-state drive (SSD). 

 

What did you learn about virtualisation tools and their differences?  

There are a few types of virtualisation tools: 

VMware Workstation, free for all personal, commercial, and educational users, effective from November 2024 

VirtualBox, free and open source,  

Microsoft Hyper-V: supports Hypervisor 1 

 

 

How confident do you feel using Ubuntu after completing this lab 

Overall, I would say that I have gotten some hands-on experience in using Ubuntu, but not to the standard of where I can say I am an expert in using it. I will require more practice and studying in this field. 

 

 

 

Lab 1a-1 Virtualisation and Linux Setup:  

First, I have installed VMware Workstation Pro. 

   

Next, I downloaded this disc image: ubuntu-24.04.3-desktop-amd64.iso 

   

For the setup, use the image downloaded for ubuntu installation, then follow by the name of the VM, size of 20GB, memory is set as default of 4096MB, network default setting remains as NAT. Then click the finish button, the VM will start to set up. 

 

 

   

Once the VM is set up, we go through the installation set up process, installation will then proceed and prompted to reboot the system. Then login as the user. 

 

 

Start with [sudo apt update]; 

 

Then i installed virtual box guest as this allows automatic screen resizing for VM: 

 

Install SSH, enable it and ensure it is running: 

 

 

 

 

Lab 1a-2 Ubuntu Desktop and Command Line Familiarisation: 

Part 1: Ubuntu Desktop GUI Familiarisation  

Check Internet using Firefox.  

 

Open LibreOffice and type a document.  

Install LibreOffice from the terminal. 

Open from the terminal and edit. 

 

 

Navigate directories using File Manager.  

 

Install a program via Ubuntu Software Centre.  

Visualise file changes by placing terminal and file browser side-by-side. 

Part 2: CLI Basics and File Operations  

Use ps -e, top, and 1 to monitor processes.  

ps -e 

Top:  

Top and 1:  

Use ls, ls -la, ls -alt, ls -lah to explore files.  

ls:  

ls –la:  

ls –alt:  

ls –lah:  

Create/edit/view files using touch, gedit, nano, cat, less.  

touch:  

gedit:  

nano file 1:  

nano file 2:  

cat file1 and file 2:  

less file1:  

 

Copy and move files with cp, mv; delete with rm.  

cp file1:  

mv copyfile1 to documents:  

 

rm, delete file2:  

View system info using uname -a, lsb_release -a, hostnamectl. 

uname –a and lsb_release –a:   

hostnamectl:  

Part 3: Super User and Permissions  

Use whoami, sudo whoami to demonstrate privilege escalation.  

whoami shows cweizhe, sudo whoami shows root: 

  

Attempt adduser as sudoregular user, then with sudo.  

 

Discuss role of root user and best practices for privilege use. 

The role of root user is like an administrator that have the highest level of privileges and control within the Linux operating system. 

It can execute any command, modify any files, changing the permissions or ownership of files and directories, modify user’s permission on the file.  

Part 4: Network Configuration and DNS  

Use ip a to identify private IP.  

 

Ping local devices or 8.8.8.8 and discuss DNS.  

8.8.8.8 is the public DNS server of Google. 

We are able to ping using both 8.8.8.8 and google.com on the terminal as the ip address is linked to the google.com address. 

 

Edit /etc/hosts to create custom aliases; test with ping.  

First I will use nano to open /etc/hosts and add the ip address and name it ‘dnsgoogle’ inside. 

Then i will ping ‘dnsgoogle’. 

 

Use nslookup and install/use whois to investigate domains.  

nslookup:   

Installation of whois program and check on google domain. 

 

 

Compare public/private IP via https://whatismyipaddress.com/. 

Part 5: System and Hardware Info  

Use lsusb, lspci, less /proc/cpuinfo to inspect hardware.  

lsusb and lspci:  

less /proc/cpuinfo:  

Compare CLI outputs with 'About This Computer' in settings.  

 

Redirect output using >, e.g., lsusb > output_of_lsusb, then view with less and cat. 

 

less:  

cat:  

Part 6: Software Installation Methods  

Install a browser (Chrome/Opera) from a .deb file.  

Download the deb file from the chrome. Then install using terminal. 

 

 

 

Install apps via Ubuntu Software Centre.  

 

 

 

 

Use sudo apt update, sudo apt upgrade, sudo apt install vlc.  

 

 

 

Search packages with sudo apt search [keyword].  

sudo apt search chrome: 

 

Explore /etc/apt/sources.list to discuss trusted repositories. 

 

Part 7: Compiling from Source (Optional)  

Install build tools: sudo apt install build-essential.  

 

Write a basic hello_world.c and compile with gcc. 

Run the executable with ./hello_world_executable.  

 

Adjust permissions with chmod 777 if needed.  

Compare source and compiled file using less. 

I am able to see the source file directly using less command. 

 

But when it comes to the compile file, it will show a prompt to ask if i want see it and this is the output. 
<img width="766" height="44" alt="less hellow compile ask" src="https://github.com/user-attachments/assets/f018bcec-9f00-4595-99b8-15218e477619" />

<img width="1832" height="780" alt="less hellow compile output" src="https://github.com/user-attachments/assets/0be1420a-b266-4bd0-815c-c18647f58643" />

<img width="802" height="152" alt="less hellow compile" src="https://github.com/user-attachments/assets/b657e72b-5477-4791-8c0e-80110b225f33" />
 

 

GitHub Usage 

 

In GitHub, I have created a public repository that allows anyone to access it. 

 

3. Linux Services, Permissions, and Bash Scripting 

Service Configuration and User Permissions 

Services installed (e.g., NGINX, SSH). 

Permission controls (e.g., chmod, chown, usermod). 

Lessons learned on least privilege and access control. 

Scripting and Automation 

Purpose of your script (e.g., log backup). 

Cron job setup and testing process. 

Reflection on debugging and improvements. 

 

Lab 1b-1: 

For lab activity 1b-1, I have installed Apache2 using this command [sudo apt install apache2], Using the ip address for localhost, [127.0.0.1], I managed to access Apache2. Next, I continue used the command [ip -a] and retrieved 2 set of ip address,  

Lab activity 1b-2: 

 

 

Linux uses 3 main permissions, read, write and execute which implies to the owner, group and other users, 

Windows uses Access Control Lists (ACL) controls which user or group have what type of permission for that file or folder 

 

 

 

4. Cloud Infrastructure and TCO Analysis 

Cloud Deployment 

Which platform you used (AWS/Azure/DO). 

Steps taken to configure your cloud VM securely. 

Reflection on cloud infrastructure provisioning. 

 

For cloud infrastructure, I have decided to use Amazon Web Services (AWS). as it provides free $100 USD credits, $20 USD for each completed for exploring the functions of AWS.  

 

For cloud infrastructure, it does not use a pricing scheme known as pay-as-you-go, which users only need to pay for the use o  

 

One that I have encountered is that when the VM has been left for a while without being used, it will not be able to do any configurations. Thus I need to refresh the entire web page to continue using it. 

 

 

 

Cost Analysis 

Summary of TCO comparison across providers. 

Criteria considered (cost, flexibility, scalability). 

Your platform recommendation and why. 

 

TCO means Total Cost of Ownership, which consist of Acquisition cost like the physical hardware, software,  

Then we have to compare both type of  

We have to consider things like:  

Price of the printer. 

Printing speed within the period of time. 

The cost of paper. 

 

 

 

5. DNS Setup and SSL Configuration 

DNS Management 

Domain used and DNS record configuration. 

Tools used to verify DNS propagation. 

SSL Certificate with Let’s Encrypt 

Certbot usage and challenges. 

HTTPS redirection and security headers. 

Reflection on the importance of encrypted traffic. 

 

I have created a domain name “cweizhe22334455.online” using GoDaddy. I will then set up my A record under the DNS Records using the public IPv4 address that my instance is currently holding. The name will remain as ‘@’. Once the record has been added,  

 

Afterwards, I used the website ‘https://www.whatsmydns.net/’ to check that the DNS record has been recorded in other cities. Once it has been recorded, a tick will be shown. 

 

Each time when the instances are on and off, the public IPv4 address of the instance will change. My original IPv4 address changed from [       ] to  [3.27.217.115]. Therefore the configuration A record on the DNS will need to change to match the current public IPv4 address. 

Certbot is a software tool that helps to generate or renew a trusted TLS certificate from the Let's Encrypt certificate authority to enable HTTPS on the selected domain. Similarly, myMurdoch Learning has a digital certificate issued by the company DigiCert. 

 

 

6. Automation and Cron Jobs 

Describe cron jobs configured. 

Script improvements and error handling. 

Importance of automation in real-world environments. 

 

 

 

 

Automation is important as it can help to handle repetitive tasks and not require human interface too frequently.  

7. Consulting Simulation and Additional Server Service 

Peer Consultation Reflection 

Overview of your proposed solution (stack, budget, security). 

Feedback received and how you incorporated it. 

Optional Lab (Your Chosen Service) 

Service deployed (e.g., MariaDB, vsftpd, Docker). 

Configuration steps and security considerations. 

Reflection on learning a new service independently. 

 

For the additional server service, I have decided to do the research on the htop. It is a useful command-line tool that allows users to determine the cause of load by each process, like what Task Manager can do for Windows. Only root has the permission to see all the system processes, other users can only see their own system process. It can be used to kill processes, which means that it can terminate a program or a task that is running in Linux. 

 

The steps for configuration are simple; it can be installed on Ubuntu like how Apache2 was installed. 

First, we start with the command [sudo apt update], to update the system. Followed by [sudo apt upgrade], to install the newest version from the internet. 

 

 

 

Next, we install htop using the command [sudo apt install htop]: 

 

 

To run htop, we just need to type [htop] and press enter: 

 

 

 

8. Problems Encountered and Solutions 

(Create a table or list format.) | Problem | How You Solved It | |——–|——————-| | Example: SSL failure | Opened firewall and EC2 SG ports | 

Failed to connect public address to domain | Solution 

Failed to connect public address again | Public ipv4 will change when start instances again. 

 

9. Industry Relevance 

Which career roles this lab series relates to (SysAdmin, DevOps, etc.). 

How this experience helped build confidence in real-world skills. 

Mention any frameworks referenced (NIST, OWASP, SANS). 

 

 

10. Final Reflection 

Summarize your overall learning experience. 

What skills you improved. 

How you would approach future server projects differently. 

 

Overall, the lessons of this course are too fast, 2 weekends in a row and there iare only 4 days of lessons. It will be tough to understand that much knowledge in this period of time. I would need more time to learn and train on using the linux commands on Ubuntu.  

 

 

In future if i were to approach server projects, i will need to be careful on each step to configure. Mistakes like typo error can cause the entire configuration to fail more easily. It will be hard to trace back to see what the problem is and more time will be wasted on reconfiguring. 

 

11. AI Tools Used (if any) 

List any AI tools (ChatGPT, Copilot) used for grammar, scripting help, etc. 

Be honest and specific. 

 

12. Appendix (Add as needed) 

Bash scripts 

Cron entries 

Screenshots 

NGINX or service config files 

GitHub repo file structure 

 

 

1a-2 Ubuntu Desktop and Command Line Familiarisation: 

 

Part 1: Ubuntu Desktop GUI Familiarisation  

 

- Check Internet using Firefox.  

- Open LibreOffice and type a document.  

- Navigate directories using File Manager.  

- Install a program via Ubuntu Software Centre.  

- Visualise file changes by placing terminal and file browser side-by-side.  

Part 2: CLI Basics and File Operations  

 

- Use `ps -e`, `top`, and `1` to monitor processes.  

 

- Use `ls`, `ls -la`, `ls -alt`, `ls -lah` to explore files.  

 

- Create/edit/view files using `touch`, `gedit`, `nano`, `cat`, `less`.  

 

- Copy and move files with `cp`, `mv`; delete with `rm`.  

 

- View system info using `uname -a`, `lsb_release -a`, `hostnamectl`.  

 

Part 3: Super User and Permissions  

 

- Use `whoami`, `sudo whoami` to demonstrate privilege escalation.  

 

- Attempt `adduser` as sudoregular user, then with `sudo`.  

 

- Discuss role of root user and best practices for privilege use.  

 

Part 4: Network Configuration and DNS  

 

- Use `ip a` to identify private IP.  

 

- Ping local devices or 8.8.8.8 and discuss DNS.  

 

- Edit `/etc/hosts` to create custom aliases; test with `ping`.  

 

- Use `nslookup` and install/use `whois` to investigate domains.  

 

- Compare public/private IP via https://whatismyipaddress.com/.  

 

Part 5: System and Hardware Info  

 

- Use `lsusb`, `lspci`, `less /proc/cpuinfo` to inspect hardware.  

 

- Compare CLI outputs with 'About This Computer' in settings.  

 

- Redirect output using `>`, e.g., `lsusb > output_of_lsusb`, then view with `less` and `cat`.  

 

Part 6: Software Installation Methods  

 

- Install a browser (Chrome/Opera) from a .deb file.  

 

- Install apps via Ubuntu Software Centre.  

 

- Use `sudo apt update`, `sudo apt upgrade`, `sudo apt install vlc`.  

 

- Search packages with `sudo apt search [keyword]`.  

 

- Explore `/etc/apt/sources.list` to discuss trusted repositories. 

 

 
