
### Student Name: Chai Wei Zhe

### Student ID: CT0388103, 35900251

### GitHub Repository Link: https://github.com/CWZ123HHS/BRG_ISEA/blob/main/README.md

### Video Walkthrough Link: https://alfalearn.sharepoint.com/sites/LEARN/Shared%20Documents/Forms/AllItems.aspx?id=%2Fsites%2FLEARN%2FShared%20Documents%2Fe%2DKAPLAN%2FMU%2DISEABRG%2D27%2DIntroServer%2Fstudent%2FVideoUpload&p=true&ga=1 


===========================================================================================

### 1. Introduction


This reflection journal is about my learning experience in the course "Introduction to Server Environments and Architectures" (ISEA). Throughout the four lessons of this module, I was introduced to the foundational concepts in relation to the server infrastructure, deployment models, and the role of servers in supporting web and network-based applications. After going through the four days of lessons and lab activities, I have gained practical insights and deeper understanding of how server environments operate in real-world scenarios. This reflection journal will highlight the lab activities that I have done, challenges faced, and knowledge learnt. 

===========================================================================================


### 2. Linux Environment Setup and GitHub Integration

**Lab 1a-1 Virtualisation and Linux Setup:**

First, I have installed VMware Workstation Pro. Next, I download the disc image provided, `ubuntu-24.04.3-desktop-amd64.iso`. Use the Ubuntu image for setup, then set name, the rest remains default, click the finish button, the VM will start to set up. 

<img width="372" height="252" alt="1a VMware WS PRO installed" src="https://github.com/user-attachments/assets/f27cc1ef-0d5a-48fd-993a-214c33ce32b0" />

<img width="1158" height="384" alt="1a ubuntu image downloaded" src="https://github.com/user-attachments/assets/b2653922-a539-43a7-988f-9b54a3772de5" />

<img width="834" height="266" alt="choose image" src="https://github.com/user-attachments/assets/6cbdbe8f-2b91-4415-9d12-16a07e732a76" />

<img width="876" height="748" alt="1a setup" src="https://github.com/user-attachments/assets/748173da-2180-410b-8e00-1e9b29c62fdd" />


Once VM is set up, complete ubuntu installation set up process, installation will then proceed and prompted to reboot the system. Then login as the user.  

<img width="952" height="668" alt="1a ubuntu install" src="https://github.com/user-attachments/assets/78d9e22d-8901-4db6-bd9f-cfe64871b55a" />


Input `sudo apt update` to update the list of available packages. Then I continue to install virtual box guest, `sudo apt install virtualbox-guest-utils virtualbox-guest-x11` to allow better performance when using VM. 


<img width="886" height="466" alt="1a sudo app update" src="https://github.com/user-attachments/assets/c6fa7ce6-a1ce-461d-a978-b7fc4af3446c" />

<img width="1726" height="936" alt="1a install virtual box guest" src="https://github.com/user-attachments/assets/96986138-55f8-4ae9-a936-08bf6952efbe" />


Install SSH with`sudo apt install openssh-server –y`, followed by `sudo systemctl start ssh`, `sudo systemctl status ssh` to enable SSH and ensure it is running. 


<img width="948" height="372" alt="1a install openssh" src="https://github.com/user-attachments/assets/086b3fbd-c4e8-4188-bd17-aa4986b11318" />

<img width="1248" height="784" alt="1a ssh enable running" src="https://github.com/user-attachments/assets/57a868c9-0668-448d-b464-8231654a77d2" />


 
**Lab 1a-1 reflection:**

When setting up the Linux environment, we were told to use virtualisation software like VirtualBox or VMware Workstation Pro to set up the Ubuntu image. I encountered problem with VirtualBox. At the installation of Ubuntu, it starts lagging, then stopped. The first half of the lesson was just trying to resolve this issue. Before lunch, I changed to using VMware Workstation Pro instead. The installation was smooth, and I can continue with the lab activities.  

I have learnt that Virtualisation tools is a type of software that simulates a virtualised environment to run an operating system on a machine, like servers or computers. It can allow Linux to run in Windows environment. The environment is configured based on the performance of the physical system, meaning that the maximum output of the environment will not exceed that of the physical system, as they share the same storage.  

If the disk size that I am using has a maximum storage of 600GB, the maximum available size for the current VM will not exceed 600GB unless I upgrade the disk size to a larger one, like installing a larger solid-state drive.  

There are a few types of virtualisation tools, such as VMware Workstation and VirtualBox:  

	* VMware Workstation provides more features and higher performance.  

	* VirtualBox, free and open source, supports Windows, Linux, macOS, Solaris.  

After completing this lab, I have gotten some hands-on experience in using Ubuntu, but my level of understanding and skills are still not up to the standard of where I can say I am confident to using it. I need more practice and studying in this field to be more familiarised with it. 



**Lab 1a-2 Ubuntu Desktop and Command Line Familiarisation:**

**Part 1: Ubuntu Desktop GUI Familiarisation**

For this activity, I start by checking connectivity with Firefox. Used `sudo snap install libreoffice` to install LibreOffice from the terminal. LibreOffice can open with`libreoffice –writer` from the terminal, LibreOffice will be opened, and I can edit and save like using a notepad. `nautilus`, can be used to open the files.  

<img width="1480" height="773" alt="1b firefox online" src="https://github.com/user-attachments/assets/61a29024-78b2-41b6-92f4-b358c063d91d" />

<img width="844" height="198" alt="1b install libreoffice" src="https://github.com/user-attachments/assets/3871ab66-52b4-4c87-9423-c982c40fa7a7" />

<img width="1284" height="585" alt="1b libreoffice save file" src="https://github.com/user-attachments/assets/f4688149-fbb0-4afc-9a5d-ec093404fae4" />

<img width="1092" height="644" alt="1b file manager" src="https://github.com/user-attachments/assets/833d1281-59ed-4185-8571-dbf0bf226302" />



**Part 2: CLI Basics and File Operations**

`ps –e`is used to display the information of all the active processes that are running on this system, sorted by PID. 
<img width="630" height="294" alt="1b ps e cmd 2" src="https://github.com/user-attachments/assets/21c3be6b-d1ef-4ed3-a7cf-1ca4640e44b9" />


`top` displays system summary information and the list of processes or threads that are currently managed by the Linux kernel. 
<img width="848" height="384" alt="1b top cmd" src="https://github.com/user-attachments/assets/f5d9d6b7-6740-4359-b05f-4ddf539d69b4" />


