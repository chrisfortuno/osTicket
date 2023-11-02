<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Enable Information Information Services (IIS)
- Install Web Platfom Installer
- Install MySQL, set up Username and Password
- Install C++ Redistributable
- Configure permissions and install osTicket

<h2>Installation Steps</h2>

![image](https://github.com/chrisfortuno/osTicket/assets/149267076/d9266148-ab94-4f58-bdcb-8c763de831ad)




Setting up a virtual machine inside of Micrsoft Azure that runs Unbutu, making sure port 3389 is enabled so we can control it with our local PC
</p>
<br />

![image](https://github.com/chrisfortuno/osTicket/assets/149267076/6d9e79f0-4d56-49ea-9c08-39f9f666a7b8)

![image](https://github.com/chrisfortuno/osTicket/assets/149267076/b32460be-35ae-4725-a288-1b4f83f2e9c3)


<p>
Enabling IIS (Internet Information Services) inside of our Virtual Machine so we can have a web server to host our web application (osTicket)
</p>
<br />

![image](https://github.com/chrisfortuno/osTicket/assets/149267076/05e20adc-a862-4e3b-b736-65d396fff0a5)

![image](https://github.com/chrisfortuno/osTicket/assets/149267076/77f41e64-4c40-4f4b-a8d3-c3190a9717e4)

![image](https://github.com/chrisfortuno/osTicket/assets/149267076/e713d1bd-02b8-4789-847d-2e86e1cb5b15)

![image](https://github.com/chrisfortuno/osTicket/assets/149267076/81221991-efc5-4217-975c-e85bc257b3b9)

![image](https://github.com/chrisfortuno/osTicket/assets/149267076/a3313c24-f7b6-492c-85b5-5643bdb9c16a)

Downloading and installing prerequisit software for IIS (PHP Manager, Rewrite Module, MySQL, C++ Redistributable), and creating a folder in the (C:) drive of our virtual machine for PHP to download into
</p>
<br />

![image](https://github.com/chrisfortuno/osTicket/assets/149267076/93e21c52-9e71-4810-9b2a-97c7ef1f0fe0)

setting up our root password for the SQL server

![image](https://github.com/chrisfortuno/osTicket/assets/149267076/70a92b09-723e-4b35-82c4-1bcb41068b3a)

setting up the SQL database on the virtual machine so osTicket has a place to store its application data

![image](https://github.com/chrisfortuno/osTicket/assets/149267076/39a88743-a9a6-4acc-8211-aa33f5de19fa)

![image](https://github.com/chrisfortuno/osTicket/assets/149267076/8964864d-6c2f-4273-99ca-bcc2c27d23f2)

Opening IIS as an administrator and registering PHP within IIS

![image](https://github.com/chrisfortuno/osTicket/assets/149267076/10ae140a-5f90-4b97-be49-f0517c8fecdb)

![image](https://github.com/chrisfortuno/osTicket/assets/149267076/37b1b840-da51-4f1b-ba3a-d7dddbc14e06)



after downloading osTicket, extracting and copying the 'upload' folder in the osTicket file to c:\inetpub\wwwroot then renaming the 'upload folder to osTicket

![image](https://github.com/chrisfortuno/osTicket/assets/149267076/3080f00d-4730-4cfd-9b2f-03f455ccea54)

![image](https://github.com/chrisfortuno/osTicket/assets/149267076/3ba6b46f-41fb-4e5f-be22-e8f90d3523d8)

After restarting IIS, access the osTicket application by selecting 'browse*.80 (http)' in the osTicket folder inside of IIS

![image](https://github.com/chrisfortuno/osTicket/assets/149267076/1b9910f4-00aa-41ce-8605-403dfe451ec9)

![image](https://github.com/chrisfortuno/osTicket/assets/149267076/24a02a1a-c771-43a7-8e11-9778aa5feed5)

![image](https://github.com/chrisfortuno/osTicket/assets/149267076/15e8aed2-478e-4a59-9ed2-ca1bfe1a7c6e)

![image](https://github.com/chrisfortuno/osTicket/assets/149267076/15ebad54-2a73-4cba-bd95-2db2fa91eeaf)



Enable some of the extensions that are 'X'd' out inside of PHP Manager, then refreshing osTicket to observe the changes 

![image](https://github.com/chrisfortuno/osTicket/assets/149267076/2144d78d-2ffb-436b-989c-dc9c65a2282e)

renaming C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php
to: C:\inetpub\wwwroot\osTicket\include\ost-config.php


![image](https://github.com/chrisfortuno/osTicket/assets/149267076/3fdf9c1d-23a1-4c5d-ab4b-459924e62cc6)

![image](https://github.com/chrisfortuno/osTicket/assets/149267076/756c0b26-8960-4b84-ab8c-a04284b3f97f)


Click 'disable inheritence' in the advanced security settings of the 'ost-config.php' file, in order to get the config file to stop inheriting permissions from its parent file. Afterwards, we click 'remove all inherited permissions from this object'











</p>
<br />





