## Installation

Each release has files for all the operating systems we support. You only need the files that are relevant to your operating system


### Install Plover on Windows

1. Download the `.exe` file from the release page.
  * You can place the file anywhere on your computer. You will run it from the same location every time.
2. Open the file to launch Plover.


### Install Plover on Mac

If you have [Homebrew Cask](https://caskroom.github.io/) installed on your system, you can run `brew cask install plover` at the command-line. Otherwise:

1. Download the `.dmg` file from the release page.
1. Open the `.dmg` file.
1. In the mounted disk, drag the `Plover.app` to your `Applications` folder.
1. Open `System Preferences > Security & Privacy > Privacy > Accessibility`.
1. Click the "+" Button, and go to your applications and select `Plover.app`.

If you use a keyboard instead of a steno machine, Plover needs [Assistive Device Permissions](https://support.apple.com/en-ca/guide/mac-help/mh43185/mac). From the Catalina version of macOS, you may need to enable both the `Plover` app and the `env` app under Security & Privacy > Privacy > Accessibility.

Plover is set up! You can run Plover like you would any other application.

> **Note**: Other "keyboard helper"-type applications (e.g. Karabiner Elements and text expanders) may interfere with Plover.


### Install Plover on Linux


#### Install Plover on Arch Linux distribution

Two AUR packages are provided:

1. [plover](https://aur.archlinux.org/packages/plover/) for the latest stable release
2. and [plover-git](https://aur.archlinux.org/packages/plover-git/) for the current `master`

 - You may need to add yourself to the group "uucp" (owner of `/dev/ttyACM*`, which is usually where your keyboard will show up).
 - These AUR packages do not come with the Plover plugins manager. This needs to be installed separately via [`pip install plover-plugins-manager`](https://pypi.org/project/plover-plugins-manager/).


#### Install Plover on Gentoo Linux distribution

Currently, only a git ebuild for the `master` branch is provided.

[Personal overlay.](https://framagit.org/3/ebuilds)


#### Install Plover on Ubuntu Linux distribution

Stable releases can be installed from a dedicated PPA, see [ppa:benoit.pierre/plover](https://launchpad.net/~benoit.pierre/+archive/ubuntu/plover) for instructions.

_2019-02-25 Note_: The PPA method doesn't currently appear to work with Ubuntu 18.04 Bionic Beaver ([there is a listing for Xenial however](https://launchpad.net/~benoit.pierre/+archive/ubuntu/plover/+packages)). One can use the [AppImage method](#appimage-method) instead. Similarly for weeklies one can use the AppImage method or [other approaches](#other-approaches) for installing on other Linux distributions.


#### Install Plover on other Linux distributions

##### AppImage Method 

An [AppImage](http://appimage.org/) is provided: it includes all the necessary dependencies and should run on most x86 64-bits distributions. To use it:

- download it
- add the user to the group "dialout" (`sudo adduser <user> dialout`)
- after adding the group, logout and login again for the change to take effect
- [make it executable](http://discourse.appimage.org/t/how-to-make-an-appimage-executable/80)
- launch it like a standard executable

Note: you can install the AppImage for your current user (and register Plover in your standard applications menu) by executing it with the `--install` flag. If you had previously installed another AppImage version of Plover, it will be automatically uninstalled and replaced.

As of January 2019 AppImage files are not in the [latest stable version](https://github.com/openstenoproject/plover/releases/latest) but can be found in [weeklies](https://github.com/openstenoproject/plover/tags) or [weekly](https://github.com/openstenoproject/plover/releases).  

##### Other Approaches 

Other approaches could include:

 - Seeking to install from the `deb` file if you are using Debian or a Debian derived distribution (e.g. with `sudo apt install <path/deb file>` or using `dpkg` ), but you may need to do some work to deal with handling the dependencies.
 - Seeking to [install from source for Linux](https://github.com/openstenoproject/plover/tree/master/linux).