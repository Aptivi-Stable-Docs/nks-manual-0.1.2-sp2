---
description: What do I need to run Nitrocid?
icon: box
---

# Dependency Information

{% hint style="info" %}
Windows users don't need to read this page as Windows provides all the necessary tools to facilitate the work of the kernel and its addons.
{% endhint %}

In order to run Nitrocid KS on all the system, you must install the essential requirements as shown in the platform-specific installation pages. However, for Linux and Android systems, you must also install the following dependencies to be able to use Nitrocid.

{% hint style="info" %}
For [Ubuntu](https://packages.ubuntu.com/search?keywords=icu\&searchon=sourcenames), [Debian](https://packages.debian.org/search?suite=all\&searchon=sourcenames\&keywords=icu), and their alternatives, you can consult a list of `libicu` versions that you can download for your distribution version. Replace `libicuXX` with the library version number applicable for your distribution.
{% endhint %}

* For Debian and its derivatives (Ubuntu, LMDE, ...)
  * ```sh
    sudo apt install tzdata
    ```
* For Android (Ubuntu PRoot on Termux)
  * ```sh
    sudo apt install libicuXX tzdata
    ```
* For Red Hat Enterprise Linux, Rocky Linux, AlmaLinux, ...
  * ```sh
    sudo dnf install -y epel-release
    sudo dnf install -y libicu tzdata
    ```
* For OpenSUSE
  * ```sh
    sudo zypper install libicu tzdata
    ```
* For Arch Linux and its derivatives (EndeavorOS, ...)
  * ```sh
    sudo pacman -S icu tzdata
    ```
* For Alpine Linux
  * ```sh
    sudo apk add icu icu-libs icu-data-full tzdata
    ```

{% hint style="info" %}
Depending on a distribution and the amount of packages installed in the current system, the download size will be from 30 to 100 MB.

For addons, extra dependencies might be needed to work. For example, the BassBoom addon might need PulseAudio or ALSA working.
{% endhint %}

Dependency information for each package installed in your target system:

* `icu` and its related packages
  * To provide localization information. Needed for the multilingual kernel system.
* `tzdata`
  * To provide time zone information, like listing all available time zones.

In addition to the base kernel requirements, all addons might require additional packages to be installed in your system:

* `pulseaudio, libasound2, ...`
  * To be able to play music using PulseAudio, ALSA, JACK, etc. Used by the BassBoom addon.
