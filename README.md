
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

<p>Make sure you have a ressource group and a virtual machine setup. If you do not know how to do so, links will be provided for both steps. 
<p></p> <a href="https://github.com/Annorbi/Ressource-Group">How to create a ressource group.

<p> <a href="https://github.com/Annorbi/Virtual-Machines">How to create a virtual machine.
</p>


<p>
<img src="https://i.imgur.com/ra9iYVD.png" height="80%" width="80%"
</p>
<p>
Once you have your virtual machine up and running, go ahead and open up "Microsoft edge" and copy/paste the osTicket installation files from above. Download the files.
</p>
<br />

<p>
<img src="https://i.imgur.com/rni9SJU.png" height="80%" width="80%"
</p>
<p>
Once the files have been downloaded, open your "Downloads" folder and right click to extract. On the next screen, set the destination to the desktop by clicking "browse" and navigating until you find the desktop. Afterwards, click "select folder" Extract the files to the desktop.
</p>
<br />

<p>
<img src="https://i.imgur.com/Fd71aU1.png" height="40%" width="40%" <p> <img src="https://i.imgur.com/Z9nnRGf.png" height="40%" width="40%"
</p>
<p>
Leave the extracted folder aside for now and search for "Control Panel" on the windows search bar at the bottom. From there, find "Programs" and then "Programs and features".
<br />

<p>
<img src="https://i.imgur.com/im1ztG2.png" height="40%" width="40%" <p> <img src="https://i.imgur.com/tHvFdF7.png" height="40%" width="40%"
</p>
<p>
On the lefthand side of the window, find "turn windows features on or off" and click on it. Fullscreen the window and find the "Internet Information Services" and click the little plus button next to it. Notice that "World Wide Web Services" and "Application Developpement Features" are already turned on, do not mess with them. Keep going until you find "CGI". Go ahead and turn that on and press "ok". A window should've popped up saying that it's installing the features. Wait for it to finish and then press "close". You can now exit the "Windows Features" window.
<br />

<p>
<img src="https://i.imgur.com/nassrBv.png" height="50%" width="50%"
</p>
<p>
You can now open up the extracted osTicket installation files. From there, install "VC_Redist.x86", "rewrite_amd64_en-US" and "PHPManagerForIIS_V1.5.0". These three should install very easily with no issues.

<p>
<img src="https://i.imgur.com/j7f69bq.png" height="40%" width="40%" <p> <img src="https://i.imgur.com/pCFF8EW.png" height="40%" width="40%"
</p>
<p>
Next, Install "mysql-5.5.62-win32". Click "next", accept the terms in the liscense agreement and click "next". Click "typical" when choosing the setup type, and click "Install". Make sure that "Launch the MSQ Installation Wizard" box is checked and press "finish".
<br />

<p>
<img src="https://i.imgur.com/Ubx8EXw.png" height="50%" width="50%"
</p>
<p>
A new window should've been opened. Press "Next" to continue. On the next page, press "standard configuration" and press "next". Press next again, making sure "Install as a windows service" box is checked.
<br />

<p>
<img src="https://i.imgur.com/ISEXpOu.png" height="50%" width="50%"
</p>
<p>
On this screen, go ahead and enter a password that's easy to remember and make sure to remember it. For this example, we will be using "root". If you want, you can also open "notepad" to write the info down. Note that the username is "Root". Press "next" and on the following screen, hit "execute". Wait for stuff to be installed and press "finish".
<br />

<p>
<img src="https://i.imgur.com/7Ac5bDC.png" height="40%" width="40%" <p> <img src="https://i.imgur.com/F4IhXZa.png" height="40%" width="40%" 
</p>
<p>
Minimize the installation folder for right, we'll come back to it later. On your keyboard, press the "windows key" and "e" simultanously to open file explorer. From there, navigate to "This PC". After, press the c:/ drive "Windows (C:)". From here, Go ahead and create a new folder by right-clicking inside the folder until you see "new" and then "folder". Name it "PHP". From there, go back to the installation folder and right-click "php-7.3.8-nts-Win32-VC15-x86" and extract it to the new folder we just created. Close the newly extracted "PHP" folder but leave the "(c:) drive" folder up.
<br />

