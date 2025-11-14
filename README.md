<img width="935" height="577" alt="image" src="https://github.com/user-attachments/assets/12f0f59a-8736-499c-abdc-66d09cdba44d" />

<h1>Confiuring Ubunutu Linux on VM</h1>
Ubuntu Linux is a user-friendly, open-source operating system widely used in enterprise environments for servers, cloud infrastructure, and secure application deployment. Its long-term support releases and robust security features make it a top choice for IT teams.
<h2>Description</h2>
In this lab, we will add an Ubunutu Linux machine to our virtual homelab. We will them explore some of its features like navigating the command line, analyzing filesystem hierarchy/permissions and keeping system up to date. At the end, we will add the Ubunutu VM to the Windows Domian we previously created.
<br />


<h2>Technologies Used</h2>

- <b>VirtualBox</b> 
- <b>Ubuntu Linux</b>
- <b>Windows Server 2022</b>

<h2>Lab walk-through:</h2>
Ubunutu VM setup

1. Download Ubuntu from this link:([https://www.virtualbox.org/wiki/Downloads](https://ubuntu.com/download/desktop)). Choose the version that matches the OS of your host computer.
 <br/>
<img width="1918" height="965" alt="image" src="https://github.com/user-attachments/assets/90b94181-faf7-416f-afa5-ac58b2d7d713" />
<br />
<br />
2. On the main menu of VirtualBox, click New > Name the VM, Select the Linux ISO image, Check "Skip Unattended Installation" > Add 4096 MB of base memeory and 2 processors > Create a virtual hard disk that is 50 GB > Check configuartions and click "Finish".
<br/>
<img width="1040" height="590" alt="image" src="https://github.com/user-attachments/assets/2ee22901-d68a-437d-9b07-065a89c84e0e" />
<br />
<br />
3. The new VM will populate on VirtualBox. Click start. The bootloader will pop up and we will choose the first selection "Try or Install Ubuntu"
<br/>
<img width="760" height="393" alt="image" src="https://github.com/user-attachments/assets/6b4a3380-006c-4694-9b04-e6f4e09b3061" />
<br />
<br />
4. Once Ubuntu starts, it will take us through the final configurations. Choose your Lanuguage > Choose your Accessibility Settings > Select Keyboard Layout > Check "Use wired connection " > Select Interactive Installation > Default Selection for Applications > Install Third Party Software > Erase Disk and Install Ubuntu > Create usernmame and password > Select Timezone > Review Selections > Click Install.
<br/>
<img width="1057" height="751" alt="image" src="https://github.com/user-attachments/assets/b37b7234-cc66-4d3a-8bf6-99def9f9ec70" />
<br />
<br />
5. Once the installtion in complete the VM will restart. Log in with your account and it is ready for use.
<br/>
<img width="1068" height="753" alt="image" src="https://github.com/user-attachments/assets/f96e34eb-daa4-4ac7-8674-c79527c9a380" />
<img width="1068" height="753" alt="image" src="https://github.com/user-attachments/assets/5d14ed2a-f765-4dc2-b217-176c0fd0b9c0" />
<br />
<br />

Navigating the Command Line
1. We will go over basic commands for navigating through the command line.

"pwd" - print working directory
 <br/>
<img width="585" height="142" alt="image" src="https://github.com/user-attachments/assets/f8e12f32-4704-4594-bcde-ba6a7797e924" />
<br />
<br />
"ls" - list directory contents
 <br/>
<img width="600" height="109" alt="image" src="https://github.com/user-attachments/assets/1b721273-b9fc-403c-afa2-0831a79c4932" />
<br />
<br />
"cd" - change directory
 <br/>
<img width="500" height="125" alt="image" src="https://github.com/user-attachments/assets/a7f6bbce-2ab0-4c9a-8855-37d5f53d6f0e" />
<br />
<br />
"mkdir" - make directory
 <br/>
<img width="399" height="114" alt="image" src="https://github.com/user-attachments/assets/67c612fd-7791-4058-a7a8-c2a5bee086f7" />
<br />
<br />
"rmdir" - remove directory
 <br/>
<img width="393" height="135" alt="image" src="https://github.com/user-attachments/assets/63b93cbb-67d2-4ea3-8bdc-3dcb97c5e6ee" />
<br />
<br />

"touch" + filename - create file 
 <br/>
<img width="408" height="107" alt="image" src="https://github.com/user-attachments/assets/cfe51355-6471-43a7-8c1f-76853acaf7b3" />
<br />
<br />

"cat" + filename - display contents of file
 <br/>
<img width="404" height="86" alt="image" src="https://github.com/user-attachments/assets/017e4cd2-b362-4afe-a32f-7667e0cef4f9" />
<br />
<br />

"rm" + filename - remove file
 <br/>
<img width="392" height="118" alt="image" src="https://github.com/user-attachments/assets/37b9363d-60d5-464e-be0a-a6e634134663" />
<br />
<br />

Connnecting to Domain
1. In this portion of the lab we will be connecting the Ubunutu VM to the Windows Domain we previously created. First, we need to make sure our Ubunutu VM is in the same VNET as the Domain Controller. On VirtualBox, Click on Ubuntu VM > Setings > Network > Adapter > Choose same network DC is located in.
 <br/>
<img width="1256" height="952" alt="image" src="https://github.com/user-attachments/assets/3dc7f03f-9dc3-4430-9ee4-69b00b771bf2" />
<br />
<br />

2. Boot up the Domain Controller and Ubuntu VMs. Log on to DC > Open Command Line > Type command "Ipconfig" > Take note of IP address. Log onto Ubuntu VM > Open Terminal > Type "sudo su" for superuser ppriviledges > Type command "ping" + IP address of DC. The purpose of this to make sure the Linux machine can connect to the Windwos machine.
 <br/>
<img width="816" height="584" alt="image" src="https://github.com/user-attachments/assets/b13a29c7-ca9d-4b25-ae9b-8cbf026a0fab" />
<br />
<br />

3. We need to point the Ubuntu VM to the DC by changing some network settings. On the Ubuntu VM, click icon on bottom left corner > Type Advanced Networking > Click Wired Connection 1 > CLick IPv4 Settings. In the box next to "Additional DNS servers"  type the IP address of the DC because it is hosting DNS.
 <br/>
<img width="1149" height="736" alt="image" src="https://github.com/user-attachments/assets/ded64786-63e1-413a-95bc-adc1dba85256" />
<br />
<br />

4. To ensure Network configuartions have been changed and updated,  type the command show below.
 <br/>
<img width="817" height="590" alt="image" src="https://github.com/user-attachments/assets/bf5aa7ae-6cc9-4a17-bf8b-5f52652bf358" />
<br />
<br />

5. Now we need to install packges required to facilitate domain discovery, authentication and user management. This will allow us to join Windows Domain from Ubunutu machine. Type the command shown below.
 <br/>
<img width="823" height="589" alt="image" src="https://github.com/user-attachments/assets/17f2e306-42d3-43c4-a6a5-0c76e95d9e4f" />
<br />
<br />

6. Next, we will chnage hostname of machine to reflect the domain we are trying to join. We will name the machine to "ubuntu" followed by your domain name. Exmaple shown below.
 <br/>
<img width="811" height="583" alt="image" src="https://github.com/user-attachments/assets/9d19017e-88b8-4e10-976f-de2a228dbe01" />
<br />
<br />

7. The next command is used to disable systemd resolve service which acts a local DNS resolver. Instead we want our Windows Machine to act as our DNS server.
 <br/>
<img width="821" height="589" alt="image" src="https://github.com/user-attachments/assets/984872d3-a945-4fe5-880d-58561e7d61fd" />
<br />
<br />

8. Now we are going to tell our Ubunutu where we are going to resolve by editing the resolv.conf file. In terminal type "nano etc/resolv.conf" > Navigate to bottom of fle > Change "namesever" to the IP address of your Windows Machine and Chnage "search" to the name of your domain.
 <br/>
<img width="814" height="583" alt="image" src="https://github.com/user-attachments/assets/4c1dc02e-2676-4b08-9681-b37a0adf106e" />
<br />
<br />

9. We will use one of the packages we installed to discover our domain. Type "realm discover" + domain name
 <br/>
<img width="823" height="579" alt="image" src="https://github.com/user-attachments/assets/64aa1829-7a09-4647-a714-12cf1f9ad4ef" />
<br />
<br />

10. Before we join the domain, I will show that the Ubunutu machine is not currently in the domain. On the WIndows machine, naviagte tu Server Manager > Tools > Active Directory Users and Computers > Computers
 <br/>
<img width="756" height="533" alt="image" src="https://github.com/user-attachments/assets/50c6801e-0333-4c45-a65c-87098025d2dd" />
<br />
<br />

11. FInally, we will join the domain using an account with administrative priviledges so we don't get any permission issues. Type "realm join -U" + username + domain name. Type in password. If no errors, we have sucessfully join the Ubunut machine to domain.
 <br/>
<img width="931" height="647" alt="image" src="https://github.com/user-attachments/assets/39b0b497-9b88-437c-972d-708a61e329e6" />
<br />
<br />

12. We can verify that the Ubunntu VM has been added by checking the same location in the previous step.
 <br/>
<img width="754" height="530" alt="image" src="https://github.com/user-attachments/assets/3f1e2312-3646-439d-807a-ff629866c380" />
<br />
<br />
