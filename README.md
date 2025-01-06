## Windows-to-Linux
The process to switch between operating systems, specifically from Windows to Linux.

A list to help me keep track of possible software alternatives to make the experience reasonable, otherwise the switch will not happen.

## Linux
- Fedora https://fedoraproject.org/
    - or Nobara? https://nobaraproject.org/
- Gnome DE https://fedoraproject.org/workstation/

## Software
I tend to use open source and FOSS software, which in the most part is available for all platforms.

- [x] Browser
    - Firefox (native) https://flathub.org/apps/org.mozilla.firefox
    - Brave (native) https://brave.com/linux/#release-channel-installation
    - Chromium (native) https://docs.fedoraproject.org/en-US/quick-docs/installing-chromium-or-google-chrome-browsers/
- [x] Google Drive (`rclone + rclone browser` or `Gnome Accounts`)
- [x] One Drive (`rclone + rclone browser` or `Gnome Accounts`)
- [x] Dropbox (native) https://www.dropbox.com/install-linux
- [x] MEGA (native) https://mega.io/desktop#download
- [ ] iCloud Drive (none, web)
- [ ] Proton Drive (none, web - [reference](https://www.reddit.com/r/ProtonDrive/comments/1e34coe/discussion_thread_for_proton_drive_on_linux_lets/))
    - Test: `Rclone` https://rclone.org/protondrive/
- [ ] Internet Download Manager [IDM] (none)
    - Specifically its browser extension integration to capture videos and download them
    - [ABDM](https://github.com/amir1376/ab-download-manager) is a close match, waiting on [feature progress](https://github.com/amir1376/ab-download-manager/issues/9), if any.
    - XDM was a possible choice, but development halted for a long time now [[reference](https://github.com/subhra74/xdm/discussions/768#discussioncomment-10842375)]
    - `yt-dlp` offers a static list, so it's not a viable alternative
    - Find possible video extractors? (ie: apps or extensions) (none so far)
- [x] Text editor, document viewer, office suit (native, many)
- [x] Media player [`mpv` + `yt-dlp` + `ffmpeg`]
    - `mpv`: https://packages.fedoraproject.org/pkgs/mpv/mpv/
    - `yt-dlp`: https://github.com/yt-dlp/yt-dlp/wiki/Installation
    - `ffmpeg`: RPM Fusion https://www.ffmpeg.org/download.html#build-linux
- [x] Image viewer (native, many, including `mpv`)
- [x] Music player [[museeks](https://github.com/martpie/museeks)] (native)
- [x] Transcoder [[Handbrake](https://github.com/HandBrake/HandBrake)] (native)
- [x] Remote desktop [[RustDesk](https://github.com/rustdesk/rustdesk)] (native)
- [x] Password manager [[KeePassXC](https://github.com/keepassxreboot/keepassxc)] (native)
- [x] Multi-factor auth [[Ente Authe](https://github.com/ente-io/ente#ente-auth)] (native)
- [x] Local share [[LocalSend](https://github.com/localsend/localsend)] (native)
- [x] Messaging
    - [SimpleXChat](https://github.com/simplex-chat/simplex-chat) (native)
    - [Telegram](https://flathub.org/apps/org.telegram.desktop) (native)
    - [Fractal](https://gitlab.gnome.org/World/fractal) [Matrix] (native)
    - [Discord](https://flathub.org/apps/com.discordapp.Discord) (native)
    - WhatsApp [eww] (Web app, through Brave or Chromium)
- [x] Equalizer [[Easy Effects](https://github.com/wwmm/easyeffects)] (native)
- [x] Screen recorder [many, [OBS Studio](https://flathub.org/apps/com.obsproject.Studio)] (native)

## Useful
- [RPM Fusion](https://rpmfusion.org/)
- [Rclone](https://rclone.org/)
- [Rclone Browser](https://github.com/kapitainsky/RcloneBrowser)
- [Bottles](https://github.com/bottlesdevs/Bottles): Run Windows software and games on Linux
- [Piper](https://github.com/libratbag/piper): GTK application to configure gaming devices
- [Solaar](https://github.com/pwr-Solaar/Solaar): Linux device manager for Logitech devices
- [Lutris](https://flathub.org/apps/net.lutris.Lutris): Lutris helps you install games from all eras and from most gaming systems
- [Heroic Games Launcher](https://github.com/Heroic-Games-Launcher/HeroicGamesLauncher): A games launcher for GOG, Amazon and Epic Games
- [Cartridges](https://flathub.org/apps/page.kramo.Cartridges): a simple game launcher for all of your games
- [Flatseal](https://flathub.org/apps/com.github.tchx84.Flatseal): A graphical utility to review and modify permissions from Flatpak apps
- XWayland Video Bridge: Utility to allow streaming Wayland windows to X applications
- [Gnome Dconf Editor](https://wiki.gnome.org/Apps(2f)DconfEditor.html)
- [Gnome Tweaks](https://gitlab.gnome.org/GNOME/gnome-tweaks)
- [Gnome Extensions Manager](https://flathub.org/apps/com.mattjakeman.ExtensionManager)
    - Reference: https://www.omgubuntu.co.uk/best-gnome-shell-extensions
- [Gnome Firmware](https://gitlab.gnome.org/World/gnome-firmware)
- [Mission Center](https://flathub.org/apps/io.missioncenter.MissionCenter): Monitor your CPU, Memory, Disk, Network and GPU usage
- [Dosage](https://flathub.org/apps/io.github.diegopvlk.Dosage): Keep track of your treatments
- [Parabolic](https://flathub.org/apps/org.nickvision.tubeconverter): A basic yt-dlp frontend
- Fedora recommendations
    - https://www.youtube.com/watch?v=dZIfjbZN0H8
    - https://www.youtube.com/watch?v=BYIDoD8VdAw

## Notes
- Nvidia Drivers: RPM Fusion => Nvidia Drivers. Might need `libnvidia-egl-wayland1`?
    - Not Gnome, but still a useful reference: https://community.kde.org/Plasma/Wayland/Nvidia
- Look into enabling non-free options (ie: `ffmpeg`), is it just using RPM Fusion or are there other steps?
   - Software Center => enable non-free/3rd party (ie: 3rd party codec packages)
