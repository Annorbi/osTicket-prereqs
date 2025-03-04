


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

- Windows 10</b> (22H2)

<h2>List of Prerequisites</h2>

- A ressource group
- A Windows virtual machine
- osTicket installation files which can be found <a href="https://drive.google.com/uc?export=download&id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD">here



<h2>Installation Steps</h2>

<p>Make sure to create a ressource group and a virtual machine if you haven't done so. If you don't know how to do so, a link will be provided. 
<p></p><a href="https://drive.google.com/uc?export=download&id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD"> How to create a ressource group.

<p></p><a href="https://drive.google.com/uc?export=download&id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD"> How to create a virtual machine.</p>


<p>
<img src="https://i.imgur.com/jkDDYDx.png" height="80%" width="80%"
</p>
<p>
Once you have your virtual machine up and running, go ahead and open up "Microsoft edge" and copy/paste the osTicket installation files. Download the files and save them on your desktop.
</p>
<br />

<p>
<img src="https://i.imgur.com/jkDDYDx.png" height="80%" width="80%"
</p>
<p>
Once the files have been downloaded, right click and select "extract all".
</p>
<br />

<p>
<img src="https://i.imgur.com/xFOutQE.png" heigh="80%" width="80%"
</p>
<p>
On the next screen, set the destination to the desktop by clicking "browse" and navigating until you find the desktop. Afterwards, click "select folder"
</p>
<br />

<p>
<img src="https://i.imgur.com/8AdlXf2.png" height="80%" width="80%"
</p>
<p>
Leave the extracted folder aside for now and search for "Control Panel" on the windows search bar at the bottom. From there, find "Programs" and then "Programs and features".
<br />

<p>
<img src="https://i.imgur.com/8AdlXf2.png" height="80%" width="80%"
</p>
<p>
On the lefthand side of the window, find "turn windows features on or off" and click on it. Fullscreen the window and find the "Internet Information Services" and click the little plus button next to it. Notice that "World Wide Web Services" and "Application Developemtn Features" are already turned on, do not mess with them. Keep going until you find "CGI". Go ahead and turn that on and press "ok". A window should've popped up saying that it's installing the features. Wait for it to finish and then press "close".You can now exit the "Windows Features" window.
<br />

<p>
<img src="https://i.imgur.com/8AdlXf2.png" height="80%" width="80%"
</p>
<p>
Back to the osTicket installation folder, install "VC_Redist.x86", "rewrite_amd64_en-US" and "PHPManagerForIIS_V1.5.0". These three should install instantly with no issues.

<p>
<img src="https://i.imgur.com/8AdlXf2.png" height="80%" width="80%"
</p>
<p>
Next, Install "mysql-5.5.62-win32". Click "next", accept the terms in the liscense agreement and click "next". Click "typical" when choosing the setup type, and click "Install". Make sure that "Launch the MSQ Installation Wizard" box is checked and press "finish".
<br />

<p>
<img src="https://i.imgur.com/8AdlXf2.png" height="80%" width="80%"
</p>
<p>
A new window should've been opened. Press "Next" to continue. On the next page, press "standard configuration" and press "next". Press next again, making sure "Install as a windows service" box is checked.
<br />

<p>
<img src="https://i.imgur.com/8AdlXf2.png" height="80%" width="80%"
</p>
<p>
On this screen, go ahead and enter a password that's easy to remember. For this example, we will be using "root". If you want, you can also open "notepad" to write the info down. Note that the username is "Root". Press "next" and on the following screen, hit "execute". Wait for stuff to be installed and press "finish".
<br />

<p>
<img src="https://i.imgur.com/8AdlXf2.png" height="80%" width="80%"
</p>
<p>
On your keyboard, press the "windows key" and "e" simultanously to open file explorer. From there, navigate to "This PC". After, press the c:/ drive "Windows (C:)". From here, Go ahead and create a new folder by right-clicking inside the folder until you see "new" and then "folder". Name it "PHP". Do not close the window.
<br />

<p>
<img src="https://i.imgur.com/8AdlXf2.png" height="80%" width="80%"
</p>
<p>
Back to the osTicket installation folder, extract "upload" in the same folder. Navigate to the newly extracted files and rename "upload" to "osTicket" written exactly like that. Copy the file and navigate the (c:) drive until you reach "inethub". Click on it and find "wwwroot". Click on it and paste the folder copied earlier. Afterwards, navigate the folder until you find "include/ost-sample-config.php". Remove the "sample" so it becomes "include/ost-config.php". Afterwards, right click the file and hit "propreties", find the "security" section and find "advanced" and click "disable inheritance". Click the second option when prompted.
<br />

