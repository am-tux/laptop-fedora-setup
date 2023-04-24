# Role Name

Enable Fedora to connect to airpods

# Psuedo code

dnf install bluez\*
modprobe btusb
systemctl restart bluetooth
vim /etc/bluetooth/main.conf & switch ControllerMode to bredr
systemctl restart bluetooth
