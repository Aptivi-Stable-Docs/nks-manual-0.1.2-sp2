---
description: How to upgrade Nitrocid KS on Windows
icon: windows
---

# Windows

Upgrading your kernel on Windows is pretty simple, depending on the way you've installed the simulator. To upgrade your kernel, choose a method. Please note that the second method, which is unpacking the update yourself, can also be done with the bleeding-edge builds.

{% hint style="info" %}
If you're upgrading bleeding-edge builds, it's recommended that you uninstall the old copy and reinstall the newer version. It doesn't wipe your Nitrocid KS data, though.
{% endhint %}

## Method 1: Windows Installer

The Windows Installer method allows you to easily upgrade Nitrocid KS.

1. Download the latest Windows Installer EXE file from [this page](https://github.com/Aptivi/Kernel-Simulator/releases)
2. Double-click on a single EXE file, and follow the instructions
3. Double-click on `Nitrocid KS` in your desktop.

## Method 2: Using Chocolatey

Any updates to the KS Chocolatey package can be done using a built-in Chocolatey command. To update the kernel, follow these steps:

1. Open your favorite terminal emulator, like ConEmu
2. Run `choco upgrade ks`
3. Once the upgrade is done, run KS like you normally would

## Method 3: Manually unpacking

Nitrocid KS can also be manually updated in case the automatic updater failed to update. To update the kernel, perform the same steps as in installing KS. Run the executable to upgrade your kernel configuration files to the latest.

1. Ensure that you have all the required software installed
2. Download the latest release ZIP file from [this page](https://github.com/Aptivi/Kernel-Simulator/releases).
3. Unpack the ZIP archive to any folder of your choice
4. Open your favorite terminal emulator, like ConEmu, and change the working directory to a folder containing the Nitrocid KS executable
5. Execute `ks` or `Nitrocid.exe` to start the kernel
