# Command Log - DevOps Internship Task 1
## Linux Environment Setup & Exploration (Ubuntu via Vagrant)

## This document contains the Linux commands practiced during Task 1 along with sample outputs.

---

## 1) Vagrant VM Setup & Login

### Start the VM

vagrant up


### SSH into the VM

vagrant ssh


### Check current user

whoami

Output:

vagrant


### Check hostname

hostname

Output:

ubuntu-jammy


### Check OS / kernel details

uname -a

Output (example):

Linux ubuntu-jammy 5.15.0-164-generic #174-Ubuntu SMP Fri Nov 14 20:25:16 UTC 2025 x86_64 x86_64 x86_64 GNU/Linux


---

## 2) Directory Navigation & Exploration

### Print current directory

pwd

Output (example):

/home/vagrant


### List files and folders

ls


### List with hidden files + permissions

ls -la


### Move to root directory

cd /
pwd

Output:

/


### Move to home directory

cd ~
pwd

Output:

/home/vagrant


### Move one directory back

cd ..
pwd


---

## 3) Create Directories & Files

### Create a working folder for Task 1

mkdir devops-task1


### Move into the folder

cd devops-task1
pwd

Output:

/home/vagrant/devops-task1


### Create subfolders

mkdir logs scripts backup


### Create files

touch notes.txt test1.txt test2.txt


### Verify creation

ls -l


---

## 4) View and Edit Files

### Write text into a file (overwrite)

echo "DevOps Internship Task 1 - Linux Exploration" > notes.txt


### Append more text

echo "Practiced basic Linux commands and monitoring tools." >> notes.txt


### View file content

cat notes.txt


### View file using pager

less notes.txt


### Edit using nano editor

nano notes.txt


> (Alternatively, vim can be used)

vim notes.txt


---

## 5) Delete Files & Directories Safely

### Remove a file

rm test2.txt


### Remove an empty directory

rmdir backup


### Remove a directory recursively (if not empty)

rm -r logs


### Verify remaining files

ls -la


---

## 6) File Permissions & Ownership

### Check file permissions

ls -l


### Change permissions (read/write for owner, read-only for others)

chmod 644 notes.txt


### Change permissions (only owner can read/write)

chmod 600 notes.txt


### Make a directory executable (enterable)

chmod 755 scripts


### Verify updated permissions

ls -l


### Change ownership (if needed)

sudo chown vagrant:vagrant notes.txt


> Note: `chown` requires sudo/root permissions.

---

## 7) System Monitoring & Resource Checks

### Check running processes and CPU/memory usage

top


### Install and use htop (if not already installed)

sudo apt update
sudo apt install -y htop
htop


### Check disk usage

df -h

Output:

Filesystem      Size  Used Avail Use% Mounted on
/dev/sda1        40G  5.2G   33G  14% /


### Check memory usage

free -m

Output:

              total        used        free      shared  buff/cache   available
Mem:           1990         300        1200          10         490        1500
Swap:             0           0           0


### Check system uptime and load average

uptime


---

## 8) Extra Helpful Commands (Optional)

### Check current date/time

date


### Check IP address

ip a


### Check Linux version details

cat /etc/os-release


---

## Task 1 Completion Notes
- Linux environment successfully set up using Ubuntu VM via Vagrant.
- Practiced navigation, file operations, permissions, and monitoring commands.
- Screenshots are included in the Task 1 documentation file (Word/PDF).
