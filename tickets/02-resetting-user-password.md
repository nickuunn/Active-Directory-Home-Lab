<h2>Ticket #02: Resetting a User's Password</h2>

<p><strong>Reported Issue:</strong><br/>
John Flem from the Finance department states that he had lost the sticky note that has his computers password on it. He would like the password reset so that he can get back to work.</p>

<p><strong>Priority:</strong> High</p>

<p><strong>Environment:</strong> Windows 10 Pro client (WIN10-CLIENT01), user account "jsmith" in the IT OU, domain-joined to corp.local</p>

<p><strong>Troubleshooting Steps:</strong></p>
<ol>
  <li>Verified the exact error message on the client. Confirmed it stated that the account was locked out.</li>
  <li>Confirmed with the user that it was caused by repeated failed login attempts.</li>
  <li>Opened Active Directory Users and Computers on the DC and located the affected user account.</li>
  <li>Checked the Account tab and confirmed the "account is locked out" flag was active.</li>
</ol>

<p><strong>Root Cause:</strong><br/>
The user typed their password in correctly but the "caps lock" key was on.</p>

<p><strong>Steps Taken to Resolve:</strong><br/>

<p align="center">
Confirmed that John Flem was locked out due to forgotten password: <br/>
<img src="../screenshots/ticket02ss1.png" height="80%" width="80%"/>
<br />
<br />
Navigated to John Flem's account and unlocked it. Along with setting a new password that John Flem will be prompted to change when he signs in: <br/>
<img src="../screenshots/ticket02ss2.png" height="80%" width="80%" alt="Resolution step"/>
<br />
<br />
Confirmed that Billy Joe was now able to sign in: <br/>
<img src="../screenshots/ticket02ss3.png" height="80%" width="80%"/>
<br />
<br />
Confirmed that Billy Joe was now able to sign in: <br/>
<img src="../screenshots/ticket02ss4.png" height="80%" width="80%"/>
<br />
<br />




</p>

<p><strong>What I Learned:</strong><br/>
In this project I learned how to unlock a user's account after multiple failed password attempts on their part. I also learned how to modify group password policies so that I could simulate this ticket.</p>

<p><a href="https://github.com/nickuunn/Active-Directory-Home-Lab/tree/main/tickets">← Back to tickets</a></p>
