## basics + python

sudo apt install libinput-tools
sudo mkdir -p /etc/libinput
sudo nano /etc/libinput/local-overrides.quirks
sudo apt update && sudo apt install python3 python3-pip

## quirck fixes

[GPD MicroPC 2 Touchpad]
MatchName=ALPS0001:00 36B6:C001 Touchpad
MatchUdevType=touchpad
MatchDMIModalias=dmi:*:svnGPD:pnG1688-08:*
AttrInputProp=-INPUT_PROP_BUTTONPAD

gsettings set org.gnome.settings-daemon.peripherals.touchscreen orientation-lock true

sudo systemctl mask --now bluetooth.service
sudo rfkill block bluetooth

## mouse & trackpad

gsettings set org.gnome.desktop.peripherals.mouse accel-profile 'flat'
gsettings set org.gnome.desktop.peripherals.touchpad accel-profile 'flat'	

## git

sudo apt install gnome-shell-extension-manager

sudo apt install git
ssh-keygen -t ed25519 -C ""
cat ~/.ssh/id_ed25519.pub