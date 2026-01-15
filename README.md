# Google_Technical-Support-Fundamentals
Google Certification Notes

# Intro to IT

## Basics  
- Career Identity: Stengths, Motivation, Values
- Strengths: Logical Perspective / Analytical Thinking / Probabilistic Approach  
- Motivation: Helping others
- Values: Responsibility, Efficiency, Optimization

## Hardware
### How to overclock a CPU safely
As an IT Support professional, you may be asked to overclock a CPU. There are steps you should follow to do this as safely as possible. Always make sure that the requestor understands the risks of overclocking before agreeing to perform this procedure. 

Check if overclocking is supported: First, make sure the CPU is a model that is unlocked for overclocking. Not all CPUs can support overclocking, including most laptop CPUs. Check the CPU manufacturer’s documentation to determine if overclocking is possible for the CPU model. Both Intel and AMD provide overclocking guides and tools for supported CPU models (see below for links to these guides). Additionally, check the documentation for the computer’s motherboard model to ensure that it can support an overclocked CPU.

Clean the inside of the computer: Turn off and unplug the computer. While wearing an anti-static wristband, open the computer and use compressed air to remove any dust build-up that has accumulated. It is especially important to remove any dust from around the CPU, fans, and intake vents.

Ensure an appropriate CPU cooler is installed (critical): If the computer has a stock CPU cooler, it is most likely insufficient for cooling an overclocked CPU. Replace the stock CPU cooler with an advanced cooling system, like a liquid cooling system.

Follow the manufacturer’s instructions for overclocking the CPU: Using the detailed instructions from the manufacturer (see below for links to Intel and AMD’s guides): 

Use benchmarking software to establish a baseline for the normal performance of the computer.

Set each CPU core multiplier to the value of the lowest multiplier using either the manufacturer’s overclocking software (recommended) or the BIOS. Then reboot the computer. 

Increase each CPU core multiplier by 1 to increase the CPU frequency. 

Test each increase for stability using the testing utility provided by the manufacturer. 

Fix any problems flagged by the testing tools, especially temperature alerts. If the system becomes too unstable, roll back to the last frequency that produced a stable performance and stop overclocking the CPU.

If the voltage appears to become insufficient to support the new frequency, increase the voltage by 0.05V. Do not increase the voltage above 1.4V without specialized cooling hardware.

If the computer freezes or crashes, it has either become completely unstable or the CPU is not getting enough voltage to support the overclocked frequency. Use the BIOS to return to the last stable frequency or increase the voltage in 0.01V increments until stable.

If stable, reboot the computer before attempting the next increase. 

# File Permissions CLI Windows
ICACLS C:\Users\Qwiklab\Documents\important_document - View existing permissions  
ICACLS C:\Users\Qwiklab\Documents\important_document /grant "Kara:(r)" - Grant Read  
ICACLS C:\Users\Qwiklab\Documents\important_document /remove "Kara" - Remove all  
# Linux Commands  
cd ../qwiklab/documents  
ls -l important_document  
sudo chmod 700 important_document - change the permissions of "important_document" (from the previous step) so that the owner has execute permissions on top of their current permissions. To do this, you'll use the chmod command, with the argument 700. The two zeros keep everyone, but the owner, from having any permissions at all, and the seven grants all available permissions to the owner (including execute). Keep in mind that because the file is owned by "root" you'll need to use sudo:  
sudo chmod u+x secret_folder/ - To add execute to the owner's permission, you can use the command below. (Note that "u" stands for "user" and "x" stands for "execute".)  
sudo chmod o-r secret_folder/ - Finally, you can remove read permissions from everyone else using the command below ("o" stands for "other"):  
sudo chmod g+w secret_folder/ - These can be done in either order; "g" stands for "group" (like "u" from before), and "w" and "r" stand for "write" and "read" respectively:  
sudo chmod g-r secret_folder/ - These can be done in either order; "g" stands for "group" (like "u" from before), and "w" and "r" stand for "write" and "read" respectively:  
ls -ld taco/ - view permissions  
sudo chown cook /home/qwiklab/taco - make cook owner  
sudo chmod u+x not_so_important_document , sudo chmod g+w not_so_important_document, - use chmod to change the permissions so that these criteria are met: The owner has all permissions ,, The group has read and write permissions. , Everyone has read permissions.  
sudo chmod a+r not_so_important_document - give everyone else read permissions. You can use the "o+r" argument to add read permissions to people other than the owner or group, but you can also use "a+r". This adds read permission to everyone (owner, group, and other)  
sudo chmod a+rwx public_document - For this file, you want everyone (owner, group, and anyone else) to have all permissions. You can add read, write, and execute permissions to everyone at once using this command:  

$ ls /dev - Lists all devices in the /dev folder 

$ lcpci - Lists devices installed on the PCI bus 

$ lsusb - Lists devices installed on the USB bus

$ lsscsi - Lists SCSI devices, such as hard drives

$ lpstat -p - Lists all printers and whether they are enabled

$ dmesg - Lists devices recognized by the kernel  


## Linux Commands
ls /var/log - View logs  
sudo cat /var/log/syslog - sys logs  
sudo du -a /home | sort -n -r | head -n 5 - top 5 largest files  
sudo apt-get update  - update list  
sudo apt-get upgrade  - upgrade apps  
sudo apt install vlc - installs vlc  
ps aux | grep totally - finds process with name totally  
sudo kill [pid]  - kills process id #pid  
sudo find / -iname "*super*"  - search for file directory containing username super  
chmod 777 [file_name] - grant read write execution permissions for file  
