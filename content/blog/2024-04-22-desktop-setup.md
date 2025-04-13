+++
title = "Desktop and Mobile Setup"
date = 2024-04-22
updated = 2024-05-04
+++

Setting up a new computer is always exciting, but when you have a number of
ongoing projects and work that quickly needs to be resumed without downtime, it
is worth standardizing and documenting the process.

Following is my preferred computer desktop setup which I replicate on any new
machine I use:

* OS: Debian stable
  * To [enable higher resolutions](https://www.reddit.com/r/wayland/comments/14hhath/comment/jpbynnv/?utm_source=share&utm_medium=web3x&utm_name=web3xcss&utm_term=1&utm_content=share_button)
    on my Acer EL220Q monitor:
    * Edit /etc/default/grub and set GRUB_CMDLINE_LINUX to "video=VGA-1:1920x1080@64.9". In case this doesn't work, try a lower refresh rate like @49.9.
    * Run 'sudo update-grub' and reboot.
* OS: Windows when I am forced to
  * [Scoop](https://scoop.sh/) package manager for installing applications
* Desktop: Gnome with the following extensions:
  * [Top Indicator App](https://github.com/ubuntu/gnome-shell-extension-appindicator)
  * [TopHat](https://github.com/fflewddur/tophat)
* Web Browser: Firefox with the following extensions:
  * [uBlacklist](https://iorate.github.io/ublacklist/docs)
  * [uBlock Origin](https://github.com/gorhill/uBlock)
* Tools:
  * [Password Safe / Secrets](https://gitlab.gnome.org/World/secrets). [KeePassXC](https://keepassxc.org/) when I am using Windows.
  * [Create new SSH key](https://github.com/settings/ssh/new)
  * git
    ```
    git config --global user.email "arunkd13@gmail.com"
    git config --global user.name "Arunkumar Dhananjayan"
    ```
* IDE: [Visual Studio Code](https://code.visualstudio.com/) with following extensions:
  * vscodevim.vim
  * vscode-org-mode.org-mode
* Application Software:
  * [Zola](https://www.getzola.org/documentation/getting-started/installation/#debian)
  * [Dropbox](https://www.dropbox.com/)
  * [Gnucash](https://www.gnucash.org/)
  * [Gimp](https://www.gimp.org/)

Following is my mobile setup with my preferred apps:
* OS: Android
* Apps
  * [Files](https://play.google.com/store/apps/details?id=com.google.android.apps.nbu.files)
  * [Dropbox](https://play.google.com/store/apps/details?id=com.dropbox.android)
  * [Orgzly](https://play.google.com/store/apps/details?id=com.orgzly)
  * [KeePassDroid](https://play.google.com/store/apps/details?id=com.android.keepass)
  * [Weather Underground](https://play.google.com/store/apps/details?id=com.wunderground.android.weather)
  * [F-Droid](https://f-droid.org/)
  * [NewPipe](https://f-droid.org/en/packages/org.schabi.newpipe/)
