# -Linux-User-and-Group-Management-

# Linux User and Group Management Cheat Sheet

This **Linux User and Group Management Cheat Sheet** provides a categorized overview of essential commands for creating, modifying, and deleting users and groups. It is a handy reference for system administrators managing Linux environments.

---

## Table of Contents
1. [User Management](#user-management)
    - [useradd Command Examples](#useradd-command-examples)
    - [usermod Command Examples](#usermod-command-examples)
    - [userdel Command Examples](#userdel-command-examples)
    - [passwd Command Examples](#passwd-command-examples)
2. [Group Management](#group-management)
    - [groupadd Command Examples](#groupadd-command-examples)
    - [groupmod Command Examples](#groupmod-command-examples)
    - [groupdel Command Examples](#groupdel-command-examples)

---

## User Management

### useradd Command Examples
- **Create a New User**:
  ```bash
sudo useradd new_username

Create a User with a Home Directory:
sudo useradd -m new_username

Set a Custom Home Directory:
sudo useradd -d /custom/home/dir new_username

Assign a Default Shell:
sudo useradd -s /bin/bash new_username

Add a User to a Specific Group:
sudo useradd -g group_name new_username

Add User to Multiple Groups:
sudo useradd -G group1,group2 new_username

usermod Command Examples
Change Username:
sudo usermod -l new_username old_username

Change Home Directory:
sudo usermod -d /new/home/dir -m username

Change Default Shell:
sudo usermod -s /bin/zsh username

Add User to a Group:
sudo usermod -aG group_name username

Lock a User Account:
sudo usermod -L username

Unlock a User Account:
sudo usermod -U username

Set Expiry Date for a User Account:
sudo usermod -e YYYY-MM-DD username

userdel Command Examples
Delete a User:
sudo userdel username

Delete a User and Home Directory:
sudo userdel -r username

passwd Command Examples
Change Current User's Password:
passwd 

Set Password for a New User:
sudo passwd username

Force User to Change Password on Next Login:
sudo passwd -e username

Lock a User Account:
sudo passwd -l username

Unlock a User Account:
sudo passwd -u username

Group Management
groupadd Command Examples
Create a New Group:
sudo groupadd group_name

Create a Group with a Specific GID:
sudo groupadd -g GID group_name

Create a System Group:
sudo groupadd -r group_name

groupmod Command Examples
Change Group Name:
sudo groupmod -n new_group_name old_group_name

Change Group GID:
sudo groupmod -g GID group_name

groupdel Command Examples
Delete a Group:
sudo groupdel group_name

Handle Files Owned by Deleted Group:
find / -gid <GID> -exec chgrp new_group_name {} \;

Contributions
This cheat sheet is a work in progress. Contributions are welcome! Feel free to suggest improvements or submit issues and pull requests to enhance this resource.
