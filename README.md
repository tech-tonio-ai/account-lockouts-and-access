# Handling Account Lockouts and User Access
# Dealing with Account Lockouts

## Step 1: Log into DC-1
1. Pick a random user account you created previously.
2. Attempt to log in with it **10 times** using an incorrect password.

## Step 2: Configure Group Policy for Account Lockout
1. Set the **Account Lockout Threshold** to **5 failed attempts** in Group Policy.
2. Attempt to log in with the same account **6 times** using an incorrect password.
3. Observe that the account has been locked out in **Active Directory**.

## Step 3: Unlock the Account
1. Unlock the locked-out account.
2. Reset the password.
3. Attempt to log in again to verify the fix.

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
2. **Check the logs on the Client Machine** to review authentication attempts and errors.

---

This guide provides a hands-on approach to handling account lockouts, enabling/disabling accounts, and monitoring logs within **Active Directory**.

