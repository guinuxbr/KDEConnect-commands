# KDE Connect Commands 📱💻

![GitHub repo size](https://img.shields.io/github/repo-size/guinuxbr/KDEConnect-commands)
![GitHub contributors](https://img.shields.io/github/contributors/guinuxbr/KDEConnect-commands)
![GitHub stars](https://img.shields.io/github/stars/guinuxbr/KDEConnect-commands)
![GitHub forks](https://img.shields.io/github/forks/guinuxbr/KDEConnect-commands)
[![X Follow](https://img.shields.io/badge/X-@guinuxbr-000000?style=flat&logo=x&logoColor=white)](https://x.com/guinuxbr)

A curated collection of useful custom commands for [KDE Connect](https://community.kde.org/KDEConnect) that allow you
to control your Plasma Desktop environment directly from your smartphone.

---

## ✨ Features

- ⚡ **System Control**: Shutdown, reboot, suspend, hibernate, lock/unlock sessions, and display power toggling.
- 🔊 **Audio & Media Control**: Manage master volume, mute audio, and mute microphone via `qdbus`.
- ☀️ **Brightness Control**: Smoothly adjust display brightness levels with power management shortcuts.
- 📸 **Screenshots & Media Transfer**: Capture screenshots or webcam photos and send them directly to your phone.
- 🖥️ **Virtual Desktop Switching**: Navigate and switch between Plasma virtual desktops on the fly.
- 🎨 **Plasma Look & Feel**: Toggle dynamically between Breeze Light and Breeze Dark themes.
- 📲 **System Output to Phone**: Send live command outputs (speedtest summaries, uptime, logged users) to your phone.

---

## 📋 Available Commands

See the full list with executable command snippets in [commands.md](commands.md).

| Category | Description | Sample Actions |
|:---|:---|:---|
| **System** | Power & session management | Lock, Suspend, Reboot, Power off, Screen on/off |
| **Volume** | Audio & microphone control | Volume up/down, Mute audio, Mute mic |
| **Brightness** | Display brightness control | Step brightness up/down via Solid PowerManagement |
| **Screenshots & Media** | Camera snapshot & screenshots | Take screenshot or webcam photo & share to phone |
| **Virtual Desktops** | Workspace navigation | Switch to Main, Next, or Previous desktop |
| **Look & Feel** | Desktop theme switcher | Switch between Breeze Light and Breeze Dark |
| **System Info** | Send terminal output via ping | Speedtest summary, Uptime, Logged users |

---

## 📦 Prerequisites & Installation

To use these commands, you need KDE Connect installed on both your Linux desktop and your mobile device.

### 1. Mobile App

Install the KDE Connect app on your mobile phone:

- **[Google Play Store](https://play.google.com/store/apps/details?id=org.kde.kdeconnect_tp)**
- **[F-Droid](https://f-droid.org/packages/org.kde.kdeconnect_tp/)**

### 2. Desktop Package

Install `kdeconnect` on your Linux distribution (example for Arch Linux):

```bash
sudo pacman -S kdeconnect
```

### 3. Optional Dependencies (Arch Linux)

Install optional packages depending on the features you plan to use:

- **`sshfs`**: remote file system browsing
- **`kde-cli-tools`**: configuration UI
- **`qt5-declarative`**: QML bindings
- **`python-nautilus`**: Nautilus file manager integration

---

## 🚀 How to Use

1. Open KDE **System Settings** > **KDE Connect**.
2. Select your paired device from the list and choose **Run commands**.
3. Click **Add Command**, provide a descriptive name, and paste the desired command line from
   [commands.md](commands.md).
4. Click **Apply** / **OK** to save.
5. Open the KDE Connect app on your phone, navigate to the **Run Commands** plugin, and tap your command to execute it!

For more details on KDE Connect plugins, visit the [KDE Community Wiki](https://community.kde.org/KDEConnect).

---

## 🤝 Contributing

1. Fork this repository.
2. Create a feature branch: `git checkout -b feature/awesome-feature`
3. Commit your changes: `git commit -m 'Add awesome feature'`
4. Push to branch: `git push origin feature/awesome-feature`
5. Open a Pull Request.

---

## 👤 Maintainer

- **Guilherme Marques** ([@guinuxbr](https://github.com/guinuxbr)) — [guinuxbr.com](https://guinuxbr.com)

---

## 👥 Contributors

Special thanks to all contributors who have submitted commands and improvements!

Browse the list of [contributors](https://github.com/guinuxbr/KDEConnect-commands/graphs/contributors).

---

## 📜 Licence

This project is licensed under the [GNU GPLv3 License](https://www.gnu.org/licenses/gpl-3.0.html).
