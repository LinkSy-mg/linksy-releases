<img width="1800" height="900" alt="Download Linksy for Android and Linux. The Linux app showing a phone's page next to the Android app showing the computer." src="assets/banner.png" />

<div align="center">

  <sub>Your Android phone and your Linux computer, working as one. Files, clipboard, screens, a webcam and more, straight between your own devices. No account, no cloud, free and open source.</sub>
  <br/><br/>

<p align="center">
  <a href="#android">
    <img src="https://shieldcn.dev/github/release/LinkSy-mg/linksy-releases.svg?mode=dark&radius=999&font=geist&split=true&height=28&fontSize=13&labelColor=141821&labelTextColor=ffffff&color=1e2a4a&valueColor=ffffff&label=Android&logo=android&logoColor=22c3e6" alt="Android version"></a>
  <a href="#linux">
    <img src="https://shieldcn.dev/github/release/LinkSy-mg/linksy-desktop.svg?mode=dark&radius=999&font=geist&split=true&height=28&fontSize=13&labelColor=141821&labelTextColor=ffffff&color=1e2a4a&valueColor=ffffff&label=Linux&logo=linux&logoColor=22c3e6" alt="Linux version"></a>
  <a href="https://github.com/LinkSy-mg/linksy-releases/releases">
    <img src="https://shieldcn.dev/github/downloads/LinkSy-mg/linksy-releases.svg?mode=dark&radius=999&font=geist&split=true&height=28&fontSize=13&labelColor=141821&labelTextColor=ffffff&color=1e2a4a&valueColor=ffffff" alt="Downloads"></a>
  <br/>
  <a href="https://github.com/LinkSy-mg/linksy-desktop">
    <img src="https://shieldcn.dev/github/license/LinkSy-mg/linksy-desktop.svg?mode=dark&radius=999&font=geist&split=true&height=28&fontSize=13&labelColor=141821&labelTextColor=ffffff&color=1e2a4a&valueColor=ffffff" alt="License"></a>
  <a href="https://github.com/LinkSy-mg/linksy-releases/issues">
    <img src="https://shieldcn.dev/github/issues/LinkSy-mg/linksy-releases.svg?mode=dark&radius=999&font=geist&split=true&height=28&fontSize=13&labelColor=141821&labelTextColor=ffffff&color=1e2a4a&valueColor=ffffff" alt="Issues"></a>
  <a href="https://linksy.diary.mg">
    <img src="https://shieldcn.dev/badge/Website-linksy.diary.mg-1e2a4a.svg?mode=dark&radius=999&font=geist&split=true&height=28&fontSize=13&labelColor=141821&labelTextColor=ffffff&color=1e2a4a&valueColor=ffffff" alt="Website"></a>
</p>

