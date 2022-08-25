## Commands to control the computer.

Name | Command 
------------ | -------------
shutdown | systemctl poweroff   
reboot | systemctl restart
suspend | systemctl suspend
hibernate | systemctl hibernate
lock screen | loginctl lock-session
unlock screen | loginctl unlock-session
turn off screen | xset dpms force off
turn on screen | xset dpms force on

## Volume control.
Name | Command 
------------ | -------------
volume down | qdbus org.kde.kglobalaccel /component/kmix invokeShortcut "decrease_volume"
volume up | qdbus org.kde.kglobalaccel /component/kmix invokeShortcut "increase_volume"
mute | qdbus org.kde.kglobalaccel /component/kmix invokeShortcut "mute"
mute microphone | qdbus org.kde.kglobalaccel /component/kmix invokeShortcut "mic_mute"

## With these commands you can control the brightness level.
Name | Command 
------------ | -------------
brightness up | qdbus org.kde.Solid.PowerManagement /org/kde/Solid/PowerManagement/Actions/BrightnessControl org.kde.Solid.PowerManagement.Actions.BrightnessControl.setBrightness $(expr $(qdbus org.kde.Solid.PowerManagement /org/kde/Solid/PowerManagement/Actions/BrightnessControl org.kde.Solid.PowerManagement.Actions.BrightnessControl.brightness) + 375)
brightness down | qdbus org.kde.Solid.PowerManagement /org/kde/Solid/PowerManagement/Actions/BrightnessControl org.kde.Solid.PowerManagement.Actions.BrightnessControl.setBrightness $(expr $(qdbus org.kde.Solid.PowerManagement /org/kde/Solid/PowerManagement/Actions/BrightnessControl org.kde.Solid.PowerManagement.Actions.BrightnessControl.brightness) - 375)

## Screenshots manipulation.
Name | Command 
------------ | -------------
screenshot | spectacle -b
screenshot to phone | file=/tmp/$(hostname)_$(date "+%Y%m%d_%H%M%S").png; spectacle -bo "${file}" && kdeconnect-cli -d $(kdeconnect-cli -a --id-only) --share ${file}
webcam to phone | file="$HOME/Pictures/WebcamImage_$(date "+%Y%m%d_%H%M%S").jpg"; ffmpeg -f video4linux2 -input_format mjpeg -s 1280x720 -i /dev/video0 -frames:v 1 "${file}" && kdeconnect-cli -d $(kdeconnect-cli -a --id-only) --share "${file}"

## Virtual Desktop manipulation.
Name | Command
------------ | -------------
VD main | qdbus org.kde.KWin /KWin setCurrentDesktop 1
VD next | qdbus org.kde.KWin /KWin nextDesktop
VD previous | qdbus org.kde.KWin /KWin previousDesktop
