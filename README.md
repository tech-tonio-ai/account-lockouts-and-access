<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>Active Directory Group Policy Objects : Account Lockouts,Access and Logs Monitoring (Azure)</h1>
This guide provides a hands-on approach to handling account lockouts, enabling/disabling accounts, and monitoring logs within Active Directory.

---


## Step 1: Configure Group Policy for Account Lockout
- Set the **Account Lockout Threshold** to **5 failed attempts** in Group Policy.
  <p align="center">
  <img src="https://i.imgur.com/0YMrW06.png" alt="Image 1" width="45%"/>  
</p>

- Log in to client-1 as admin(mydomain.com\jane_admin) and force the Group Policy update:
    - in CMD type "gpupdate /force :
<p align="center">
  <img src="https://i.imgur.com/tgHDXJ5.png" alt="gpupdate /force" width="45%"/>  
</p>
    - log out

- Attempt to log in with the same account (cub.dem) **6 times** using an incorrect password in <b>client-1</b>.
<p align="center">
  <img src="https://i.imgur.com/TnzmYBe.png" alt="gpupdate /force" width="45%"/> 
  
</p>

- Observe that the account has been locked out in **Active Directory**.
<p align="center">
<img src="https://i.imgur.com/Ry3o570.png" alt="gpupdate /force" width="45%"/>
</p>
## Step 2: Unlock the Account
- Unlock the locked-out account.
  
- Reset the password.
  
- Attempt to log in again to verify the fix.

---

# Enabling and Disabling Accounts

## Step 1: Disable the Account
1. Disable the same user account in **Active Directory**.
2. Attempt to log in and observe the error message.

## Step 2: Re-enable the Account
1. Re-enable the account in **Active Directory**.
2. Attempt to log in again to verify access.

---

# Observing Logs

1. **Check the logs on the Domain Controller** to monitor account lockout events.
<p align="center">
<img src="https://i.imgur.com/nmdR9JR.png" alt="gpupdate /force" width="45%"/>
</p>
3. **Check the logs on the Client Machine** to review authentication attempts and errors.
<p align="center">
<img src="https://i.imgur.com/z5RukJw.png" alt="gpupdate /force" width="45%"/>
</p>

---



