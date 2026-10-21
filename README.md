<p align="center">
  <img src="assets/linksy-mark.svg" width="96" height="96" alt="">
</p>

<h1 align="center">Linksy</h1>

<p align="center">
  <b>Your phone and your computer, connected. Or two computers.</b><br>
  Files, clipboard, screens, a webcam and more, straight between your own devices.<br>
  No account. No cloud. Nothing stored anywhere but on your devices.
</p>

<p align="center">
  <a href="#android"><b>Android</b></a> ·
  <a href="#linux"><b>Linux</b></a> ·
  <a href="https://linksy.diary.mg">Website</a> ·
  <a href="https://github.com/LinkSy-mg/linksy-releases/issues">Report a problem</a>
</p>

<p align="center">
  <img src="screenshots/desktop-dark.png" width="760" alt="Linksy on Linux: a phone's page with Send Files, Clipboard, View Screen, Ring and Locate, Use as Second Display or Webcam, and the activity">
</p>

## Download

Install Linksy on both devices, open it on each, and pair them once: both screens show
the same code. That's it.

It works between any two devices with Linksy, not only a phone and a computer: two Linux
computers on the same network pair the same way, then send files and the clipboard, see
and control each other's screen, or use one as a second display for the other.

### Android

| | |
|---|---|
| **[linksy.apk](https://github.com/LinkSy-mg/linksy-releases/releases/latest/download/linksy.apk)** | Works on every Android phone. Start here. |
| [linksy-arm64.apk](https://github.com/LinkSy-mg/linksy-releases/releases/latest/download/linksy-arm64.apk) | Smaller, for 64-bit phones. |
| [linksy-armv7.apk](https://github.com/LinkSy-mg/linksy-releases/releases/latest/download/linksy-armv7.apk) | Smaller, for older 32-bit phones. |

Open the downloaded file on the phone. Android asks once to allow installing apps from
your browser; allow it, then install. To update, install a newer one the same way.

### Linux

<!-- linux:start -->
Linksy **0.7.0** for x86_64. Pick the one for your system:

| System | Download | Then, in a terminal |
|---|---|---|
| **Fedora** 41+ | [linksy-0.7.0-1.x86_64.rpm](https://github.com/LinkSy-mg/linksy-releases/releases/download/linux-v0.7.0/linksy-0.7.0-1.x86_64.rpm) | `sudo dnf install ./linksy-0.7.0-1.x86_64.rpm` |
| **Ubuntu** 24.10+, **Debian** 13+ | [linksy_0.7.0_amd64.deb](https://github.com/LinkSy-mg/linksy-releases/releases/download/linux-v0.7.0/linksy_0.7.0_amd64.deb) | `sudo apt install ./linksy_0.7.0_amd64.deb` |
| **Any distribution** (Flatpak) | [linksy-0.7.0.flatpak](https://github.com/LinkSy-mg/linksy-releases/releases/download/linux-v0.7.0/linksy-0.7.0.flatpak) | `flatpak install --user linksy-0.7.0.flatpak` |
| Any distribution, no root | [linksy-0.7.0-linux-x86_64.tar.gz](https://github.com/LinkSy-mg/linksy-releases/releases/download/linux-v0.7.0/linksy-0.7.0-linux-x86_64.tar.gz) | `tar xzf linksy-0.7.0-linux-x86_64.tar.gz && linksy-0.7.0-linux-x86_64/install.sh` |

Release notes and checksums: [Linksy 0.7.0 for Linux](https://github.com/LinkSy-mg/linksy-releases/releases/tag/linux-v0.7.0).
<!-- linux:end -->

Then open **Linksy** from your apps. If your system is missing something a feature needs
(a codec, the camera driver, the firewall rule), **Finish Setup** opens and adds it all in
one go; your computer asks for your password once. Linksy updates itself in the
background after you install a newer version, and tells you when there is one.

The .deb, .rpm and tarball need glibc 2.39+, GTK 4.14+ and libadwaita 1.6+ (the systems
above have them). The Flatpak runs anywhere, but can't add the webcam driver or open a
terminal for your phone.

## What it does

Between a phone and a computer, or between two computers:

- **Files and folders**, any size, both ways. Drop them on the window; transfers resume
  and are checked byte for byte.
- **Clipboard**: copy on one, paste on the other. Text, a screenshot or a small file.
- **Open on PC**: share a link from any phone app and it opens on the computer.
- **Your phone as a webcam, microphone or second display**, in every app.
- **See and control** another device's screen, or use the phone as a touchpad, keyboard
  or slide clicker.
- **Find your phone**: make it ring, even on silent, or ask where it is.
- **Lock when away**: walk off with your phone and the computer locks.
- **Terminal on your phone** (coming to Android): Claude Code, neovim or a build on your
  computer, behind a code you set on the computer.
- **Away from home**: files, clipboard, links and Ring over the internet too, for a week
  after your devices were last together.
- Over **Wi-Fi** or a **USB cable**.

## Screenshots

<p align="center">
  <img src="screenshots/phone-home-dark.png" width="190" alt="The phone app: your computers">
  <img src="screenshots/phone-device-dark.png" width="190" alt="A computer's page on the phone">
  <img src="screenshots/phone-incoming-files.png" width="190" alt="Files arriving on the phone">
  <img src="screenshots/phone-remote.png" width="190" alt="The phone as a touchpad and remote">
</p>

<p align="center">
  <img src="screenshots/desktop-light.png" width="760" alt="Linksy on Linux, light style">
</p>

## Private by design

- Devices pair once by comparing a code; after that they only talk to each other,
  encrypted end to end (QUIC, TLS 1.3 with each device's own key).
- No account, no sign-in, no analytics. Nothing about you or your files is sent anywhere.
- Away from home, Linksy's relay only helps two devices find each other; it can't read
  anything.
- Screens, cameras, microphones and the terminal always ask first, and show while
  they're on.

## Help

- Something not working? [Open an issue](https://github.com/LinkSy-mg/linksy-releases/issues)
  with what you did and what happened.
- Both devices need to be on the same network the first time you pair them (or connected
  by a USB cable). On Linux, Finish Setup checks your firewall lets them meet.

Linksy is freeware: free to use on all your devices, for personal or commercial use, and
free to share unmodified. [License](https://linksy.diary.mg/license).
