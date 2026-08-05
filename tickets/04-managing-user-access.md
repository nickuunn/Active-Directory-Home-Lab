<h2>Ticket #04: Managing User Access</h2>

<p><strong>Reported Issue:</strong><br/>
Pete Parker from the HR department is transitioning over to the Finance department. His user access must be changed so that he no longer has access to any files containing sensitive HR information.</p>

<p><strong>Priority:</strong> High</p>

<p><strong>Environment:</strong> Windows 10 Pro client (WIN10-CLIENT01), user account "thern" in the Customer Support OU, domain-joined to mydomain.local</p>

<p><strong>Troubleshooting Steps:</strong></p>
<ol>
  <li>Confirmed with HR/manager that Tracy's last day had passed and offboarding was authorized before taking any action.</li>
  <li>Opened Active Directory Users and Computers on the DC and located Tracy Hernandez's account in the Customer Support OU.</li>
  <li>Right-clicked the account and selected "Disable Account" to immediately revoke login access.</li>
  <li>Moved the disabled account into a dedicated "Disabled Users" OU to keep active-employee OUs clean and simplify future access audits.</li>
</ol>

<p><strong>Root Cause:</strong><br/>
Not a technical issue — a standard offboarding action following an employee's voluntary resignation and completed notice period.</p>

<p><strong>Steps Taken to Resolve:</strong><br/>

<p align="center">
Located the user "Tracy Hernandez" and disabled the account: <br/>
<img src="../screenshots/ticket04ss1.png" height="80%" width="80%"/>
<br />
<br />
Moved the disabled account to the "Disabled Users" OU to keep things organized: <br/>
<img src="../screenshots/ticket04ss2.png" height="80%" width="80%" alt="Resolution step"/>
<br />
<br />
Confirmed that the disabled account was no longer able to sign in: <br/>
<img src="../screenshots/ticket04ss3.png" height="80%" width="80%"/>
<br />
<br />




</p>

<p><strong>What I Learned:</strong><br/>
In this project I learned how to disable a user's account. Along with learning how to move the disabled account to a dedicated "Disabled Users" OU in order to keep things neat and abide by the best practices.</p>

<p><a href="https://github.com/nickuunn/Active-Directory-Home-Lab/tree/main/tickets">← Back to tickets</a></p>