<p>
<img src="https://i.imgur.com/8AdlXf2.png" height="80%" width="80%"
</p>
<p>
After, click "add", "select and principal" and for the "object name" type in "Everyone". Press "ok". Press on "full control" and press "ok". Exit out of that window and press "apply" and "ok".
<br />

<p>
<img src="https://i.imgur.com/8AdlXf2.png" height="80%" width="80%"
</p>
<p>
On the search bar, type in "IIS" as an admin.
<br />

<p>
<img src="https://i.imgur.com/8AdlXf2.png" height="80%" width="80%"
</p>
<p>
Find "CGI" and click on it.
<br />

<p>
<img src="https://i.imgur.com/8AdlXf2.png" height="80%" width="80%"
</p>
<p>
Find "PHP manager" and register. 
<br />

<p>
<img src="https://i.imgur.com/8AdlXf2.png" height="80%" width="80%"
</p>
<p>
For the path, navigate to where we created and installed PHP earlier. (c:\PHP\php-cgi.exe). Navigate until you find the executable. Press "ok" Stop and start the server.
<br />


<p>
<img src="https://i.imgur.com/8AdlXf2.png" height="80%" width="80%"
</p>
<p>
Still in the same window, find "php extensions" and click on "enable or disable an extension". Find "php_imap.dll", "p0hp_intl.dll" and php_opcache.dll. Enable them by right-clicking and pressing "enable" on each of them. These are necessary to allow osTicket to run correctly.
<br />

<p>
<img src="https://i.imgur.com/8AdlXf2.png" height="80%" width="80%"
</p>
<p>
Afterwards, navigate the lefthand side until you find "osTicket". Click on it and browse. the osTicket site should've popped up.
<br />

<p>
<img src="https://i.imgur.com/8AdlXf2.png" height="80%" width="80%"
</p>
<p>
Click next a couple of times until you are greated with this page. Go ahead and name your helpdesk, and input an email. For the admin settings, Fill in your name and add an email different from the one used previously.
<br />

<p>
<img src="https://i.imgur.com/8AdlXf2.png" height="80%" width="80%"
</p>
<p>
For the database settings, the first two bars should've been already filled, don't touch them. For the MySQL database, enter "osTicket". For the MySQL Username and password, enter the configuration you created when installing MySQL, for this example, we used "Root" for both. Press "Install Now" and wait.
<br />

<p>
<img src="https://i.imgur.com/8AdlXf2.png" height="80%" width="80%"
</p>
<p>
For the database settings, the first two bars should've been already filled, don't touch them. For the MySQL database, enter "osTicket". For the MySQL Username and password, enter the configuration you created when installing MySQL, for this example, we used "Root" for both. Press "Install Now" and wait.
<br />

<p>
<img src="https://i.imgur.com/8AdlXf2.png" height="80%" width="80%"
</p>
<p>
In the meantime, go back to the osTicket installation files and install "Heidi SQL". Agree to the terms and press "next" until you reach the page that says "Ready to install". Press the install button and wait for it to be installed. After that, press "finish", making sure that "Launch HeidiSQL" box is ticked on. 
<br />

<p>
<img src="https://i.imgur.com/8AdlXf2.png" height="80%" width="80%"
</p>
<p>
On this window, press "skip". Then, press "new" and enter your password that you created for root. A bunch of folders should've appeared, including one called "osTicket".
<br />

<p>
<img src="https://i.imgur.com/8AdlXf2.png" height="80%" width="80%"
</p>
<p>
After all of this, osTicket should be up and running, congrats on following this tutorial on how to get osTicket up and running. Make sure to clean stuff up like deleting the "setup" folder in C:\inetpub\wwwroot\osTicket\setup, as well as
setting permissions to “Read” only in the "ost-config.php" file located in C:\inetpub\wwwroot\osTicket\include\ost-config.php
<br />

<p>
<img src="https://i.imgur.com/8AdlXf2.png" height="80%" width="80%"
</p>
<p>
You can now access the osTicket site as an admin <a href=http://localhost/osTicket/scp/login.php>here and as a user <a href=http://localhost/osTicket/>here.
<br />