When `top`is running and I press 1, the display will change. It will now then display the usage for each individual CPU core. 
<img width="860" height="504" alt="1b top and 1 cmd" src="https://github.com/user-attachments/assets/aa7ced86-aed0-4150-ab55-daa8e15810bc" />


`ls` is used to display the files and subdirectories present in the current working directory. 
<img width="808" height="198" alt="1b ls cmd" src="https://github.com/user-attachments/assets/69eae084-a87f-4965-a6c6-d747a86afa92" />


`ls –la` will display all the files and directories in the current directory in a long format. 
<img width="832" height="722" alt="1b ls la cmd" src="https://github.com/user-attachments/assets/cec92f81-d5fe-4389-861e-7cdc836a0551" />



`ls –alt` will display all the files and directories in the current directory in a long format and sorted by the newest first. 
<img width="678" height="288" alt="image" src="https://github.com/user-attachments/assets/fc78ba83-84bd-45c0-80df-9390eef91299" />


`ls –lah` is like `ls –la`, what it does differently is that it does not show the exact size of the file but convert to human readable format, for example, 4096 has been shortened to 4.0k.  

<img width="750" height="566" alt="1b ls lah cmd" src="https://github.com/user-attachments/assets/a7c28e30-bab1-4b1e-8790-ed33d62d631f" />


`touch` is used to create an empty file while `gedit` is used to open the file with gedit text editor, allows editing and changes can be saved. In the screenshot below, I created file1 with the `touch file1` and added two short sentences with `gedit file1`. Apart from it, I also created another empty file named `file2`. 

<img width="866" height="252" alt="1b touch install gedit" src="https://github.com/user-attachments/assets/e795c0bd-7dbd-44e8-bb4b-379ec3a33fe7" />

<img width="934" height="534" alt="1b gedit success opening file1" src="https://github.com/user-attachments/assets/f8cfea10-7cf2-43e9-8ef3-fa1b3f49efee" />


`nano` will open Nano text editor that allows the file to be edited directly from the terminal. If I want to save the file that is updated using `nano file1`, press ctrl and o together, then press enter to confirm the changes made. 

<img width="814" height="434" alt="1b nano cmd new file" src="https://github.com/user-attachments/assets/ea275680-8cbc-480e-870a-3288503ec7f2" />
<img width="810" height="418" alt="1b nano cmd" src="https://github.com/user-attachments/assets/9caeff18-fc7c-4415-8d26-3f6fdba67aa1" />


`cat` can be used to display the content in the file like how I use for file1 and the empty file2. `less` is used to allow users to view the content of a file, `command | less` allows user to see the output of a command.  

<img width="784" height="172" alt="1b cat file" src="https://github.com/user-attachments/assets/6b22a304-d10a-4097-bfc0-ad63833785d8" />

<img width="696" height="418" alt="1b less cmd" src="https://github.com/user-attachments/assets/e70ca0a7-5039-423e-a472-4a2f8ca77be2" />

<img width="560" height="94" alt="image" src="https://github.com/user-attachments/assets/0a5ae45c-50b1-44af-abff-d437a6710f96" />


`cp file1 copyfile1`makes a copy of file1 and name it copyfile1. `mv ` is used to move the file to another location. 

<img width="830" height="432" alt="1b cp cmd copyfile1" src="https://github.com/user-attachments/assets/5f0212df-a77d-4dd8-b939-f2f84bed94d2" />


Similarly, I have made a copy of copyfile1 first, then renamed it using `mv copyfile1 documents`. Then I used `mv copyfile1 /home/cweizhe/Downloads` to move the file into the Downloads directory of my VM. Afterwards, I use `rm file2` to delete file2. 

<img width="804" height="450" alt="1b mv cmd rename file to documents" src="https://github.com/user-attachments/assets/6902d3f3-5d85-4b8c-bb56-284dae1afd51" />

<img width="840" height="376" alt="1b mv cmd move location" src="https://github.com/user-attachments/assets/bb66c524-6605-4942-a767-ef3b849b306a" />

<img width="780" height="490" alt="1b rm cmd del file" src="https://github.com/user-attachments/assets/283fbf48-c43c-43ba-a152-3c7935645153" />


The command `uname –a` is used to display a summary of all available system information.  While `lsb_release –a` is used to display the available information about the Linux Standard Base. 

<img width="822" height="350" alt="1b uname lsb release cmd" src="https://github.com/user-attachments/assets/6bf99a49-b24a-4a20-9add-a8e3496f5cc3" />


`hostnamectl` show hostname and other system information of the current machine. 

<img width="834" height="464" alt="1b hostnamectl cmdd" src="https://github.com/user-attachments/assets/245e8217-866f-4328-9f15-64df513fb746" />


**Part 3: Super User and Permissions** 

`whoami` shows my current username ‘cweizhe’, `sudo whoami` shows username ‘root’. 

<img width="596" height="274" alt="1b whoami and sudo cmd" src="https://github.com/user-attachments/assets/187bdfeb-e973-48e4-9050-3f3eb4f36783" />


When I tried to add user with `adduser `, it says that only root user has the privileges to operate this command. So, I continued with `sudo adduser testuser1` to create a new user. 

<img width="824" height="332" alt="1b adduser with sudo" src="https://github.com/user-attachments/assets/1cd00d2c-f121-4b29-82fd-994edfc03729" />


The role of root user is like an administrator that have the highest level of privileges and control within the Linux operating system. It can execute any command, modify any files, changing the permissions or ownership of files and directories, modify user’s permission on the file. It is best to have only one root user. 

**Part 4: Network Configuration and DNS** 

I have used to identify the private IP. 

<img width="822" height="478" alt="1b ip a cmd" src="https://github.com/user-attachments/assets/81e4bb0f-5683-43ef-babd-ffddd7728f29" />


The IP address `8.8.8.8` is the public DNS server of Google. We can ping using both 8.8.8.8 and google.com on the terminal as the IP address is linked to the google.com address. 

<img width="730" height="438" alt="1b ping 8 8 8 8 cmd" src="https://github.com/user-attachments/assets/fca29a43-7eb5-44f4-83c4-de2e0c12b428" />


I will use `nano` to open `/etc/hosts` and add the ip address and name it ‘dnsgoogle’ inside. So, when I ping ‘dnsgoogle’, it will ping to ‘8.8.8.8’ directly. 

<img width="830" height="584" alt="1b edit etc google dns ping" src="https://github.com/user-attachments/assets/747ce3df-7a59-4f45-9acf-9d4825a61871" />

