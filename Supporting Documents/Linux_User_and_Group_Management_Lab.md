# Overview
To understand how to set up users and groups, manage file and directory permissions, and apply various permission scenarios in a Linux environment.

## Step 1: Create Users and Groups
### Create Two User Accounts:
This command creates two users: `Ulises` and `Brian`.
```bash
sudo useradd Ulises
sudo useradd Brian
```
### Create a Group and Add Users:
This creates a new group called `corp_sec` and adds both `Ulises` and `Brian` to this **group**.
```bash

sudo groupadd corp_sec
sudo usermod -aG corp_sec Ulises
sudo usermod -aG corp_sec Brian
```
### Verify Group Membership:
Check if users are added to the group by using:
```bash
groups Ulises
groups Brian
```
## Step 2: Create Directories and Files with Specific Permissions
### Create a Shared Directory for the corp_sec group:
```bash
sudo mkdir /corp_sec_shared
sudo chown :corp_sec /corp_sec_shared
sudo chmod 770 /corp_sec_shared
```
This sets `corp_sec` as the group owner of `/corp_sec_shared` and grants `read`, `write`, and `execute` **permissions** for the `group`, while denying access to others.

### Create a Private Directory for Ulises:
This grants `Ulises` **full permissions** on `/home/Ulises/private` but denies access to all other users.
```bash
sudo mkdir /home/Ulises/private
sudo chown Ulises:Ulises /home/Ulises/private
sudo chmod 700 /home/Ulises/private
```

### Create a Shared File in /corp_sec_shared and Assign Permissions:
This allows members of the `corp_sec` group to `read` and `write` to `shared_file.txt`, but others cannot access it.
```bash
sudo touch /corp_sec_shared/shared_file.txt
sudo chown :cor_sec /corp_sec_shared/shared_file.txt
sudo chmod 660 /corp_sec_shared/shared_file.txt
```

## Step 3: Practice Scenarios with Permissions
### Scenario 1: 
Ulises creates a file in /corp_sec_shared.

1. Login as Ulises:
```bash
sudo -u Ulises bash
```
2. Create a file in the `/corp_sec_shared` **directory**:
```bash
touch /corp_sec_shared/Ulises_file.txt
```
3. Check the file’s permissions:
```bash
ls -l /corp_sec_shared/Ulises_file.txt
```
### Scenario 2: 
Brian attempts to read Ulises’ private directory.

1. Login as Brian(If you are still signed in as ulises, type `exit`  first in order to logout as ulises):
```bash
sudo -u Brian bash
```
Try accessing the private directory for `Ulises`:
```bash
ls /home/Ulises/private
```
**Expected Result:** Permission denied message since `Brian` has no access to `Ulises’` **private directory**.

### Scenario 3: 
Modifying Group Permissions on a Shared File.

1. Change the permissions of `shared_file.txt` to make it **read-only** for the `corp_sec group`(If you are still signed in as brian, type `exit`  first in order to logout as brian):
```bash
sudo chmod 440 /corp_sec_shared/shared_file.txt
```
2. **Test:** Log in as Ulises or Brian and attempt to write to the shared_file.txt.
**Expected Result:** Both users should see a Permission denied message, as the file is now read-only for the group.
## Step 4: Clean-Up (Optional)
Remove the created users, group, and directories if they’re no longer needed:
```bash
sudo userdel Ulises
sudo userdel Brian
sudo groupdel corp_sec
sudo rm -rf /corp_sec_shared /home/Ulises/private
```
## Summary
- User and Group Management: Created users, assigned them to groups, and verified group membership.
- File and Directory Permissions: Assigned read, write, and execute permissions to different users and groups.
- Permission Scenarios: Practiced different scenarios to see how permissions affect access control.
