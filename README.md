# Updated Xpad Linux Kernel Driver

This driver allows you to use the Thrustmaster 458 Spider wheel with linux

# Installing

```
sudo git clone https://github.com/capure/xpad.git /usr/src/xpad-0.5
sudo dkms install --force -m xpad -v 0.5
sudo modprobe -r xpad
sudo modprobe xpad
```

# Updating

```
cd /usr/src/xpad-0.5
sudo git fetch
sudo git checkout origin/main
sudo dkms remove -m xpad -v 0.5 --all
sudo dkms install --force -m xpad -v 0.5
sudo modprobe -r xpad
sudo modprobe xpad
```

# Removing

```
sudo dkms remove -m xpad -v 0.5 --all
sudo rm -rf /usr/src/xpad-0.5
```

# Credits

Repository this is based on [xpad](https://github.com/paroj/xpad)

Original driver [xpad](https://github.com/torvalds/linux/blob/master/drivers/input/joystick/xpad.c)

# License

This project inherits the license of the original xpad driver, which is GPLv2.