`nslookup` helps to domain's IP address or an IP address's domain name. 

<img width="779" height="712" alt="1b nslookup google" src="https://github.com/user-attachments/assets/285e2549-5597-45d5-af0e-697e1824a178" />


I install the `whois` program with `sudo apt install whois` and check on google domain with `whois google.cpm`. 

<img width="936" height="506" alt="1b whois install cmd" src="https://github.com/user-attachments/assets/59906ecd-3817-467a-8099-3049bf69cba4" />

<img width="1028" height="558" alt="1b whois google" src="https://github.com/user-attachments/assets/6177684d-c90d-4142-a45c-f4382b23c723" />


**Part 5: System and Hardware Info** 

`lsusb` display the lists of information of the connected USB devices and `lspci` display the detailed information about all PCI buses in the system and the devices connected.  `less /proc/cpuinfo`displays the info of CPU in the terminal. 

<img width="1172" height="536" alt="1b lsusb and lspci cmd" src="https://github.com/user-attachments/assets/8dde486a-b0b3-4e7f-a328-3418ddadd84c" />

<img width="1212" height="752" alt="1b less pro cpu info cmd" src="https://github.com/user-attachments/assets/14ddf7e9-337f-464e-9430-06da202d168d" />

<img width="970" height="660" alt="1b system abt image" src="https://github.com/user-attachments/assets/1c936b4c-403c-4411-a40c-d692ca907b1e" />


`lsusb > output_of_lsusb` creates a file to input the data of the connect USB devices. Viewing the content of the file with `less` and `cat`. 

<img width="952" height="362" alt="1b lsusb file" src="https://github.com/user-attachments/assets/107b4991-3837-4361-b656-ee020b24aea2" />

<img width="776" height="210" alt="1b lsusb file less output" src="https://github.com/user-attachments/assets/e46e85cd-db7d-4884-b8c8-e6c8e10c22d9" />

<img width="1042" height="514" alt="1b lsusb file cat and rm" src="https://github.com/user-attachments/assets/a3be3419-ff2a-43f7-b02f-e4e895b922c4" />


**Part 6: Software Installation Methods**

To install chrome on Ubuntu, I went to the website and download the deb file, then I install it using the commands in the terminal. 

<img width="1134" height="636" alt="1b install chrome download file" src="https://github.com/user-attachments/assets/bce43b0e-2a32-4efe-b2fe-96a762aa061c" />

<img width="1588" height="794" alt="1b install chrome deb file success" src="https://github.com/user-attachments/assets/2df3ac8d-811a-48b5-ae75-cfdd6012dd7f" />

<img width="1152" height="512" alt="1b install chrome success open" src="https://github.com/user-attachments/assets/30f0843d-bc7a-4db5-af44-d5cc2bae6d70" />


From the App Center, I will download Discord directly, but there is a pop up that asks for the password for authentication before download can start. After input, Discord is downloaded and installed, the app can used. 

<img width="1234" height="538" alt="1b app center install app" src="https://github.com/user-attachments/assets/91125fb6-383d-4f6f-9931-de8fc89cf825" />

<img width="430" height="382" alt="1b app center install authorization" src="https://github.com/user-attachments/assets/b26fc7ab-0f0c-4ab1-9f15-4a76b5c5d5e1" />

<img width="1000" height="450" alt="1b app center install success" src="https://github.com/user-attachments/assets/b988af7e-6ed8-4e98-93af-d787fcde2584" />

<img width="1304" height="714" alt="1b app center install can run" src="https://github.com/user-attachments/assets/c5e501a2-aa34-49da-a2a8-edd504cf48fd" />


I use `sudo apt update` to find the latest package update list for the system. 

<img width="850" height="276" alt="1b sudo app update cmd" src="https://github.com/user-attachments/assets/4df0c845-bf87-4db8-b2cc-8ecad6ce0735" />


The command `sudo apt upgrade` is used to install the newer versions of all packages currently installed on the system that are available for update. 

<img width="1138" height="666" alt="1b sudo app upgrade cmd" src="https://github.com/user-attachments/assets/8dba0a6c-3658-4bb2-9ce8-1b261061b7b3" />


The command `sudo apt install vlc` is used to install the VLC package. 

<img width="1100" height="794" alt="1b sudo apt install vlc cmd" src="https://github.com/user-attachments/assets/1717f74e-8cc9-4858-861d-9b52456a11af" />


The command `sudo apt search chrome` is used to find the available packages and descriptions that match the keyword chrome. 

<img width="944" height="430" alt="1b sudo app search chrome cmd" src="https://github.com/user-attachments/assets/d98569b8-9914-448d-a475-30406af46900" />


`/etc/apt/sources.list` is used to find the repository where the packages can be found. 

<img width="824" height="336" alt="1b etc app source cmd" src="https://github.com/user-attachments/assets/71dd807e-99c3-431e-bb83-48a00db29eb1" />


Part 7: Compiling from Source (Optional)  

I will install buid essential with `sudo apt install build-essential`. Then create a C file with `touch`, use `cat > hello_world.c << “EOF” ` to write the script, then compile it using `gcc` to make it executable. It can now be executed with `./hello_world_executable`. 

<img width="832" height="776" alt="1b sudo app install build essential" src="https://github.com/user-attachments/assets/7242dde2-e2a2-4c12-abe0-a5013d15e0bf" />

<img width="974" height="622" alt="1b hello world" src="https://github.com/user-attachments/assets/66cb56f4-29a1-4e10-bbea-bb19c93a8c54" />


Then, I change the permission of the script so now anyone can read, write and execute the file. I can see the source script directly using the `less hello_world c`. 

<img width="866" height="180" alt="1b hello world permision" src="https://github.com/user-attachments/assets/2e4baa2d-e68d-4aca-8c7a-597282272d52" />

<img width="484" height="228" alt="less hello world" src="https://github.com/user-attachments/assets/28faad7d-4276-45aa-abc9-df7066efc6d5" />


When it comes to the compile file, it will show a prompt to ask if I want to see it and the output will be a binary file. 

<img width="766" height="44" alt="less hellow compile ask" src="https://github.com/user-attachments/assets/3719e28d-f094-49c6-b786-d17a5af902ba" />

<img width="1832" height="780" alt="less hellow compile output" src="https://github.com/user-attachments/assets/aaeccef4-9186-43b2-952c-1747861a3cc2" />

<img width="802" height="152" alt="less hellow compile" src="https://github.com/user-attachments/assets/5f496390-d294-4d94-acd5-a635faaf7140" />