<p>
<img src="https://i.imgur.com/TGuSTUp.png" height="30%" width="30%" <p> <img src="https://i.imgur.com/8OpqnRs.png" height="30%" width="30%" <p> <img src="https://i.imgur.com/EPd125O.png" height="30%" width="30%" <p> <img src="https://i.imgur.com/NEkDINx.png" height="30%" width="30%"
</p>
<p>
Back to the osTicket installation folder, extract "upload" in the same folder. Navigate to the newly extracted files and rename "upload" to <b>"osTicket"</b> written exactly like this. Right-click to copy the file. After that, find "This PC" and navigate the (c:) drive until you reach "inethub". Click on it and find "wwwroot". Click on it and paste the folder copied earlier. 
<br />

<p>
<img src="https://i.imgur.com/8OpqnRs.png" height="30%" width="30%" <p> <img src="https://i.imgur.com/ZN5YwLd.png" height="30%" width="30%" <p>
  <img src="https://i.imgur.com/HI6uCsL.png" height="30%" width="30%" <p> <img src="https://i.imgur.com/DBLSJUi.png" height="10%" width="10%" <p> <img src="https://i.imgur.com/U1nRmuw.png" height="30%" width="30%" <p> <img src="https://i.imgur.com/OwIaEdS.png" height="30%" width="30%" 
</p>
<p>
Afterwards, navigate the folder until you find "include/ost-sample-config.php". Remove the "sample" so it becomes "include/ost-config.php". Afterwards, right click the file and hit "propreties", find the "security" section and find "advanced" and click "disable inheritance". Click the second option when prompted.
<br />

<p>
<img src="https://i.imgur.com/cPp9BSs.png" height="30%" width="30%" <p> <img src="https://i.imgur.com/iY7D2bl.png" height="30%" width="30%" <p> <img src="https://i.imgur.com/ywywRuM.png" height="30%" width="30%" 
</p>
<p>
After, click "add", "select and principal" and for the "object name" type in "Everyone". Press "ok". Press on "full control" and press "ok". Exit out of that window and press "apply" and "ok". You can now press "ok" on the "ost-config.php propeties" window, but minimize the "include" folder, we'll come back to it later.
<br />

<p>
<img src="https://i.imgur.com/8AdlXf2.png" height="80%" width="80%"
</p>
<p>
On the search bar, type in "IIS" as an admin.
<br />

<p>
<img src="https://i.imgur.com/qBbgrZ3.png" height="80%" width="80%"
</p>
<p>
IIS should look like this picture. Next, find "CGI" and click on it.
<br />

<p>
<img src="https://i.imgur.com/5uoPb89.png" height="80%" width="80%"
</p>
<p>
Find "PHP manager" and register. 
<br />

<p>
<img <img src="https://i.imgur.com/s6R2pYG.png" height="30%" width="30%" <p> <img src="https://i.imgur.com/9LKSX98.png" height="30%" width="30%" <p> <img src="https://i.imgur.com/jTmOf30.png" height="30%" width="30%" <p> <img src="https://i.imgur.com/wJqXhYL.png        " height="30%" width="30%" <p> <img src="https://i.imgur.com/FN0zELv.png" height="30%" width="30%" 
</p>
<p>
For the path, navigate to where we created the PHP folder and extracted "php-7.3.8-nts-Win32-VC15-x86" to earlier. (c:\PHP\php-cgi.exe). Navigate until you find the executable. Switch back to "IIS" and go back to the main page. press "ok" to "Stop" and "Start" the server.
<br />


<p>
<img src="https://i.imgur.com/sVrXRVz.png" height="50%" width="50%" <p> <img src="https://i.imgur.com/5GOFRT3.png" height="50%" width="50%"
</p>
<p>
Go back to "PHP manager" and find "php extensions" and click on "enable or disable an extension". Find "php_imap.dll". Enable them by right-clicking and pressing "enable" on each of them. Do the same for "php_intl.dll" and php_opcache.dll. These are necessary to allow osTicket to run correctly. Go back to the main menu once again.
<br />

<p>
<img src="https://i.imgur.com/pSuXiwn.png" height="80%" width="80%"
</p>
<p>
Afterwards, navigate the lefthand side until you find "osTicket". Click on it and "browse". the osTicket site should've popped up.
<br />

