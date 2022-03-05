        _            _             _    _        _   
       / /\         / /\      _   / /\ /\ \     /\_\ 
      / /  \       / / /    / /\ / /  \\ \ \   / / / 
     / / /\ \__   / / /    / / // / /\ \\ \ \_/ / /  
    / / /\ \___\ / / /_   / / // / /\ \ \\ \___/ /   
    \ \ \ \/___// /_//_/\/ / // / /  \ \ \\ \ \_/    
     \ \ \     / _______/\/ // / /___/ /\ \\ \ \     
 _    \ \ \   / /  \____\  // / /_____/ /\ \\ \ \    
/_/\__/ / /  /_/ /\ \ /\ \// /_________/\ \ \\ \ \   
\ \/___/ /   \_\//_/ /_/ // / /_       __\ \_\\ \_\  
 \_____\/        \_\/\_\/ \_\___\     /____/_/ \/_/  BY JIJTECH
 
 * Pre-install
 * Install
 * Gesture setup
 * Final info

###################################################################
## 𝙋𝙍𝙀-𝙄𝙉𝙎𝙏𝘼𝙇𝙇                                                 
###################################################################
Dependencies:
+-----------------------------------------------------------------+
sway waybar azote python3 pavucontrol rofi nautilus rxvt-unicode
wmctrl xdotool pavucontrol swaylock light playerctl bpytop

+-----------------------------------------------------------------+
SOFT DEPENDENCIES(OPTOINIAL):
brave-browser 
microsoft-edge 
spotify


###################################################################
## 𝙄𝙉𝙎𝙏𝘼𝙇𝙇 𝙂𝙐𝙄𝘿𝙀
###################################################################
(Im planning a install script for my dots in the furture)

Add user to inputgroup:
+---------------------------------+
| $ sudo gpasswd -a $USER input   |
+---------------------------------+
start playerctld:
+----------------------+
| $ playerctld daemon  |
+----------------------+

## 𝘚𝘌𝘛 𝘗𝘖𝘓𝘒𝘐𝘛 𝘙𝘜𝘓𝘌 𝘍𝘖𝘙 𝘞𝘐𝘍𝘐 𝘊𝘖𝘕𝘛𝘙𝘖𝘓 ##

(this is needed to scan for networks)
Move '50-org.freedesktop.NetworkManager.rules' into polkit rule set:
+------------------------------------------------------------------------+
|$ sudo mv 50-org.freedesktop.NetworkManager.rules /etc/polkit-1/rules.d/|
+------------------------------------------------------------------------+


## 𝘔𝘖𝘝𝘌 𝘛𝘏𝘌 𝘋𝘖𝘛𝘚  ##

Move all the "./*" folders such as ".fonts", ".wall" to $HOME.
Move 'libinput-gestures.conf', '.Xdefaults', "prettier/" "rofi/" "sway/" "waybar/" to ~/.config
extract the fonts within ~/.fonts
allow the media module to run:
+---------------------------------------------------------+
|$ chmod +x ~/.config/waybar/custom_modules/mediaplayer.py|
+---------------------------------------------------------+


###################################################################
## 𝙂𝙀𝙎𝙏𝙐𝙍𝙀 𝙎𝙀𝙏𝙐𝙋
###################################################################
THE GESTURE SUPPORT IS NOT MAINTAINED BY JIJTECH.
DOTS CONTAINS A CONF FILE FOR SWAY AND IS INSTALLED BY THE SCRIPT!

LIBINPUT-GEASTURES FOR WM(NON-DE) - SYSTEMD INSTALL:
+-----------------------------------------------------------------+
|$ git clone https://github.com/bulletmark/libinput-gestures.git  |
+-----------------------------------------------------------------+

+---------------------- +
|$ cd libinput-gestures |
+-----------------------±

install the files:
+------------------------------------------±
| $ sudo ./libinput-gestures-setup install |
+------------------------------------------+

create systemd symlink:
+---------------------------------+
|$ libinput-gestures-setup service|
+---------------------------------+

Autostart on login:
+-----------------------------------+ 
|$ libinput-gestures-setup autostart|
+-----------------------------------+

### 𝙁𝙄𝙉𝘼𝙇 𝙄𝙉𝙁𝙊 ###################################################

 'MOD + SPACE' Shows the "Shortcut Overview"

 
###  𝘋𝘖𝘛 𝘚𝘛𝘙𝘜𝘊𝘛𝘜𝘙𝘌 𝘖𝘝𝘌𝘙𝘝𝘐𝘌𝘞  ###

/*
├─── $HOME/
│   ├──── .wall/*
│   ├──── .fonts/
│   │      └─ ProFont/*
│   └──── .config/
│         ├── '.libinput-gestures-is-service'
│         ├── 'libinput-gestures.conf'
│         ├── prettier
│         │   └── prettier.json
│         ├── rofi
│         │   └── config
│         ├── sway
│         │   ├── config
│         │   ├── import-gsettings
│         │   ├── nm-rofi
│         │   └── sway-shortcuts.conf
│         └── waybar
│             ├── 'config'
│             ├── custom_modlues/
│             │   └── mediaplayer.py
│             └── 'style.css'
└──── /etc/polkit-1/rules.d/
                    └─── 50-org.freedesktop.NetworkManager.rules