**Lab 1a-2 reflection:**

From this activity, I would say that Nano is the better file editor as it can be open from the terminal directly for edit and it is more user friendly for beginners. 

Using CLI allows me to be more used to input the commands as Linux uses the terminal to input the commands. 

### GitHub Usage

GitHub is a cloud-based platform that enables the developers to store, manage, and collaborate on code and projects. In addition, it can also be used as a place to store notes by uploading into GitHub. In GitHub, I have created a public repository that allows anyone to access it.   

===========================================================================================


### 3. Linux Services, Permissions, and Bash Scripting 

*Service Configuration and User Permissions*
	* Services installed (e.g., NGINX, SSH). 
	* Permission controls (e.g., chmod, chown, usermod). 
	* Lessons learned on least privilege and access control. 
*Scripting and Automation* 
	* Purpose of your script (e.g., log backup). 
	* Cron job setup and testing process. 
	* Reflection on debugging and improvements. 

**Lab 1b-1 Linux Services, SSH, Firewalls & Compression**

For this activity, I start by installing apache2 using the commands and test that it will open on the browser when the IP address is typed. 

<img width="916" height="564" alt="1b install apache2" src="https://github.com/user-attachments/assets/310f76c1-078c-4f49-8d11-6949c2519a17" />


<img width="956" height="274" alt="1b open apache via ip" src="https://github.com/user-attachments/assets/f3816936-596a-4af2-8755-3a3119b3b119" />


<img width="1148" height="384" alt="1b install openssh" src="https://github.com/user-attachments/assets/8df3af4b-594e-4382-9a60-57a0d97c9e5b" />


<img width="1066" height="328" alt="1b ip a" src="https://github.com/user-attachments/assets/7b5bae65-160a-489e-97c5-7a5a23c79ee5" />


<img width="1404" height="468" alt="1b open apache via another ip" src="https://github.com/user-attachments/assets/4bcac2c4-a605-4590-9cf7-1177309eae7e" />



Nano allows user to edit the file on the terminal itself while gedit will show a GUI that allows user to edit and save like using a notepad. 

<img width="660" height="484" alt="1b edit index with nano" src="https://github.com/user-attachments/assets/843e2613-ecce-4596-9c49-67f500b105ed" />

<img width="810" height="318" alt="1b gedit nano" src="https://github.com/user-attachments/assets/21b14f28-39b1-4c5d-a4cf-7235c7fb7c37" />

<img width="904" height="494" alt="1b nmap" src="https://github.com/user-attachments/assets/44a94d95-6d3e-4c39-8824-7066382fc668" />


After removing Apache, port 80 will be open and available for other applications to use. Once Apache is reinstalled, port 80 will be configured again. 

<img width="828" height="316" alt="1b remove apache2" src="https://github.com/user-attachments/assets/7161798a-89fb-4967-9230-18a163597036" />

<img width="896" height="472" alt="1b nmap after remove apache2" src="https://github.com/user-attachments/assets/ae13ff95-2c19-4211-9412-008d42382162" />

<img width="862" height="530" alt="1b nmap after reinstall apache" src="https://github.com/user-attachments/assets/0022f887-2f7f-44ff-af6f-ca6d52079ec3" />

When UFW enables port 80, it allows connections for IPv4 and IPv6 to be available. Then I used `ssh 192.168.77.130` to connect with the IP address. Afterwards, ssh connection was successful.   

<img width="762" height="324" alt="1b sudo firewall 80tcp" src="https://github.com/user-attachments/assets/50d9483f-8eb3-407c-b45d-291354362ae1" />

<img width="920" height="662" alt="1b ssh partner ip address" src="https://github.com/user-attachments/assets/a58cfceb-22f3-476a-8153-7dd931eb910b" />


I created a new user with `sudo adduser testuser`, establish ssh connection using the username and IP address, the username on the terminal will become 'testuser’. This means that I am remotely controlling that user. 

<img width="920" height="662" alt="1b ssh partner ip address" src="https://github.com/user-attachments/assets/eb6c4361-441c-4c07-8b81-9fc131efc2cf" />


Now I use `wget -w 2 http://www.gutenberg.org/robot/harvest` to download the books from the website. `-w 2` is used to set a 2 second delay for each book downloaded. Afterwards I created a new directory named ‘books’ and moved the folder `aleph.gutenberg.org` to the directory `books`. I then create a tar with `tar cf books.tar books` then zip it with `bzip2` and unzip using `bunzip`. I can read `books.tar` with ` tar –xvf books.tar` 

<img width="908" height="104" alt="guten books collection" src="https://github.com/user-attachments/assets/e32cf12a-0bd3-45fe-9e38-0c1fb5c374f7" />

<img width="656" height="62" alt="mkdir books" src="https://github.com/user-attachments/assets/48278b74-3667-438d-bc27-de1b5cb1ac0e" />

<img width="776" height="386" alt="1b bzip files" src="https://github.com/user-attachments/assets/030c63a6-8588-4759-8751-acea6d8653d6" />

<img width="722" height="338" alt="1b bunzip2" src="https://github.com/user-attachments/assets/c0f10b68-1d65-4350-9d8a-e05478e25dd8" />

<img width="710" height="518" alt="1b taf" src="https://github.com/user-attachments/assets/5297f921-02db-4d12-92d3-2ae92d921334" />


**Virtual Networking**

First, I will power off the VM so I can clone it. Then I will open both VM together and check their ip address with `ip –a`. Next, I will ping the IP address of ‘Ubuntu-L1’ to the clone, then ping from the clone to ‘Ubuntu-L1’. The result on both VM shows that it is successful. 

<img width="1428" height="926" alt="1b clone" src="https://github.com/user-attachments/assets/57048942-0928-40a6-808d-7a6f988dd89b" />

<img width="984" height="672" alt="1b vm1" src="https://github.com/user-attachments/assets/18844e41-6391-494f-9ecf-ad4f7fb35bf6" />

<img width="946" height="634" alt="1b vm2" src="https://github.com/user-attachments/assets/72ada24c-36f2-4724-9812-bcfcbda7397e" />

<img width="1022" height="522" alt="1b vm1 ping vm2" src="https://github.com/user-attachments/assets/ec3139af-e9a5-4bc6-9165-242462fb9d70" />

<img width="922" height="418" alt="1b vm2 ping vm1" src="https://github.com/user-attachments/assets/7903b66d-80e7-402f-8ca2-e6f348e454c9" />

