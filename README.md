# Omni Control

Omni Control is a remote management application that lets you control and monitor your computer directly from your phone.

## Download

| File | Install on |
|---|---|
| [OmniControl.apk](https://github.com/ufuksagcan927-star/omni-control/raw/main/OmniControl.apk) | Android phone |
| [OmniControl.exe](https://github.com/ufuksagcan927-star/omni-control/raw/main/OmniControl.exe) | Windows PC |
| [OmniControl-linux-x64.tar.gz](https://github.com/ufuksagcan927-star/omni-control/raw/main/OmniControl-linux-x64.tar.gz) | Linux PC: Ubuntu 22.04 or newer, Linux Mint 21 or newer, Debian 12, Pardus 23, Arch Linux and systems built on it (Garuda, Manjaro...) |
| [OmniControl-mac-AppleSilicon.zip](https://github.com/ufuksagcan927-star/omni-control/raw/main/OmniControl-mac-AppleSilicon.zip) | Mac with an Apple chip (M1, M2, M3...), **beta** |
| [OmniControl-mac-Intel.zip](https://github.com/ufuksagcan927-star/omni-control/raw/main/OmniControl-mac-Intel.zip) | Mac with an Intel processor, **beta** |

Clicking a file name downloads it.

Install the app on your phone and the program on your computer, then connect with the QR code or the password the computer shows.

## Features

*   **Hardware Monitoring:** CPU and RAM usage and GPU temperature. A value the computer does not expose is shown as "-".
*   **System Controls:** volume, mute and screen brightness; sleep, restart and shut down.
*   **Remote Screen & Touchpad:** watch your computer's screen live with zoom and the mouse pointer, tap the picture to click there, or use the phone as a touchpad (two-finger scroll and right click, hold to drag).
*   **Keyboard:** type in any language, emoji included, and send common shortcuts.
*   **Media Controls:** play, pause and skip in your media players.
*   **Files and Apps:** browse the computer's folders, send files both ways, open apps and pinned shortcuts.

## Running on Linux

1. Right-click the downloaded file and choose "Extract Here" or "Extract" (on KDE desktops such as Garuda: "Extract" > "Extract archive here"). Then double-click the extracted OmniControl file; if that does not start it, right-click it and choose "Run as a Program". Extract it first: started from inside the archive window it may not open.
   Or in a terminal opened in the folder with the file: `tar xzf OmniControl-linux-x64.tar.gz && ./OmniControl`
2. Screen sharing and mouse control need an Xorg (X11) session. If you log in with Wayland, pick the X11 session on the login screen: "Ubuntu on Xorg" on Ubuntu, "Plasma (X11)" on KDE desktops. Garuda and other Arch-based KDE systems need it installed first: `sudo pacman -S plasma-x11-session`, then log out.

If the phone cannot find the computer, a firewall may be blocking it:
*   Ubuntu, Mint, Pardus: `sudo ufw allow 8765/tcp && sudo ufw allow 8766/udp`
*   Fedora, Garuda and other systems with firewalld: `sudo firewall-cmd --permanent --add-port=8765/tcp --add-port=8766/udp && sudo firewall-cmd --reload`

If no window appears, start it from a terminal (`./OmniControl`) and send us what it prints, or the file `~/.config/OmniControl/OmniControl_error.log`.

## Running on a Mac (beta)

1. Unzip the file and move OmniControl into Applications. The app is not signed with an Apple developer account, so the first time macOS says it cannot verify it: open System Settings > Privacy & Security and click "Open Anyway" (on macOS 14 and older, right-click the app and choose Open).
2. When asked, allow "Screen Recording" and "Accessibility" for OmniControl, then quit and reopen it.

The Mac version passes automatic tests on macOS 15 and macOS 26 (Apple chip and Intel) but has not yet been tried by a person on a real Mac. Please report any problem.

## Platform Support

*   **Computer:** Windows, Linux (Xorg sessions; on Wayland the program runs but cannot share the screen or move the mouse), macOS (beta).
*   **Mobile:** Android (APK provided).

## What's new

### 6 October 2026

*   **Linux on Arch-based systems (Garuda, Manjaro, EndeavourOS):** tested on Arch Linux with an Xorg desktop and with KDE Plasma on Wayland. The program now uses the computer's own font library, so it no longer prints dozens of "Fontconfig error" lines or builds a second font cache when it first starts.
*   **Linux tray icon in every language:** with the program set to Russian, Polish, Chinese and some other languages, the tray icon did not appear. Now it does.
*   **Linux typing:** a letter the keyboard layout does not have was occasionally lost while typing. Fixed.
*   **Wayland hint:** the message shown on a Wayland session now also names KDE's X11 session, "Plasma (X11)".
*   The Windows and Android versions work the same as before.

### 5 October 2026, second update

*   **Linux typing fix:** letters the keyboard layout does not have (Turkish letters on an English layout, other languages, emoji) are no longer mixed up or lost when the program you type into is busy.
*   **Under the hood:** the computer program and the phone app are now organized in one part per feature, which keeps future changes safer. They look and work the same as before.

### 5 October 2026

*   **Linux and macOS (beta):** the computer program now runs on Linux and on Macs as well as on Windows.
*   **Screen share and touchpad rebuilt:** a larger, zoomable screen with the mouse pointer drawn on it, a sharper picture with Low/Medium/High quality, and tapping the picture clicks there. The touchpad clicks instantly on tap and has two-finger scroll and right click, acceleration and hold-to-drag. A keyboard sheet types in any language.
*   **GPU temperature without administrator rights**, for NVIDIA and other graphics cards.
*   **Fixes:** the chosen language is kept after a restart; the QR code window no longer cuts the code off; "Start with the computer" now works on Windows installations where it failed without a message; the mouse no longer gets stuck in the screen corners.
