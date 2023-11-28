# YTcrackerhacker-.i
arch linx install document

installed arch Linux iso created a virtual machine with 20gb of storage and 2gb of ram  

inserted the firmware = UEFI into the vm 

Enable network time synchronization using timedatectl by running the following command: timedatectl set-ntp true

partition the drives using the fdisk command made a 500mb boot drive and used the remaining storage to make the rest of the partion 

changed the file system to exfat using the mkfs.ext4 /dev/sda command 

mounted the disk using mount /dev/sda /mnt

installed the essential packages using pacstrap /mnt base linux linux-firmware

created the fstab file using  genfstab -U /mnt >> /mnt/etc/fstab

set time zone using ln -sf /usr/share/zoneinfo/America/New_York /etc/localtime

generate locals locale-gen

created root password passwd command 

installed boot loader using pacman -Sy grub

installed drivers using 
command pacman -S networkmanager 
command systemctl enable NetworkManager 

created user accounts useradd -m username

added them to the sudo group using usermod -aG wheel,video,audio username

install the `grub` package using pacman. pacman -S grub

additional packages required for the bootloader to work properly. pacman -S efibootmgr dosfstools os-prober mtools

Mount your EFI partition ( `/dev/sda1` ) to the `/boot/EFI` directory. mkdir /boot/EFI
mount /dev/sda1 /boot/EFI

run the `grub-install` script to install the bootloader in the EFI directory. grub-install --target=x86_64-efi --efi-directory=/boot/EFI --bootloader-id=grub

Generate a GRUB configuration file using `grub-mkconfig` as follows:
grub-mkconfig -o /boot/grub/grub.cfg

install desktop envirment using pacman -S xorg plasma-meta kde-applications

enable the SDDM and NetworkManager services by typing:

systemctl enable sddm

systemctl enable NetworkManager

exit chroot

unmount drive using umount -R /mnt

reboot system to get to new installed os 

