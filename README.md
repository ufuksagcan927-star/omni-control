# Omni Control

Omni Control is a remote management application that lets you control and monitor your computer directly from your phone.

## Download

| File | Install on |
|---|---|
| [OmniControl.apk](OmniControl.apk) | Android phone |
| [OmniControl.exe](OmniControl.exe) | Windows PC |
| [OmniControl-linux-x64.tar.gz](OmniControl-linux-x64.tar.gz) | Linux PC: Ubuntu 22.04 or newer, Linux Mint 21 or newer, Debian 12, Pardus 23 |
| [OmniControl-mac-AppleSilicon.zip](OmniControl-mac-AppleSilicon.zip) | Mac with an Apple chip (M1, M2, M3...), **beta** |
| [OmniControl-mac-Intel.zip](OmniControl-mac-Intel.zip) | Mac with an Intel processor, **beta** |

Install the app on your phone and the program on your computer, then connect with the QR code or the password the computer shows.

## Features

*   **Hardware Monitoring:** CPU and RAM usage and GPU temperature. A value the computer does not expose is shown as "-".
*   **System Controls:** volume, mute and screen brightness; sleep, restart and shut down.
*   **Remote Screen & Touchpad:** watch your computer's screen live with zoom and the mouse pointer, tap the picture to click there, or use the phone as a touchpad (two-finger scroll and right click, hold to drag).
*   **Keyboard:** type in any language, emoji included, and send common shortcuts.
*   **Media Controls:** play, pause and skip in your media players.
*   **Files and Apps:** browse the computer's folders, send files both ways, open apps and pinned shortcuts.

## Running on Linux

1. Put the file in a folder, right-click inside the folder, choose "Open in Terminal" and run:
   `tar xzf OmniControl-linux-x64.tar.gz && ./OmniControl`
2. Screen sharing and mouse control need an Xorg session. If you log in with Wayland, pick "Xorg" on the login screen (on Ubuntu: "Ubuntu on Xorg").

If the phone cannot find the computer, a firewall may be blocking it: `sudo ufw allow 8765/tcp && sudo ufw allow 8766/udp`

## Running on a Mac (beta)

1. Unzip the file and move OmniControl into Applications. The app is not signed with an Apple developer account, so the first time macOS says it cannot verify it: open System Settings > Privacy & Security and click "Open Anyway" (on macOS 14 and older, right-click the app and choose Open).
2. When asked, allow "Screen Recording" and "Accessibility" for OmniControl, then quit and reopen it.

The Mac version passes automatic tests on macOS 15 and macOS 26 (Apple chip and Intel) but has not yet been tried by a person on a real Mac. Please report any problem.

## Platform Support

*   **Computer:** Windows, Linux (Xorg sessions), macOS (beta).
*   **Mobile:** Android (APK provided).

## What's new

### 5 October 2026

*   **Linux and macOS (beta):** the computer program now runs on Linux and on Macs as well as on Windows.
*   **Screen share and touchpad rebuilt:** a larger, zoomable screen with the mouse pointer drawn on it, a sharper picture with Low/Medium/High quality, and tapping the picture clicks there. The touchpad clicks instantly on tap and has two-finger scroll and right click, acceleration and hold-to-drag. A keyboard sheet types in any language.
*   **GPU temperature without administrator rights**, for NVIDIA and other graphics cards.
*   **Fixes:** the chosen language is kept after a restart; the QR code window no longer cuts the code off; "Start with the computer" now works on Windows installations where it failed without a message; the mouse no longer gets stuck in the screen corners.
