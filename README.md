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

![image](https://github.com/chrisfortuno/osTicket/assets/149267076/4b1fbf07-b877-4134-825e-41376d492946)

![image](https://github.com/chrisfortuno/osTicket/assets/149267076/73243a27-ceb3-43c3-89b6-2177db90b3b0)

![image](https://github.com/chrisfortuno/osTicket/assets/149267076/417bb08f-4250-4ccf-a86b-fff279446cb0)

![image](https://github.com/chrisfortuno/osTicket/assets/149267076/8e10d837-58ca-4141-8fe9-535e4e8ba6c2)


next, we add permissions, click 'select principle' and type 'everyone' in order to give everyone permission to have full control over the .php file

![image](https://github.com/chrisfortuno/osTicket/assets/149267076/6f102ac2-307c-47cd-9196-996ec6e8aea1)

now we can continue setting up osTicket in the browser after clicking 'Continue'

![image](https://github.com/chrisfortuno/osTicket/assets/149267076/65fc8323-7ce7-46fb-8a67-00181126a9d6)


Fill out the system settings and admin user fields to continue to osTicket installation 

![image](https://github.com/chrisfortuno/osTicket/assets/149267076/62d2006b-57fd-4f5c-acb6-48d0c968590f)

Download and install HeidiSQL, which is a client that allows us to interact with the SQL database from osTicket

![image](https://github.com/chrisfortuno/osTicket/assets/149267076/5ae5f734-67ee-4040-b12e-75a5c928df3f)

![image](https://github.com/chrisfortuno/osTicket/assets/149267076/73addba7-5bb1-4934-aa28-d3ffd6f1379e)

![image](https://github.com/chrisfortuno/osTicket/assets/149267076/097dca3c-b3fc-4c30-a4f1-2f05343ae832)

![image](https://github.com/chrisfortuno/osTicket/assets/149267076/025060d8-d808-4727-854e-df07b49f4ff7)

Next, create a new session in HeidiSQL, use whatever username and password you chose earlier. Then, go back to the osTicket browser and connect to the session in the 'Database settings' section using the same username and password. Afterwards, go back to HeidiSQL and create a new database and name it 'osTicket', then click 'Install Now'

![image](https://github.com/chrisfortuno/osTicket/assets/149267076/c1177fb8-fc44-464f-8730-bce9b690d647)

If everything was done correctly, we should see this screen that says installation was succeessful

![image](https://github.com/chrisfortuno/osTicket/assets/149267076/beff84b8-d53d-46cf-8b45-90d834fa35b3)

![image](https://github.com/chrisfortuno/osTicket/assets/149267076/754d3028-d127-48d8-bc8a-3aa4c0031041)

Lastly, delete C:\inetpub\wwwroot\osTicket\setup and set permissions to 'read only': C:\inetpub\wwwroot\osTicket\include\ost-config.php

![image](https://github.com/chrisfortuno/osTicket/assets/149267076/8c276e2a-2517-44f7-b8e3-5d8f47496af4)

![image](https://github.com/chrisfortuno/osTicket/assets/149267076/1e1a4cb4-72cd-4bf4-982c-0baa77ad2ced)

Go to the login page with this link: (http://localhost/osTicket/scp/login.php) then putting in the username and password you chose and you should be logged in to the osTicket dashboard  


































</p>
<br />





