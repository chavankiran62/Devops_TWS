Management & Disk Usage Task
To check  the available block devices - lsblk   
If no extra disk is available, Create a Loopback file(Virtual Disk) 
If we see an unmounted partition (eg., /dev/xvdb), we use it for mounting. 

Orelse will create a 100MB Virtual Disk File 
sudo dd if=/dev/zero of=/mnt/virtualdisk.img bs=1M count=100 

Format It as ext4 
sudo mkfs.ext4 /mnt/virtualdisk.img 

Mount the file as a loop Device 
sudo mkdir /mnt/devops_data

Mount the file as a Loop Device 
sudo mount -o loop /mnt/virtualdisk.img /mnt/devops_data

To verify  
df –h or lsblk 
