<h1>Active Directory</h1>


<h2>Description</h2>
Project consists of a simple PowerShell script that walks the user through "zeroing out" (wiping) any drives that are connected to the system. The utility allows you to select the target disk and choose the number of passes that are performed. The PowerShell script will configure a diskpart script file based on the user's selections and then launch Diskpart to perform the disk sanitization.
<br />

<h2>Project walk-through:</h2>

<p align="center">
Create the Windows 10 and Windows 2022 Server machines: <br/>
<img src="screenshots/VirtualMachines.png" height="80%" width="80%"/>
<br />
<br />
Right click the network icon and select "Open Network and Internet Settings":  <br/>
<img src="screenshots/2.png" height="80%" width="80%"/>
<br />
<br />
Scroll down and click on "change adapter options" and then right click on the displayed adapter. Then click on "properties": <br/>
<img src="screenshots/3.png" height="80%" width="80%"/>
<br />
<br />
Click on the selected box and then select "properties":  <br/>
<img src="screenshots/4.png" height="80%" width="80%"/>
<br />
<br />
Fill in the boxes with the displayed settings for the sake of simplicity, then click "ok":  <br/>
<img src="screenshots/5.png" height="80%" width="80%"/>
<br />
<br />
Start the Windows 2022 Server VM and repeat the previous steps and fill in the following information:  <br/>
<img src="screenshots/6.png" height="80%" width="80%"/>
<br />
<br />
Open up the Server Manager and click "Manage" in the top right corner. Click "add roles" and then "next" and verify that the following is selected. Then click "next" and then "next" again:  <br/>
<img src="screenshots/7.png" height="80%" width="80%"/>
<br />
<br />
Select "Active Directory Domain Services" and then click "add features." Continue clicking "next" until you reach and select "install":  <br/>
<img src="screenshots/8.png" height="80%" width="80%"/>
<br />
<br />
Once it finishes installing, click "close" and return to the Server Manager Dashboard. Select the flag with the warning icon at the top right and click on "promote this server to a domain controller":  <br/>
<img src="screenshots/9.png" height="80%" width="80%"/>
<br />
<br />
Select the following option and create a name with ".local" or ".test" at the end:  <br/>
<img src="screenshots/10.png" height="80%" width="80%"/>
<br />
<br />
Create a password and then select "next." Continue clicking next until you can click "install" on the prerequisite check page:  <br/>
<img src="screenshots/11.png" height="80%" width="80%"/>
<br />
<br />
Once it is finished installing, restart the server as prompted:  <br/>
<img src="screenshots/12.png" height="80%" width="80%"/>
<br />
<br />
Log back in and return to the Server Manager Dashboard. Click on "tools" on the top right corner and select "Active Directory Users and Computers":  <br/>
<img src="screenshots/13.png" height="80%" width="80%"/>
<br />
<br />
Click the dropdown on the domain you just created:  <br/>
<img src="screenshots/14.png" height="80%" width="80%"/>
<br />
<br />
We will be creating a new organizational unit within our domain for our IT team. To do that, right click on your domain, select "new" and select "organizational unit":  <br/>
<img src="screenshots/15.png" height="80%" width="80%"/>
<br />
<br />
Next we will be creating a user for the IT department. Right click in the empty section in the IT folder, go to "new" then select user:  <br/>
<img src="screenshots/16.png" height="80%" width="80%"/>
<br />
<br />
Choose any name you want:  <br/>
<img src="screenshots/17.png" height="80%" width="80%"/>
<br />
<br />
Set a password. Also, to simplify things, you can uncheck the first box:  <br/>
<img src="screenshots/18.png" height="80%" width="80%"/>
<br />
<br />
After that you can select "next" and then "finish" to create the user:  <br/>
<img src="screenshots/19.png" height="80%" width="80%"/>
<br />
<br />
For practice, repeat the previous steps and create a new department with a new user in it:  <br/>
<img src="screenshots/20.png" height="80%" width="80%"/>
<br />
<br />





  
</p>

