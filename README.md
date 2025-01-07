## Windows-to-Linux
A list to help me keep track of possible software alternatives to make the experience reasonable, otherwise the switch will not happen.

I'm not well versed in Linux, so all the information I have is by doing research and comparing results. So errors, bad choices and mistakes are possible.

The goal is to try and plan the best route before making the switch, to not hop back and forth between operating systems.

## Linux
- Fedora https://fedoraproject.org/
  - or Nobara? https://nobaraproject.org/
- Gnome DE

## Process
I tend to use open source and FOSS software a lot, which in the most part is available for many platforms or an alternative exists already.

#### Setbacks (cons)
- Forced ecosystems that don't exist on Linux or yet to be found. (ie: iCloud Drive, WhatsApp, IDM...etc)
- Cloud: `Rclone` is a huge learning curve, even with a frontend like `Rclone Browser`
  - Gaining sync (local storage) access with my cloud services would definitely be an annoying chore
  - Affects `Proton Drive`, `Google Drive` and `Microsoft OneDrive`
- Flatpaks are sandboxed by default, which can result in mis-matched themes, no access to folders and such
  - Use `dnf`/`rpm` for installing a package if available and maintained, otherwise, use verified Flatpaks
  - Use `Flatseal` to resolve sandboxed issues, if any
  - As far as I can tell, sometimes the name of the related environment variables are needed, which is a chore, since I'll have to research them when needed

## Software
- [x] Browser
  - Firefox (native) [`dnf`/`rpm`]
  - Brave (native) https://brave.com/linux/#release-channel-installation
  - Chromium (native) [`dnf`/`rpm`]
- [ ] Google Drive ([setback](#setbacks-cons))
  - `Rclone`: https://rclone.org/drive/
  - `Gnome Accounts`: Online use only
- [ ] One Drive ([setback](#setbacks-cons))
  - `Rclone`: https://rclone.org/onedrive/
  - `Gnome Accounts`: Online use only, Gnome 46+
- [ ] iCloud Drive (none, web)
- [ ] Proton Drive (none, web) [[reference](https://www.reddit.com/r/ProtonDrive/comments/1e34coe/discussion_thread_for_proton_drive_on_linux_lets/)] ([setback](#setbacks-cons))
  - Test: `Rclone` https://rclone.org/protondrive/
- [x] Dropbox (native) https://www.dropbox.com/install-linux
- [x] MEGA (native) https://mega.io/desktop#download
- [ ] Internet Download Manager [IDM] (none)
  - Specifically its browser extension integration to capture videos and download them
  - Why this QoL is needed for me: [reference](https://github.com/amir1376/ab-download-manager/issues/9#issuecomment-2470097235)
  - [ABDM](https://github.com/amir1376/ab-download-manager) is a close match, waiting on [feature progress](https://github.com/amir1376/ab-download-manager/issues/9), if any
  - XDM was a possible choice, but development halted for a long time now [[reference](https://github.com/subhra74/xdm/discussions/768#discussioncomment-10842375)]
  - `yt-dlp` offers a static list, so it's not a viable alternative
  - Find possible video extractors? (ie: apps or extensions) [incomplete]
    - [hls-downloader](https://github.com/puemos/hls-downloader): Web Extension for sniffing and downloading HTTP Live streams (HLS)
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
- [Rclone Browser](https://github.com/kapitainsky/RcloneBrowser): A simple cross platform GUI for Rclone
- [Bottles](https://github.com/bottlesdevs/Bottles): Run Windows software and games on Linux
- [Piper](https://github.com/libratbag/piper): GTK application to configure gaming devices
- [Solaar](https://github.com/pwr-Solaar/Solaar): Linux device manager for Logitech devices
- [Flatseal](https://flathub.org/apps/com.github.tchx84.Flatseal): A graphical utility to review and modify permissions from Flatpak apps
- [Mission Center](https://flathub.org/apps/io.missioncenter.MissionCenter): Monitor your CPU, Memory, Disk, Network and GPU usage
- [Parabolic](https://flathub.org/apps/org.nickvision.tubeconverter): A basic `yt-dlp` frontend
- [Lutris](https://flathub.org/apps/net.lutris.Lutris): Lutris helps you install games from all eras and from most gaming systems
- [Heroic Games Launcher](https://github.com/Heroic-Games-Launcher/HeroicGamesLauncher): A games launcher for GOG, Amazon and Epic Games
- [Cartridges](https://flathub.org/apps/page.kramo.Cartridges): A simple game launcher for all of your games
- [Dosage](https://flathub.org/apps/io.github.diegopvlk.Dosage): Keep track of your treatments
- [Gnome Dconf Editor](https://wiki.gnome.org/Apps(2f)DconfEditor.html): A viewer and editor of applications internal settings
- [Gnome Tweaks](https://gitlab.gnome.org/GNOME/gnome-tweaks): Customize Gnome DE
- [Gnome Extensions Manager](https://flathub.org/apps/com.mattjakeman.ExtensionManager): A utility for browsing and installing GNOME Shell Extensions
  - Reference: https://www.omgubuntu.co.uk/best-gnome-shell-extensions
- [Gnome Firmware](https://gitlab.gnome.org/World/gnome-firmware): Manage firmware on devices supported by `fwupd`
- [RPM Fusion](https://rpmfusion.org/): Provides software that the Fedora Project doesn't want to ship
- XWayland Video Bridge: Utility to allow streaming Wayland windows to X applications
  - As far as I can tell, this isn't needed anymore (ie: Discord screen share), need to verify
- Fedora recommendations
  - https://www.youtube.com/watch?v=dZIfjbZN0H8
  - https://www.youtube.com/watch?v=BYIDoD8VdAw

## Notes
- Nvidia Drivers: RPM Fusion => Nvidia Drivers
  - Might need `libnvidia-egl-wayland1`?
  - Useful reference: https://community.kde.org/Plasma/Wayland/Nvidia
- Look into enabling non-free options (ie: `ffmpeg`), is it just using RPM Fusion or are there other steps?
  - Software Center => enable `non-free` (ie: 3rd party codec packages)
