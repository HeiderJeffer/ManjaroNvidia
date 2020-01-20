# Nvidia Manjaro

https://github.com/dglt1/optimus-switch-gdm

#And Here: 

https://forum.manjaro.org/t/manjaro-nvidia-slow-gaming-manjaro-nvidia-fast-no-gaming/112996/20

```
sudo set-intel.sh
sudo set-nvidia.sh
```
```
sudo pacman -Syyu
```
```
sudo mhwd -r pci video-linux
sudo mhwd -i pci video-nvidia-435xx
sudo rm /etc/X11/xorg.conf.d/90-mhwd.conf
sudo rm /etc/modprobe.d/mhwd-gpu.conf
sudo rm /etc/modules-load.d/mhwd-gpu.conf
sudo mhwd -r pci video-linux
sudo mhwd -i pci video-nvidia-435xx
```
```
cd ~
sudo pacman -S linux54-headers dkms acpi_call-dkms xf86-video-intel xorg-xrandr git
git clone https://github.com/dglt1/optimus-switch-gdm.git
cd ~/optimus-switch-gdm
chmod +x install.sh
sudo ./install.sh
```

dont reboot yet, post these and i'll let you know if everything looks good
```
mhwd -li
ls -laR /etc/X11 ; cat /etc/X11/xorg.conf.d/*.conf
ls -la /etc/modprobe.d ; cat /etc/modprobe.d/*.conf
ls -la /etc/modules-load.d ; cat /etc/modules-load.d/*.conf
```
# Switch Nvidia / Intel
```
sudo set-intel.sh
sudo set-nvidia.sh
```