**Lab 1b-1 reflection:**

Firewalls manage the network services by filtering all incoming and outgoing network traffic based on security rules defined. This helps to protect the network from unauthorised personnel to access, malicious software, cyberattacks,  

SSH provides secure connection to the remote host. File compression makes the file easier for storing by removing unwanted data. 

User privilege management grants the necessary permission to prevent misuse, possible cyber-attacks. 


**Lab 1b-2 Linux File Permissions and Group Access Control**

I have created three new users, Alice, Bob and Mallory, a group, a directory and 10 test files. I then change the group ownership of the user group, added Alice and Bob into it. Then I set the directory permission to 770, only the owner and users from the group have the permission to read, write and execute the files and directory. 



Then, I changed the permission to 750, removed Mallory from the user group. I will then test using the 3 users. Alice and Bob have full permission, but Mallory does not. Afterwards, I will delete the directory. 







**Lab 1b-2 reflection:**

Linux uses mainly three permissions, read, write and execute for the owner, group and other users.  

Windows uses Access Control Lists (ACL) controls to specify which user or group has what type of permission for that file or folder. (Access-control list, n.d.)  

`chmod 770` allows the owner and group users to have permission to read, write and execute the file and directory, while other users do not have. `chmod 750` allows the owner to have read, write and execute permission, group users to read and execute, no permission for other users.  

Adding users to the sudo group allows the users apart from the owner to have the same privilege as the owner will cause the security risk of the system to increase. (Critical Linux 'sudo' flaw allows any user to take over the system, 2025)  

 

**Lab 1b-3 File Search, Analysis & Archiving in Linux** 

First, I download the file from LMS in VM and move it to `/home/cweizhe`. After I extracted it with `bunzip2` and `tar –xvf`, three files will be extracted. `ls –l` lists down the file and directories, `tree` will show the content of the directory in a treelike structure, `less “filename” ` will display the content of the file. I used `find` but nothing shows up. 

<img width="792" height="432" alt="1c downloadzip" src="https://github.com/user-attachments/assets/24038113-5fce-4578-9c06-7046a4ac89e8" />

<img width="916" height="390" alt="1c download zip file" src="https://github.com/user-attachments/assets/cbd9532d-3a7a-48e2-8bf0-9fd2ef91864e" />

<img width="769" height="351" alt="1c after bunzip 1" src="https://github.com/user-attachments/assets/3de69da3-966a-4f7e-9a4d-1e07bbe782f3" />

<img width="868" height="406" alt="1b taf file" src="https://github.com/user-attachments/assets/39e10578-fa0d-46b2-a42d-66efe48af727" />

<img width="738" height="470" alt="1b ls l" src="https://github.com/user-attachments/assets/8c9ee947-0478-4974-a33d-a03a3f349c3a" />

 <img width="620" height="534" alt="1b tree" src="https://github.com/user-attachments/assets/12700c6c-c996-4a2c-865d-02b3e8da026f" />

<img width="676" height="244" alt="1b less" src="https://github.com/user-attachments/assets/5a1996f5-8fcb-4840-b0be-5f3bfad3828c" />

<img width="976" height="96" alt="1b les fr" src="https://github.com/user-attachments/assets/3756664e-35fd-4d9e-abd7-3b5599d0b773" />

<img width="262" height="94" alt="1b moby" src="https://github.com/user-attachments/assets/c12dd10e-198b-4389-8c15-ad305f27f6ef" />

<img width="596" height="136" alt="1b les two" src="https://github.com/user-attachments/assets/8f0ecd8c-1c9b-486c-8429-a657f03e945e" />

<img width="794" height="56" alt="1b find no" src="https://github.com/user-attachments/assets/f2192c72-e97d-4eda-9e8f-c4da857ba990" />


**Lab 1b-3 reflection:**

The `tree` command can list the files and directories for the user to understand the locations of the files. Scripting helps to inform the user when unknown data has been detected. 

===========================================================================================

### 4. Cloud Infrastructure and TCO Analysis

*Cloud Deployment*
	* Which platform you used (AWS/Azure/DO). 
	* Steps taken to configure your cloud VM securely. 
	* Reflection on cloud infrastructure provisioning. 


2b-1 Cloud Web Server Deployment with Amazon EC2 

Before creating a new instance, set up the security group named 'ssh-and-web' and to enable both SSH and HTTP traffic. Select ‘Create Security Group’, name it 'ssh-and-web', the description will be ‘To allow SSH and HTTP traffic’, VPC leave it as default, then add the rule for inbound rules. Create 2 inbound rules, one for SSH and the other for HTTP, put `0.0.0.0` for the CIDR blocks. Then create it. 

<img width="2500" height="460" alt="2b sec location" src="https://github.com/user-attachments/assets/db4f2b06-2517-4557-90c5-870b1073f7e4" />

<img width="2500" height="460" alt="2b sec location" src="https://github.com/user-attachments/assets/7bd6296e-892a-4678-9667-45730e56b04f" />

<img width="1154" height="918" alt="2b sec create" src="https://github.com/user-attachments/assets/b92357cc-2f0e-4dfd-aa12-c49345b82606" />

<img width="2474" height="840" alt="2b create sec rule" src="https://github.com/user-attachments/assets/c2587841-c55a-48a8-86a5-7d14c388d3ce" />

<img width="2084" height="954" alt="2b create sec grp" src="https://github.com/user-attachments/assets/e8f7e04e-62ac-4738-aea0-4df8b90e096b" />


When creating a new instance, it requires a name for it, selecting the image that will be used, Ubuntu 20.04, then name the Key Pair as ‘BRG27’, security group choose ‘ssh-and-web'. 

<img width="1708" height="898" alt="2b setup instance" src="https://github.com/user-attachments/assets/7fc0bea3-abd6-4fb0-ae16-74f5fdfaf88b" />

<img width="1446" height="386" alt="2b setup instance key pair" src="https://github.com/user-attachments/assets/5faa4d01-83d7-4c42-8e87-8a75f791b3ae" />

<img width="1478" height="840" alt="2b setup instance sec grp" src="https://github.com/user-attachments/assets/1ea36c02-914b-44d9-a4ca-757901775a57" />

<img width="942" height="112" alt="2b key press" src="https://github.com/user-attachments/assets/96cf5882-5751-4236-9168-666edc197ff4" />


**Budget and Cost Monitoring in AWS**

From the AWS console, I can go to Billing and Cost Management Home to set up a budget alert to alert when the charges have reached the limit set. Apart from setting up the budget alert, I can also see what the cost and usage are directly from the AWS console itself. 

