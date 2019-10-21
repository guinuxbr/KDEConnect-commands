## Commands to control the computer.
Shutdown:<br>
```systemctl poweroff```
    
Reboot:<br>
```systemctl restart```

Suspend:<br>
```systemctl suspend```

Hibernate:<br>
```systemctl hibernate```

Lock screen:<br>
```loginctl lock-session```

Unlock screen:<br>
```loginctl unlock-session```

Turn off screen:<br>
```xset dpms force off```

Turn on screen:<br>
```xset dpms force on```

Lock keyboard and mouse (not the screen):<br>
```pyxtrlock```

Unlock keyboard and mouse:<br>
```pkill pyxtrlock```

## Volume control.
If you are running Plasma
Volume down:<br>
```qdbus org.kde.kglobalaccel /component/kmix invokeShortcut "decrease_volume"```

Volume up:<br>
```qdbus org.kde.kglobalaccel /component/kmix invokeShortcut "increase_volume"```

Mute:<br>
```qdbus org.kde.kglobalaccel /component/kmix invokeShortcut "mute"```

Mute microphone:<br>
```qdbus org.kde.kglobalaccel /component/kmix invokeShortcut "mic_mute"```

## With these commands you can control the brightness level.
Brightness Up:<br>
```qdbus org.kde.Solid.PowerManagement /org/kde/Solid/PowerManagement/Actions/BrightnessControl org.kde.Solid.PowerManagement.Actions.BrightnessControl.setBrightness $(expr $(qdbus org.kde.Solid.PowerManagement /org/kde/Solid/PowerManagement/Actions/BrightnessControl org.kde.Solid.PowerManagement.Actions.BrightnessControl.brightness) + 375)```

Brightness Down:<br>
```qdbus org.kde.Solid.PowerManagement /org/kde/Solid/PowerManagement/Actions/BrightnessControl org.kde.Solid.PowerManagement.Actions.BrightnessControl.setBrightness $(expr $(qdbus org.kde.Solid.PowerManagement /org/kde/Solid/PowerManagement/Actions/BrightnessControl org.kde.Solid.PowerManagement.Actions.BrightnessControl.brightness) - 375)```

## Screenshots manipulation.
Use this to take a screenshot and save it in your phone:<br>
```spectacle -b```

Use this to take a screenshot and send it to your phone:<br>
```file=/tmp/$(hostname)_$(date "+%Y%m%d_%H%M%S").png; spectacle -bo "${file}" && kdeconnect-cli -d $(kdeconnect-cli -a --id-only) --share ${file}```

Take webcam photo, save it in ~/Images, and send it to the phone:<br>
```file="$HOME/Images/WebcamImage_$(date "+%Y%m%d_%H%M%S").jpg"; ffmpeg -f video4linux2 -s 1280x720 -i /dev/video0 -ss 0:0:2 -frames 1 "${file}" && kdeconnect-cli -d $(kdeconnect-cli -a --id-only) --share "${file}"```