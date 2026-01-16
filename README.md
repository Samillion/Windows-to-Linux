## :mag: Windows-to-Linux
A record to help me keep track of possible software alternatives and solutions to make the experience reasonable, otherwise the switch will not happen.

The goal is to try and plan the best route before making the switch, to not hop back and forth between operating systems.

I'm not well versed in Linux, so all the information I have is by doing research and comparing results. Errors, bad choices and mistakes are possible.

## :computer: System(s)
| :nut_and_bolt: | Main                                                                | Secondary                                                                                                                                    |
|----------------|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| **CPU**        | AMD Ryzen 9800X3D                                                   | Intel i7 3770K                                                                                                                               |
| **RAM**        | 32GB DDR5                                                           | 32GB DDR3                                                                                                                                    |
| **GPU**        | Nvidia RTX 5070                                                     | Nvidia GTX 660                                                                                                                               |
| **Notes**      | ✔️ Modern hardware, should work fine on distros with Wayland only. | ❌ Uses old driver that doesn't work on Wayland. Open source driver works, but tested performance on GPU makes even surfing web intolerable. |

## :penguin: Linux
<table>
  <thead>
    <tr>
      <th colspan="3">Distributions (Choose One)</th>
    </tr>
    <tr>
      <th>Name</th>
      <th>Website</th>
      <th>Note</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Debian</td>
      <td><a href="https://www.debian.org/">debian.org</a></td>
      <td>Pure Debian, requires manual configuration, most-likely cli. Outdated (stable) software, unless testing or unstable branch used</td>
    </tr>
    <tr>
      <td>Ubuntu</td>
      <td><a href="https://ubuntu.com/">ubuntu.com</a></td>
      <td>Based on Debian, user friendly experience with GUI tools for drivers and such, but mainly with commercial goals (Canonical)</td>
    </tr>
    <tr>
      <td>Mint</td>
      <td><a href="https://linuxmint.com/">linuxmint.com</a></td>
      <td>Based on Ubuntu. Main differences seem to be: Cinnamon DE focus, stability, user friendly and no Snaps</td>
    </tr>
    <tr>
      <td>Fedora</td>
      <td><a href="https://fedoraproject.org/">fedoraproject.org</a></td>
      <th>Same as Debian, as in it's not based on another distribution. Difference is that it has more frequent updates to software and packages, almost cutting edge</th>
    </tr>
    <tr>
      <td>Bazzite</td>
      <td><a href="https://bazzite.gg/">bazzite.gg</a></td>
      <th>Based on Fedora, comes pre-installed with Steam and other game focused optimizations, and has GPU specific ISOs for an easy out of box experience</th>
    </tr>
    <tr>
      <td>Nobara</td>
      <td><a href="https://nobaraproject.org/">nobaraproject.org</a></td>
      <th>Same as Bazzite. Difference is, as far as I can tell: philosphy and method</th>
    </tr>
    <tr>
      <td colspan="3">Desktop environment: Gnome or KDE</td>
    </tr>
    <tr>
      <td colspan="3"><strong>Switch status:</strong> ❌</td>
    </tr>
  </tbody>
</table>

## :black_nib: Process
I tend to use open source and FOSS software a lot, which in the most part is available for many platforms or an alternative exists already.

#### Setbacks (cons)
The following issues are not Fedora or Debian specific, they seem to be a general occurance within Linux.

It is common to suggest "just use online/web version" as a solution, but that is not effective, it's simply a forced compromise, unfortunately.

- Outdated Software:
  - Due to policy and the fact that in some cases it's about volunteer based work, some packages are outdated
  - Fedora seems to be balanced, from what I've seen it's mostly Debian based distros and indpendent package support (ie: `flatpak`, `rpm`, `apt`, `deb`), sometimes none (ie: mpv)
  - An alternative would be to build/compile packages yourself, which in itself a huge setback and a chore, from a user experience standpoint, especially ones new to Linux
