# Born2BeRootGUIDE42lisboa
Guide to Born2BeRoot for 42lisboa WITHOUT BONUSSSS!!!

In this project you will have to create a password with specific rules I recommend to use the same password as everything try "42.HelloWorld"

Linux (cluster 2) guide for debian

1 -  https://cdimage.debian.org/debian-cd/current/amd64/iso-cd/   -  debian-11.6.0-amd64-netinst.iso
2 - open oracle virtualbox - click NEW - 
3 - name: Born2beroot; Folder: sgoinfre or goinfre; type: debian version 64bits
4 - Memory Size as 1024 MB ;  Create a Virtual Hard Disk Now; VDI (VirtualBox Disk Image)
5 - STORAGE: i put fixed size (but i believe you can put dynamic a lot of colleagues did and was fine
6 - Set Size as 8 GB and then click Continue
7 - Click settings in debian, then storage, Optical Drive  disc symbol you click Choose a disk file... and go find the file you downloaded in step 1 and select it. click OK.

Installing the VM:
1 - click on arrow start, use the arrows to select "install" (dont install graphic!!)
2 - Select the following in order - 1 English - 2 other europe portugal - 3 American English 
3 - Host Name needs to be your school login + 42 at the end   (Username42)
4 - Domain name: leave empty, Password for the Host Name use something similar to what i recommended above
5 - User: write user name of the school without 42, Full name I left blank
6 - Create a Password for the User Name (you might as well use the same password as your Host Password)
7 - Timezone: central (any is fine)

8 - Partition disks: select  Guided - use entire disk and set up encrypted LVM + select CSI...
9 - Select Separate /home, /var, and /tmp paritions , then Select Yes for the LVM question.
10 - Create a Encryption passphrase - same as password
11 - amount of volume group to use for guided partitioning. - write "max", then select Finish partitioning and write changes to disk
12 - Partition Disks: click yes, Configure the package manager: select no. 
13 - enter in the country Portugal - Archive mirror : enter on deb.debian.org. (Standart) - HTTP Proxy leave Empty
14 - Participate in Survey? No / Next in software selection we select with space bar the options  SSH server and standard system utilities and then press enter on Continue.
15 -  Install the GRUB boot loader on a hard disk : yes, then /dev/sda  + continue


Starting the VM and setting up everything needed for the project:
Open you VM in the green arrow; Enter your encryption password, then login in as you shoocl username + password again 

*Creating SUDO and adding our user

1 - type su - (login as root user)
2 - type apt-get update -y            type apt-get upgrade -y           type apt install sudo
3 - type usermod -aG sudo username to add user in the sudo group         type getent group sudo  (check if user is in sudo group)

*Creating sudo.log

1 - type cd ~/../    then cd ..
2 - type cd var/log           type cd sudo          type touch sudo.log
3 - type cd ~/../  then cd .. to go back

*Configuring Sudoers Group



*Creating a New Group and adding our user

1 - type sudo groupadd user42
2 - type sudo adduser username user42                       getent group user42    (check)