<img width="1858" height="782" alt="2b Biling and cost management home" src="https://github.com/user-attachments/assets/aee70144-1527-44a9-b998-5330413230ba" />

<img width="1598" height="1080" alt="2b monthly cost budget template" src="https://github.com/user-attachments/assets/9b51a9f3-9375-4c0a-a3ea-15dbf49d3c28" />

<img width="1950" height="970" alt="2b cost budget setup" src="https://github.com/user-attachments/assets/601a11a6-72bd-4f3f-ace1-92761a0bbbd1" />

<img width="1152" height="696" alt="2b cost and usage" src="https://github.com/user-attachments/assets/6e8a9b22-064b-4f42-a462-cf9adc80a19f" />


**Lab 2b-1 reflection:**

Compared to local virtualisation, cloud deployment uses pay-as-you-go, which means users only need to pay for the use of resource they have used, security measures are provided by the cloud providers. If instances are left running, the bill will increase for the resources used. 


**Lab 2b-2: Introduction to Bash Scripting & System Automation:**

For this lab, I start by creating a script with `touch hello_world.sh`, then use `nano hello_world.sh` to update the script starting with `#!/bin/bash`, then with `echo “Hello, World!” `. Afterwards, change the permission of the script to make it executable for all the users so I can execute the script with `./hello_world.sh`. 

<img width="564" height="204" alt="2b nano world" src="https://github.com/user-attachments/assets/1d5bfda1-1701-419f-892f-b984af809d2a" />


<img width="706" height="180" alt="2b create and nano world" src="https://github.com/user-attachments/assets/56384426-52c5-4957-88c8-112c43ac34d0" />

<img width="722" height="218" alt="2b echo hello world" src="https://github.com/user-attachments/assets/cd806ad3-6df1-4092-9e3b-694d14ad38c7" />


For `if`, `elif`, `else` and `read`, I used the same file to edit with nano, then add in the updated script. Now, the user will be prompt to input a number and according to the number input by the user, different text will be displayed based on user input. 

<img width="738" height="738" alt="2b sys script" src="https://github.com/user-attachments/assets/72b74a99-5410-471f-a67f-076d2a79cf0e" />

<img width="718" height="430" alt="2b sys script output" src="https://github.com/user-attachments/assets/bed62bd8-6ffa-49ff-af2c-272546066303" />

Like the previous 2 exercises I start by creating the script with `resource_monitor.sh`, then update codes that will help to retrieve CPU usage, Memory usage, and Disk usage. `free –h` will produce human readable output.   Afterwards, I will set the permission to 777 then execute it, the out will be shon the log. 

<img width="808" height="746" alt="image" src="https://github.com/user-attachments/assets/b74f93ee-ca76-4268-beb2-2ac050ce544c" />

<img width="834" height="510" alt="image" src="https://github.com/user-attachments/assets/6d90d594-5105-40ac-bb56-416c535970fc" />


**Lab 2b-2 reflection:** 

In Ubuntu, I have used `mkdir` to create a new directory, `cat` and `less` used to view the contents of a file.  

`chmod 777` is used to set the permission so the file can be read, write and executed by every user.  

The purpose of `#!/bin/bash` is to instruct the operating system on which interpreter should be used to execute the script. When there is an invalid input entered, the script will terminate when it starts to run.  

If I would monitor the network bandwidth in a Bash script, I include `netstat` in it. 


*Cost Analysis*
	* Summary of TCO comparison across providers. 
	* Criteria considered (cost, flexibility, scalability). 
	* Your platform recommendation and why. 


**Lab 2a-1 Total Cost of Ownership (TCO) Analysis**

TCO means Total Cost of Ownership, which consist of Acquisition cost like the physical hardware, software,  

For this process, we will usually research for 2 or more brands to research and analyse, the result after the we list down price of the things we must consider will be used for our decision making. 

For this scenario, I will be comparing two different brands of printers with an assumption that the printer will be used for 5 years, 750 pages to be printed per week, power on for 40 hours per week. 

We have to consider things like the type and price of the printer, what functions do the printers have, cost of the cartridges, maintenance fee, price of paper, price of cartridges, maintenance fee and etc. 


<img width="1694" height="906" alt="TCO" src="https://github.com/user-attachments/assets/cdf1d13e-ecb5-47a3-b237-935ee22a591f" />


===========================================================================================
	
### 5. DNS Setup and SSL Configuration

*DNS Management*
 	* Domain used and DNS record configuration. 
 	* Tools used to verify DNS propagation. 

*SSL Certificate with Let’s Encrypt*
 	* Certbot usage and challenges. 
 	* HTTPS redirection and security headers.
	* Reflection on the importance of encrypted traffic. 

Before creating a domain, I must ensure that the inbound ports for port 22, 80 and 443 must be open, and Apache installed. Then I have created a domain name “cweizhe22334455.online” using GoDaddy. I will then set up my A record under the DNS Records using the public IPv4 address that my instance is currently holding. The name will remain as ‘@’. Once the record has been added, it will take a while for DNS records to be in full effect across all servers on the internet.  

Afterwards, I will use `https://www.whatsmydns.net/`to check if the DNS record has been recorded in other cities. If recorded, a tick will be shown. Once the IP address of DNS has been recorded, it can now be pinged from the VM or EC2 instances.  

However, I realised that each time when the instances are on and off, the public IPv4 address of the instance will change. My original IPv4 address changed from `3.107.8.103`to `3.27.217.115`. This means that if I have not applied any service, like a Certbot, that links to the IP address of the instance, I will have to reconfigure A record on the DNS to match the current public IPv4 address. Afterwards, the DNS IP address will be fixed to the domain name. When the IP of instance has refreshed again, there will be a digital certificate linked to the domain name beside the URL. 

Certbot is a software tool that helps to generate or renew a trusted TLS certificate from the Let's Encrypt certificate authority to enable HTTPS on the selected domain. Similarly, myMurdoch Learning website has a digital certificate issued by the company DigiCert. When using Certbot to generate a certificate for the domain, there is a chance that port 80 and port 443 has been forgotten to be open for connections, causing the Certbot failing to generate the certificate. 


**Lab 3a-1 Domain, DNS and TLS Certificates with Let's Encrypt**

In this exercise, I will first ensure that the inbound ports are opened and install Apache2. From the instance summary webpage, I can find the public IP address and use it to access Apache page.  

