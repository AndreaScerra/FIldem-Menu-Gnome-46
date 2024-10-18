**Installation**

Clone this repository
```
git clone https://github.com/AndreaScerra/FIldem-Menu-Gnome-46.git
```


Install the dependencies, I tested everything on arch linux and
gnome 46.
```
sudo pacman -S bamf appmenu-gtk-module libkeybinder3 libdbusmenu-gtk2 libdbusmenu-gtk3 libdbusmenu-qt5 git python-pip
```
```
yay -S python-fuzzysearch         #replace with your aur helper
```

Download the file in the releases 
```
curl -L0 https://github.com/AndreaScerra/FIldem-Menu-Gnome-46/releases/download/Public/python3-fildem-0.6.7-1-x86_64.pkg.tar.zst > python3-fildem-0.6.7-1-x86_64.pkg.tar.zst
```

and install it
```
sudo pacman -U python3-fildem-0.6.7-1-x86_64.pkg.tar.zst
```

Go to the cloned repository directory and run
```
sudo python3 setup.py install --optimize=1

cp -r fildemGMenu@gonza.com ~/.local/share/gnome-shell/extensions/
```

Edit or create this file _~/.gtkrc-2.0_ and add
```
gtk-modules="appmenu-gtk-module"
```

Edit or create this file _~/.config/gtk-3.0/settings.ini_ it should look like this
```
[Settings]
another voice
gtk-modules="appmenu-gtk-module" #IMPORTANT
another voice
```

If you want to run fildem at startup create this file _~/.config/autostart/fildem.desktop_, it may be necessary to create the entire directory
```
[Desktop Entry]
Type=Application
Exec=fildem
Hidden=false
NoDisplay=false
X-GNOME-Autostart-enabled=true
Name[en_US]=Fildem
Name=Fildem
Comment[en_US]=Fildem Global Menu and HUD
Comment=Fildem Global Menu and HUD
```

Logout and Login

**Configuration**

In the extension settings disable _show menu only when the mouse is over the panel_ to make the menu always visible Mac OS style. I do not recommend it given the presence of some graphic glitches.

**Credits**

[Gonzaarcr ](https://github.com/gonzaarcr/Fildem ) for the fildem file

[Sominemo](https://github.com/Sominemo/Fildem-Gnome-45) For the updated extension
