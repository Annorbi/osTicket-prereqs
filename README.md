# osTicket Prerequisites and Installation
A guide on what you need to get osTicket up and running

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
- A wWndows virtual machine
- osTicket installation files which can be found <a href="https://drive.google.com/uc?export=download&id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD">here



<h2>Installation Steps</h2>

<p>Make sure to create a ressource group and a virtual machine if you haven't done so. If you don't know how to do so, a link will be provided for <a href="https://drive.google.com/uc?export=download&id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD">ressource group,
  as well as a <a href="https://drive.google.com/uc?export=download&id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD">virtual machine.</p>


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
On the lefthand side of the window, find "turn windows features on or off" and click on it. Fullscreen the window and find the "Internet Information Services" and click the little plus button next to it. Do the same for "World Wide Web Services" and "Application Developemtn Features" until you find "CGI". Go ahead and turn that on and press "ok".A window should've popped up saying that it's installing the features. Wait for it to finish and then press "close".You can now exit the "Windows Features" window.
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
On this screen, go ahead and enter a username and password that's easy to remember. For this example, we will be using "root" for both the username and password. If you want, you can also open "notepad" to write the info down. Press "next" and on the following screen, hit "execute". Wait for stuff to be installed and press "finish".
<br />

<p>
<img src="https://i.imgur.com/8AdlXf2.png" height="80%" width="80%"
</p>
<p>
On your keyboard, press the "windows key" and "e" simultanously to open file explorer. From there, navigate to "This PC". After, press the c:/ drive "Windows (C:)". From here, Go ahead and create a new folder by right-clicking inside the folder until you see "new" and then "folder". Name it "PHP".
<br />

<p>
<img src="https://i.imgur.com/8AdlXf2.png" height="80%" width="80%"
</p>
<p>
On the search bar, type in "CGI
<br />
