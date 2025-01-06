## Windows-to-Linux
The process to switch between operating systems, specifically from Windows to Linux.

A list to help me keep track of possible software alternatives to make the experience reasonable, otherwise the switch will not happen.

## Linux
- Fedora https://fedoraproject.org/
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
- [x] Remote desktop [[Rustdesk](https://github.com/rustdesk/rustdesk)] (native)
- [x] Password manager [[KeePassXC](https://github.com/keepassxreboot/keepassxc)] (native)
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
- [Gnome Dconf Editor](https://wiki.gnome.org/Apps(2f)DconfEditor.html)
- [Gnome Tweaks](https://gitlab.gnome.org/GNOME/gnome-tweaks)
- [Gnome Extensions Manager](https://flathub.org/apps/com.mattjakeman.ExtensionManager)
    - Reference: https://www.omgubuntu.co.uk/best-gnome-shell-extensions
- Fedora recommendations: https://www.youtube.com/watch?v=dZIfjbZN0H8

## Notes
- Nvidia Drivers: RPM Fusion => Nvidia Drivers. Might need `libnvidia-egl-wayland1`?
    - Not Gnome, but still a useful reference: https://community.kde.org/Plasma/Wayland/Nvidia
- Look into enabling non-free options (ie: `ffmpeg`), is it just using RPM Fusion or are there other steps?