- GPU Drivers:
  - I keep stumbling upon comments about GPU issues, especially when it comes to Wayland
    - Some have opted to switch back to X11, since old drivers work well on it. Though many DEs and distros are dropping XORG one after the other, for good reasons but bad for older GPUs
    - There are detailed guides. The downside is that it's a lot to take in as a user, compared to Windows' "just works". [[#notes](#memo-notes)]
  - Some other comments here and there, mostly solvable by tinkering with a config or a setting that sometimes have a label of "at your own risk". Still, a bothersome chore
- Cloud:
  - No alternative or method for `iCloud Drive`
  - `Rclone` is a huge learning curve, even with a frontend like `Rclone Browser`
    - Having auto-sync and mount (local copy) access with my cloud services would definitely be an annoying chore
    - Affects `Proton Drive`, `Google Drive` and `Microsoft OneDrive`
- Flatpaks are sandboxed by default, which can result in mis-matched themes, no access to folders and such
  - Use `dnf`/`rpm`/`apt`/`deb`/`binary` for installing a package if available and maintained officially, otherwise, use verified Flatpaks
  - Use `Flatseal` to resolve sandboxed issues, if any
    - As far as I can tell, sometimes the name of the related environment variables are needed, which is a chore, since I'll have to research them when needed
- Internet Download Manager (IDM) alternative [✔️ `solved-partially`:`listed`]
  - Specifically its browser extension integration to capture videos and download them
  - [ABDM](https://github.com/amir1376/ab-download-manager) is a close match, ~~waiting on [feature progress](https://github.com/amir1376/ab-download-manager/issues/9), if any~~
    - Feature is added, but unfortunately it does not work half the time. Needs to mature, hopefully
  - XDM was a possible choice, but development halted for a long time now [[reference](https://github.com/subhra74/xdm/discussions/768#discussioncomment-10842375)]
  - `yt-dlp` offers a static list, so it's not a viable alternative
- WhatsApp [✔️ `solved-partially`:`listed`]
  - Not really an optimal solution, just using PWA, which would make some features unavailable (ie: calls)

## :floppy_disk: Software
- [x] Browser
  - Firefox (native) https://www.firefox.com/en-US/browsers/desktop/linux/
  - Brave (native) https://brave.com/linux/#release-channel-installation
  - Chromium (native) [`dnf`/`rpm`/`apt`/`deb`]
- [ ] Google Drive [[#setback](#setbacks-cons)]
  - `Rclone`: https://rclone.org/drive/
  - `Gnome Accounts`: Online use only
- [ ] One Drive [[#setback](#setbacks-cons)]
  - `Rclone`: https://rclone.org/onedrive/
  - `Gnome Accounts`: Online use only, Gnome 46+
- [ ] iCloud Drive (none, web) [[#setback](#setbacks-cons)]
- [ ] Proton Drive (none, web) [[reference](https://www.reddit.com/r/ProtonDrive/comments/1e34coe/discussion_thread_for_proton_drive_on_linux_lets/)] [[#setback](#setbacks-cons)]
  - Test: `Rclone` https://rclone.org/protondrive/
- [x] Dropbox (native) https://www.dropbox.com/install-linux
- [x] MEGA (native) https://mega.io/desktop#download
- [x] Internet Download Manager [IDM] (alternative method)
  - Video sniffers: [✔️ having both extensions seem to provide a good enough alternative]
    - [hls-downloader](https://github.com/puemos/hls-downloader): Extension for sniffing and downloading HTTP Live streams (HLS)
    - [cat-catch](https://github.com/xifangczy/cat-catch): Extension for sniffing resources from a webpage
    - **Note:** It's not ideal nor does it work the same as IDM, but it's a compromise, better than nothing
- [x] Text editor, document viewer, office suit (native, many)
- [x] Media player [`mpv` + `yt-dlp` + `ffmpeg`]
  - `mpv`: No official packages
    - https://packages.fedoraproject.org/pkgs/mpv/mpv/ (only stable release, not git)
    - https://mpv.io/installation/
    - Hopefully one day they provide an official Flatpak to stop relying on third parties
  - `yt-dlp`: https://github.com/yt-dlp/yt-dlp/wiki/Installation
  - `ffmpeg`: https://www.ffmpeg.org/download.html#build-linux
- [x] Image viewer (native, many)
- [x] Music player (native, many)
- [x] Transcoder [[Handbrake](https://github.com/HandBrake/HandBrake)] (native)
- [x] Remote desktop [[RustDesk](https://github.com/rustdesk/rustdesk)] (native)
- [x] Password manager [[KeePassXC](https://github.com/keepassxreboot/keepassxc)] (native)
- [x] Multi-factor auth [[Ente Authe](https://github.com/ente-io/ente#ente-auth)] (native)
- [x] Local share [[LocalSend](https://github.com/localsend/localsend)] (native)
- [x] Messaging
  - [Signal](https://signal.org/download/linux/) (❌ official native for Debian based only. Why!?)
    - There is an unofficial Flatpak and some community solutions to make it work on Fedora, but, really have no idea why a secure communication software opts out of providing their own official packages
  - [Telegram](https://flathub.org/apps/org.telegram.desktop) (native)
  - [Fractal](https://gitlab.gnome.org/World/fractal) [Matrix] (native)
  - [Discord](https://flathub.org/apps/com.discordapp.Discord) (native)
  - WhatsApp (Web app, through Brave or Chromium)
    - Note: Some features might not work as a PWA, like calls and such
- [x] Equalizer [[Easy Effects](https://github.com/wwmm/easyeffects)] (native)
- [x] Screen recorder [many, [OBS Studio](https://flathub.org/apps/com.obsproject.Studio)] (native)

## :bulb: Useful
- [Bazaar](https://flathub.org/en/apps/io.github.kolunmi.Bazaar): Flatpak App store for Linux
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
  - [Refine](https://flathub.org/apps/page.tesk.Refine) seems to be a decent frontend for Dconf, a possible alternative with QoL experience
- [Gnome Tweaks](https://gitlab.gnome.org/GNOME/gnome-tweaks): Customize Gnome DE
- [Gnome Extensions Manager](https://flathub.org/apps/com.mattjakeman.ExtensionManager): A utility for browsing and installing GNOME Shell Extensions
  - Reference: https://www.omgubuntu.co.uk/best-gnome-shell-extensions
- [Gnome Firmware](https://gitlab.gnome.org/World/gnome-firmware): Manage firmware on devices supported by `fwupd`
- Extras:
  - [RPM Fusion](https://rpmfusion.org/): Provides software that the Fedora Project doesn't want to ship
  - XWayland Video Bridge: Utility to allow streaming Wayland windows to X applications
    - As far as I can tell, this isn't needed anymore (ie: Discord screen share), need to verify
  - Fedora recommendations
    - https://www.youtube.com/watch?v=dZIfjbZN0H8
    - https://www.youtube.com/watch?v=BYIDoD8VdAw

## :memo: Notes
By far the biggest setback on Linux is GPU driver. Not Linux's fault, just companies refusing to provide proper support and updates. 

It is actually easier to have older hardware work on Windows than Linux sometimes, especially with hardware like Nvidia and Broadcom. Which is sadly a big deal to people that want to migrate. Most just want things to work, easily.

The other notable issue is gaming. Many games will just not work due to how their anti-cheat methods are applied. Companies can provide patches to make it work. Hopefully, one day.

- Nvidia Drivers: [[#setback](#setbacks-cons)]
  - Might need `libnvidia-egl-wayland1`?
  - Useful reference: (fedora) https://rpmfusion.org/Howto/NVIDIA
  - Useful reference: (debian) https://wiki.debian.org/NvidiaGraphicsDrivers
  - Useful reference: https://community.kde.org/Plasma/Wayland/Nvidia
- Look into enabling non-free options (ie: `ffmpeg`):
  - Software Center => enable `non-free` (ie: 3rd party codec packages)
  - Useful reference: (fedora) https://rpmfusion.org/Howto/Multimedia
  - Useful reference: (debian) https://wiki.debian.org/DebianSoftware