<img width="1626" height="384" alt="3a set rule" src="https://github.com/user-attachments/assets/114751d2-3661-4f75-a885-ebdebcec8d09" />

<img width="1090" height="554" alt="3a check port open" src="https://github.com/user-attachments/assets/e60b41eb-080e-47eb-8308-5ff80a1ce125" />

<img width="1198" height="274" alt="3a install apache2" src="https://github.com/user-attachments/assets/d466a2b0-cced-441f-93de-14c74cbb3068" />

<img width="1944" height="940" alt="3a public and private ip address" src="https://github.com/user-attachments/assets/620d592b-25d4-4a20-93b4-f07963c3a646" />

<img width="2028" height="1306" alt="3a access apache website http" src="https://github.com/user-attachments/assets/5ce2d695-76fa-407e-87b0-39167bbe1265" />


Next, I will register a domain with GoDaddy, create A record that points to the public IP address of the instance, then wait for DNS propagation. Ping test and nslookup are successful.  

<img width="1132" height="742" alt="godaddy domain name purchase" src="https://github.com/user-attachments/assets/028a8f1b-f32e-4fb5-9835-c4d80250e37e" />

<img width="1106" height="574" alt="3a domain name registered" src="https://github.com/user-attachments/assets/da3ce4c7-fbae-429c-a477-43b3cd2e8ac5" />

<img width="1794" height="504" alt="3a A record created" src="https://github.com/user-attachments/assets/a004a6bc-a764-4d01-a516-a299af9211bc" />

<img width="2176" height="846" alt="3a dns propagation check" src="https://github.com/user-attachments/assets/310f7a50-87e9-4b8c-82e8-24a71c9b441d" />

<img width="1336" height="568" alt="3a nslookup after ip add change" src="https://github.com/user-attachments/assets/173a136a-99e2-4366-a281-7eed05369c56" />

<img width="1954" height="626" alt="3a ping after change ip add" src="https://github.com/user-attachments/assets/1f8fa36b-4cd0-436a-b86b-7a361d4e0ca8" />


Now, I will install and execute Certbot to generate the certificate for the domain. When the certificate is generated, I can see the certificate at the icon beside the URL of Apache page. 

<img width="1578" height="464" alt="3a cert bot update" src="https://github.com/user-attachments/assets/7fc983b3-3c27-4f8b-a474-7d8aac60f5db" />

<img width="2004" height="980" alt="3a reinstall cert" src="https://github.com/user-attachments/assets/2e4c4092-91fb-4bd7-9e2b-e98a479c46b3" />

<img width="1656" height="564" alt="3a check apache status" src="https://github.com/user-attachments/assets/1eca980a-a86c-49cf-83f2-c604becf3826" />

<img width="832" height="304" alt="3b not secure" src="https://github.com/user-attachments/assets/5e93720e-8f09-4199-b5b5-d32c177ac743" />

<img width="1164" height="1170" alt="3a certificate" src="https://github.com/user-attachments/assets/c07f9f06-38de-4cc5-89ab-b20d61d731d2" />

This is a digital certificate issued by DigiCert to the website, `https://moodleprod.murdoch.edu.au/my/ `. 

<img width="1058" height="1116" alt="murdoch web cert" src="https://github.com/user-attachments/assets/cd25299d-a21b-40a0-acc6-b27321d5c5f7" />


**Lab 3a-1 reflection**

The role of DNS is to translate the names of the domain into IP addresses for the machine to read. 

DNS propagations take time for the servers at the other side of the world to update the changes of DNS.   

Let’s Encrypt uses Certbot to validate domain ownership. Certbot will generate a unique token that will be added as a TXT record in the domain. Let’s Encrypt then queries the public DNS for the TXT record, which then validates the existence and content of the record. If the record can be found on public DNS servers, ownership is then validated. (User Guide — Certbot 5.1.0.dev0 documentation, n.d.) 

If TLS is not configured, malicious actors can attack the sites and modify the data. 

If the cloud VM is left running for months, the bill for using the VM will be high, the certificate might have expired. 



**Lab 3a-2 Enabling HTTPS with Let's Encrypt & Certbot**

Enter the website using VM, select Apache and Ubuntu via Snap. Follow the instruction to install Snap and installed a `hello-world` snap to test it. Afterwards I continued to configure the certificate, but the web page remains the same, saying that it is not secure. 

<img width="1058" height="560" alt="3a snap install" src="https://github.com/user-attachments/assets/3d8a44f8-316d-4e74-8b98-b0ce60b5e556" />

<img width="1384" height="826" alt="3b sudo" src="https://github.com/user-attachments/assets/5ceb4282-9ec5-4a20-8eab-94053763389a" />

<img width="832" height="304" alt="3b not secure" src="https://github.com/user-attachments/assets/64878eec-3750-414c-9106-2b61cb377af3" />


**Lab 3a-2 reflection:**

HTTPS uses the SSL/TLS protocol to encrypt the data transmitted between a user's browser and the website's server. The digital certificate is issued by Let's Encrypt. 

My digital certificate is valid for 3 months; it can be renewed by running the Certbot program. If digital certificate has expired and not renewed, users will see security warning messages in their browsers when visiting the domain. 

===========================================================================================

 **6. Automation and Cron Jobs**

 	* Describe cron jobs configured. 
 	* Script improvements and error handling. 
 	* Importance of automation in real-world environments. 

A cron job is a scheduled task that can be used to run a command or script at a specific time, it can be scheduled to run at a selected time or selected day of the week. (Cron - Wikipedia, n.d.) 

Automation helps to reduce human intervention to complete repetitive jobs, it also allows resources to be put to use in other areas that require more resources. Automation is important as it can help to handle repetitive tasks and not require human intervention too frequently.   


**Lab 3b-1 Bash Backup Scripting, Cron Jobs & Cloud Export:**

First, I will use `cd /home/cweizhe/Documents` to move to the directory, then create test files and directories. Next, I will input the commands into the script created, giving it permission to execute. The new zip folder will be created at `/home/cweizhe`. Afterwards, I entered the cron using `crontab –e` directly and set the time for the script to be executed. 

<img width="982" height="376" alt="3b testfile" src="https://github.com/user-attachments/assets/6eb02605-bae6-4599-b45a-ac7dbe793fdd" />

<img width="570" height="290" alt="3b nano script" src="https://github.com/user-attachments/assets/dc33b8bb-ea04-4c3b-a50d-3fece6fb17ce" />

<img width="752" height="621" alt="image" src="https://github.com/user-attachments/assets/524032e3-5e4a-454e-83ad-eda92a319889" />

