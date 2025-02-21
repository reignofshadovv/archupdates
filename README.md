# ArchUpdates

ArchUpdates is a simple package for automating system updates on Arch Linux. It provides an update script and user-level systemd service and timer units to run the update process automatically every Saturday at midnight.

## Features

- **Automated Updates:** Runs your update script every Saturday at 00:00.
- **User-level Services:** Installs as a user service and timer, ensuring the updates run after your desktop environment is loaded.
- **Persistent Scheduling:** With `Persistent=true`, missed updates (if the computer is off) will run at the next login.
- **Customizable:** Easily modify the update script and unit files to suit your needs.

## Installation

Ensure you have the `base-devel` group installed. Then, build and install the package using `makepkg`:

```bash
makepkg -si