<p>
<img src="https://i.imgur.com/N1eY7N6.png" height="40%" width="40%"  <p> <img src="https://i.imgur.com/CBYLyNv.png" height="40%" width="40%"
</p>
<p>
From here, click "continue". On the next page, go ahead and name your helpdesk, and input an email. For the admin settings, Fill in your name and add an email different from the one used previously. Make sure to take note of your admin details, you'll need them to login on the login page.
<br />

<p>
<img src="https://i.imgur.com/8AdlXf2.png" height="80%" width="80%" 
</p>
<p>
For the database settings, the first two bars should've been already filled, don't touch them. For the MySQL database, enter "osTicket". For the MySQL Username and password, enter the configuration you created when installing MySQL, for this example, we used "Root" for both. Press "Install Now" and wait.
<br />

<p>
<img src="https://i.imgur.com/e33MceJ.png" height="80%" width="80%"
</p>
<p>
For the database settings, the first two bars should've been already filled, don't touch them. For the MySQL database, enter "osTicket". Remmeber that the MySQL username is "Root". For the MySQL password, enter the password you created when installing MySQL, for this example, we used "root". Press "Install Now" and wait.
<br />

<p>
<img <img src="https://i.imgur.com/jxC7ebK.png" height="30%" width="30%" <p> <img src="https://i.imgur.com/dyqNjY8.png" height="30%" width="30%" <p> <img src="https://i.imgur.com/VAy4RWu.png" height="30%" width="30%" <p> <img src="https://i.imgur.com/jrV9Sod.png        " height="30%" width="30%" <p> <img src="https://i.imgur.com/4gayK4h.png" height="30%" width="30%" <p> <img src="https://i.imgur.com/qUKDiQN.png" height="30%" width="30%"  <p> <img src="https://i.imgur.com/fDAWneb.png" height="30%" width="30%" 
</p>
<p>
In the meantime, go back to the osTicket installation files and install "Heidi SQL". Agree to the terms and press "next" until you reach the page that says "Ready to install". Press the install button and wait for it to be installed. After that, press "finish", making sure that "Launch HeidiSQL" box is ticked on. 
<br />

<p>
<img <img src="https://i.imgur.com/0rKChbm.png" height="30%" width="30%" <p> <img src="https://i.imgur.com/wFf3gQJ.png" height="30%" width="30%" <p> <img src="https://i.imgur.com/2ELX50S.png" height="30%" width="30%" 
<p>
On this window, press "skip". Then, press "new" and enter your password that you created for root. A bunch of folders should've appeared, including one called "osTicket". Once you see these folders, go ahead and exit out of Heidi SQL.
<br />

<p>
<img src="https://i.imgur.com/p7pp7wk.png" height="30%" width="30%" <img <img src="https://i.imgur.com/4Gfu1Q2.png" height="30%" width="30%" <p> <img src="https://i.imgur.com/dWrc1m3.png" height="30%" width="30%" <p> <img src="https://i.imgur.com/s2vLixq.png" height="30%" width="30%" <p> <img src="https://i.imgur.com/IMlRRBO.png "height="30%" width="30%" <p> <img src="https://i.imgur.com/YlcpyG4.png" height="30%" width="30%" 
</p>
<p>
After all of this, osTicket should be up and running, congrats on following this tutorial on how to get osTicket up and running! But we are not quite down yet. It's time to clean stuff up. For instance, deleting the "setup" folder in C:\inetpub\wwwroot\osTicket\setup. (Right-click -> Delete). You can exit the folder now. Remember that "include" folder I hope you minimized? Now's the time to open it and set permissions to “Read” only in the "ost-config.php". If you accidently closed the folder, the file is located in C:\inetpub\wwwroot\osTicket\include\ost-config.php. Once you do that, you can exit the folder, as well as close IIS.
<br />

<p>
<img src="https://i.imgur.com/9HNCxTy.png" height="40%" width="40%" <p> <img src="https://i.imgur.com/ZRnZj0w.png" height="40%" width="40%"
</p>
<p>
You can now access the osTicket site as an admin <a href=http://localhost/osTicket/scp/login.php>here<p> and as a user <a href=http://localhost/osTicket/>here. Congratulations (for real this time), you are now have osTicket running. It is now time to configure osTicket so that we can get ready to solve tickets.
<br />

