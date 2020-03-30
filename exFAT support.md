apt-get update
sudo apt-get upgrade
sudo apt-get install exfat-fuse
sudo apt-get install exfat-utils
sudo mkdir /media/exfat
sudo mount -t exfat /dev/sdb1 /media/exfat
sudo blkid /// find the UUID
sudo nano /etc/fstab
UUID=CA1C-06BC /media/exfat exfat defaults,auto,umask=000,users,rw 0 0
mkfs.exfat /dev/sdb1