**[Android](#android)** &nbsp;·&nbsp; **[Linux](#linux)** &nbsp;·&nbsp; **[What it does](#what-it-does)** &nbsp;·&nbsp; **[Screenshots](#screenshots)** &nbsp;·&nbsp; **[Privacy](#private-by-design)** &nbsp;·&nbsp; **[Help](#help)**

</div>

> [!TIP]
> Install Linksy on both devices, open it on each, and pair them once: both screens show the same code. Two Linux computers pair the same way.

---

## Install

### Android

| Download | For |
|---|---|
| **[Linksy for every phone](https://linksy.diary.mg/download/android)** | Start here. |
| [64-bit phones](https://linksy.diary.mg/download/android-arm64) | Smaller download. |
| [32-bit phones](https://linksy.diary.mg/download/android-armv7) | Smaller, for older phones. |

Always the newest version. Open the file on the phone, allow installing from your browser
once, and install. To update, install a newer one the same way.

> [!IMPORTANT]
> **If Play Protect blocks the install.** Linksy can show your phone's notifications on your
> computer, so Google Play Protect may stop it with "App blocked to protect your device". To
> install it:
> 1. Open the Play Store, tap your picture, then **Play Protect**, then the gear at the top right.
> 2. Turn off **Scan apps with Play Protect**.
> 3. Install Linksy, then turn scanning back on.
>
> Or install it from a computer with a cable: `adb install linksy.apk`.
>
> **To show notifications on your computer** (Android 13 and later): if Linksy's switch in
> Notification access is greyed out, open **App info** for Linksy, tap **⋮** at the top right,
> then **Allow restricted settings**, and turn Linksy on again. Linksy walks you through it.

### Linux

<!-- linux:start -->
Linksy **0.11.3** for x86_64. Two packages: `linksy-common` (runs in the background) and the
app for your desktop: `linksy` for GNOME and most desktops, `linksy-qt` for KDE Plasma.

**The quickest way, any distribution**

```sh
# Finds your system and desktop, asks which app (GNOME or KDE Plasma), installs it with one password
curl -fsSL https://linksy.diary.mg/install.sh | sh
```

[See what it does](https://linksy.diary.mg/install.sh). Older systems get the Flatpak. Or do it by hand:

**Fedora · GNOME and others**

```sh
# The background service, and the GTK app
curl -LO https://linksy.diary.mg/download/linksy-common-0.11.3-1.x86_64.rpm
curl -LO https://linksy.diary.mg/download/linksy-0.11.3-1.x86_64.rpm
# Install both together
sudo dnf install ./linksy-common-0.11.3-1.x86_64.rpm ./linksy-0.11.3-1.x86_64.rpm
```

**Fedora · KDE Plasma**

```sh
# The background service, and the Qt 6 app
curl -LO https://linksy.diary.mg/download/linksy-common-0.11.3-1.x86_64.rpm
curl -LO https://linksy.diary.mg/download/linksy-qt-0.11.3-1.x86_64.rpm
# Install both together
sudo dnf install ./linksy-common-0.11.3-1.x86_64.rpm ./linksy-qt-0.11.3-1.x86_64.rpm
```

> **On KDE Plasma, for the systems below too:** replace `linksy` with `linksy-qt` in the app's
> file name, for example `linksy_0.11.3_amd64.deb` becomes `linksy-qt_0.11.3_amd64.deb`, in both
> the download and the install line. `linksy-common` stays the same. The Plasma app needs
> Ubuntu 25.04 or newer.

**Ubuntu 24.04+, Linux Mint 22+, Debian 13+** (the KDE app: Ubuntu 25.04+, Debian 13+)

```sh
# The background service, and the GTK app
curl -LO https://linksy.diary.mg/download/linksy-common_0.11.3_amd64.deb
curl -LO https://linksy.diary.mg/download/linksy_0.11.3_amd64.deb
# Install both together
sudo apt install ./linksy-common_0.11.3_amd64.deb ./linksy_0.11.3_amd64.deb
```

> **Older systems** (Debian 12, Ubuntu 22.04, Linux Mint 21 and older): use
> the **Flatpak** below. It brings everything it needs (the GTK app). Install Flatpak first:
> `sudo apt install flatpak`.

**openSUSE Tumbleweed**

```sh
# The background service, and the GTK app
curl -LO https://linksy.diary.mg/download/linksy-common-0.11.3-1.suse.x86_64.rpm
curl -LO https://linksy.diary.mg/download/linksy-0.11.3-1.suse.x86_64.rpm
# Install both together (not signed yet, hence the flag)
sudo zypper install --allow-unsigned-rpm ./linksy-common-0.11.3-1.suse.x86_64.rpm ./linksy-0.11.3-1.suse.x86_64.rpm
```

**Any distribution: Flatpak**

```sh
# Everything in one file (the GTK app), installed for your user
curl -LO https://linksy.diary.mg/download/linksy-0.11.3.flatpak
flatpak install --user linksy-0.11.3.flatpak
```

**Any distribution, no root: tarball**

```sh
# The GTK app, into your home folder; uninstall.sh removes it
curl -LO https://linksy.diary.mg/download/linksy-0.11.3-linux-x86_64.tar.gz
tar xzf linksy-0.11.3-linux-x86_64.tar.gz && linksy-0.11.3-linux-x86_64/install.sh
```

Notes and checksums: [Linux 0.11.3](https://github.com/LinkSy-mg/linksy-releases/releases/tag/linux-v0.11.3).
<!-- linux:end -->

Then open **Linksy** from your apps. **Finish Setup** adds anything a feature still needs
(a codec, the webcam driver, the firewall rule), with one password.

- **Needs:** GTK app: glibc 2.39+, GTK 4.14+, libadwaita 1.5+. Plasma app: Qt 6.8+, KDE
  Frameworks 6.13+.
- **Flatpak:** does everything the packages do (it asks for access to your computer for
  this): Finish Setup adds the webcam driver and the USB cable with one password, and the
  phone's terminal opens your computer's own shell. On Sway, controlling the screen needs
  the packages.
- **Desktops:** GNOME, KDE Plasma, Xfce, Cinnamon, MATE, Openbox, i3, Hyprland, Sway, niri
  and others. On X11 desktops Linksy shares and controls the screen itself, on Hyprland and
  Sway the phone controls it through the compositor, and where no password prompt runs,
  Linksy asks for the password itself.
- **Older versions:** on the [releases page](https://github.com/LinkSy-mg/linksy-releases/releases),
  as **Android** and **Linux** releases.

> [!IMPORTANT]
> Only download Linksy from here, [linksy.diary.mg](https://linksy.diary.mg) or the AUR. A copy from anywhere else could be modified.

---

## What it does

- **Files**: any size, both ways; drop them on the window. Resumed and checked byte for byte.
- **Clipboard**: copy on one, paste on the other. Text, a screenshot or a small file.
- **Open on PC**: share a link from any phone app, it opens on the computer.
- **Webcam and microphone**: the phone's, in every app on the computer.
- **Second display**: a tablet, phone or another computer extends your desktop.
- **Screens**: see and control another device's screen.
- **Remote**: the phone as a touchpad, keyboard or slide clicker.
- **Find your phone**: ring it, even on silent, or ask where it is.
- **Lock when away**: walk off with your phone, the computer locks.
- **Terminal**: your computer's shell on the phone, behind a code you set.
- **Away from home**: files, clipboard, links and Ring over the internet, for a week after
  your devices last met.
- **Wi-Fi or USB cable**: whichever is there.

---

## Screenshots

<p align="center">
  <img src="screenshots/phone-home-dark.png" width="150" alt="Your devices on the phone: a computer on the same Wi-Fi at 82%">
  <img src="screenshots/phone-device-dark.png" width="150" alt="A computer's page on the phone: Send files, Clipboard, Ping, Remote, Find it, See its screen">
  <img src="screenshots/phone-webcam.png" width="150" alt="The phone's camera live as the computer's webcam, with zoom, torch and light controls">
  <img src="screenshots/phone-remote.png" width="150" alt="The phone as a touchpad, with left and right click and a keyboard">
  <img src="screenshots/phone-terminal.png" width="150" alt="A shell on the computer from the phone, with Esc, Ctrl, Alt, Tab and arrows above the keyboard">
</p>

<p align="center">
  <img src="screenshots/desktop-light.png" width="470" alt="Linksy on Linux, light style">
  <img src="screenshots/phone-watch-screen.png" width="300" alt="The computer's screen shown on the phone, full screen in landscape">
</p>

---

## Private by design

- **Paired once**: devices compare a code, then only talk to each other.
- **Encrypted end to end**: QUIC and TLS 1.3, with each device's own key.
- **Nothing collected**: no account, no sign-in, no analytics.
- **The relay can't read**: away from home it only helps your devices find each other.
- **Always asks**: screens, cameras, microphones and the terminal ask first and show while on.

---

## Windows, macOS, iPhone?

No plans. Linksy aims to be the best at Linux and Android: each other system would be a
whole new app, its best features (webcam, second display) need paid, signed drivers, and an
iPhone app can barely run in the background or read the clipboard.

---

## Help

- **Something wrong?** [Open an issue](https://github.com/LinkSy-mg/linksy-releases/issues)
  with what you did and what happened.
- **First pairing:** both devices on the same network, or a USB cable. Finish Setup checks
  the firewall lets them meet.

Free and open source under the GNU AGPL v3.0 or later:
[LinkSy-mg/linksy-desktop](https://github.com/LinkSy-mg/linksy-desktop). A star there helps
others find Linksy.