<img width="788" height="60" alt="3b move sc" src="https://github.com/user-attachments/assets/f9c3b26c-2480-402e-82ae-5d4ec8a6562f" />

<img width="636" height="288" alt="3b initial cront" src="https://github.com/user-attachments/assets/f00fd122-845c-43c2-a5b3-c9e0b5e4627d" />

<img width="762" height="572" alt="3b crontab" src="https://github.com/user-attachments/assets/d7824c06-2822-472d-b198-f653f778d211" />

**Lab 3b-1 reflection:**

Absolute path is important for running scripts as it will start the execution of the script from the root until it reaches the designated directory or file. 

Benefits of cloud exporting for backups such as disaster recovery, the data are stored remotely so data can be recovered faster after events like fire, cyberattacks has hit the physical server. (4 Benefits of Using the Cloud for Disaster Recovery, n.d.) It also supports automation for backup, so it does not require the user to backup manually. 

Cron helps to execute the scripts that are created to run automated at a specific time like every day 7 pm, so users will not need to run the script manually every day. 

If the SSH keys are not accepted ahead of time, this means that the SSH keys are either not accepted by the client, or it is not present in the server's authorized_keys file. 

===========================================================================================

### 7. Consulting Simulation and Additional Server Service

*Peer Consultation Reflection*
 	* Overview of your proposed solution (stack, budget, security). 
	* Feedback received and how you incorporated it. 

*Optional Lab (Your Chosen Service)*
	* Service deployed (e.g., MariaDB, vsftpd, Docker). 
	* Configuration steps and security considerations. 
	* Reflection on learning a new service independently. 

**Lab4a-1 Additional Server Services**

For the additional server service, I have decided to do the research on the `htop` service. `htop` allows users to see all the system processes and determine the cause of the load by each process, like what Task Manager can do for Windows. It can be used to show both processes and their threads by default, and kill processes, which means that it can terminate a program or a task that is running in Linux. (How to Manage Linux Processes With htop, n.d.) 

`htop` can be installed on Ubuntu. First, use `sudo apt update`, to update the system, and `sudo apt upgrade`, to install the newest package version. 
 
<img width="950" height="524" alt="ensure apt updated" src="https://github.com/user-attachments/assets/bbdaf30e-17ec-4530-aeec-31704b8ad8bc" />

 

Install `htop` using `sudo apt install htop`: 

<img width="896" height="542" alt="htop install" src="https://github.com/user-attachments/assets/5f20388d-d33f-4267-98ed-d0fe431cda48" />

 

Input `htop` in the terminal to use it: 

<img width="574" height="52" alt="htop cmd" src="https://github.com/user-attachments/assets/99e13ccf-3fa5-4f42-8954-341be2de727e" />

<img width="1286" height="774" alt="htop output" src="https://github.com/user-attachments/assets/0101678b-83b7-4eae-bf1c-28eec9bfe57f" />


 
===========================================================================================

 

### 8. Problems Encountered and Solutions


(Create a table or list format.) | Problem | How You Solved It | |——–|——————-| | Example: SSL failure | Opened firewall and EC2 SG ports | 

| S.No | Problem | Solution |
|---|---|---|
| 1. | Unable to start up VM with VirtualBox. | Switch to VMware Workstation. |
| 2. | Failed to connect public address to domain. | Remove other A records that were added with the Domain name. |
| 3. | Failed to encrypt HTTPS on the domain. | Not resolved. |
| 4. | Cron failed to operate. | Not resolved. |
 

===========================================================================================


### 9. Industry Relevance

	* Which career roles this lab series relates to (SysAdmin, DevOps, etc.). 
	* How this experience helped build confidence in real-world skills. 
	* Mention any frameworks referenced (NIST, OWASP, SANS). 


These lab series are related to career roles like System Administrator, DevOps Engineer, Linux Engineer as these types of career roles that require a strong foundation on Linux operating system.  

This experience helps me to have a better understanding of how Linux skills is important and demanding as a real-world skill as many careers in the IT field are related to it. 

===========================================================================================


### 10. Final Reflection

	* Summarize your overall learning experience
	* What skills you improved. 
	* How you would approach future server projects differently. 


I feel that the lessons of this course are scheduled fast, four days of lesson in two weekends. It is tough to absorb that much knowledge and going through the lab activities. I would need more time to learn and train on the Linux with Ubuntu to familiarise with it. 

During these four lessons, I have learnt about Linux commands, permission, scripting, understand how to implement TCO to decide on the better equipment, understand how to use Amazon EC2 and Certbot. 

In future if I were to approach server projects, I will be careful on each step of configuration. Mistakes like typo error can cause the configuration to fail more easily. It will be hard to trace back to know cause, more time and resources will be wasted on reconfiguring. I also need to understand what the server will be used for to ensure the proper packages and setup is configured. Overall, interacting with servers needs to be careful in each portion and is best to take note of what was configured. 


===========================================================================================



### 11. AI Tools Used (if any)

	* List any AI tools (ChatGPT, Copilot) used for grammar, scripting help, etc. 

	* Be honest and specific. 

Grammarly – For citation in APA style.

===========================================================================================


**12. Appendix (Add as needed)**

	* Bash scripts 
	* Cron entries 
	* Screenshots 
	* NGINX or service config files 
	* GitHub repo file structure 

(n.d.). 4 Benefits of Using the Cloud for Disaster Recovery. Arcserve. https://www.arcserve.com/blog/4-benefits-using-cloud-disaster-recovery 

(n.d.). Access-control list. en.wikipedia.org/wiki/Access-control_list. https://en.wikipedia.org/wiki/Access-control_list 

(2025, January 7). Challenge Types - Let's Encrypt Documentation. letsencrypt.org/docs/challenge-types/. https://letsencrypt.org/docs/challenge-types/ 

(n.d.). Cron - Wikipedia. en.wikipedia.org/wiki/Cron. https://en.wikipedia.org/wiki/Cron 

(2025). Critical Linux 'sudo' flaw allows any user to take over the system. https://cybernews.com/security/critical-linux-sudo-flaw-discovered/ 

(n.d.). How to Manage Linux Processes With htop. www.makeuseof.com/htop-linux-process-manage/. https://www.makeuseof.com/htop-linux-process-manage/ 

(n.d.). User Guide — Certbot 5.1.0.dev0 documentation. eff-certbot.readthedocs.io/using.html. https://eff-certbot.readthedocs.io/using.html 






