<img width="935" height="577" alt="image" src="https://github.com/user-attachments/assets/12f0f59a-8736-499c-abdc-66d09cdba44d" />

<h1>Confiuring Ubunutu Linux on VM</h1>
Ubuntu Linux is a user-friendly, open-source operating system widely used in enterprise environments for servers, cloud infrastructure, and secure application deployment. Its long-term support releases and robust security features make it a top choice for IT teams.
<h2>Description</h2>
In this lab, we will add an Ubunutu Linux machine to our virtual homelab. We will them explore some of its features like navigating the command line, analyzing filesystem hierarchy/permissions and keeping system up to date. At the end, we will add the Ubunutu VM to the Windows Domian we previously created.
<br />


<h2>Technologies Used</h2>

- <b>VirtualBox</b> 
- <b>Ubuntu Linux</b>

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


