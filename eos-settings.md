# Elementary OS: personal settings

---

## Table of Contents

* [Disk Partition](#disk-partition)

* [Add PPA](#add-ppa-repositories-management)

* [Hide GRUB](#hide-grub)

* [Pantheon Tweaks](#pantheon-tweaks)

* [Additional GNOME Settings](#additional-gnome-settings)

* [KeePassXC](#keepassxc)

* [Firefox + bonus](#firefox-via-official-mozilla-ppa-repository)

* [Installation from DEBs](#installation-from-debs)

* [Fonts](#fonts)

* [OPT Folder](#opt-folder)

* [Audacity](#audacity)

* [gThumb](#gthumb)

* [GIMP](#gimp)

* [qBittorrent](#qbittorrent)

* [Foliate](#foliate)

* [Ksnip](#ksnip)

* [Drawing](#drawing)

* [Conky](#conky)

* [GTK for QT](#add-support-of-gtk-for-qt)

* [Correct Jibberish Coding](#correct-jibberish-coding)

---

## Disk Partition

Install **Elementary OS** in the Expert Mode and partition your disk space as you need. The following table is the example of my disk.

| Order | Size     | File System | Mount       | Flags     |
|-------|----------|-------------|-------------|-----------|
| 1     | 512 Mb   | fat32       | /boot/efi   | boot, esp |
| 2     | 50-55 Gb | btrfs       | /           |           |
| 3     | 8 GB     | linux-swap  |             | swap      |
| 4     | All      | btrfs       | /home       |           |

⚠️ Choose ROOT and SWAP size as well as file system for ROOT and HOME in accordance with your demands.

---

## Add PPA Repositories Management

```
sudo apt install -y software-properties-common software-properties-gtk
```

---

## Hide GRUB

1. Open the following file as admin `/etc/default/grub`

2. Add the following string `GRUB_RECORDFAIL_TIMEOUT=0` and save the file.

3. Run `sudo update-grub`

---

## Pantheon Tweaks

```
sudo add-apt-repository -y ppa:philip.scott/pantheon-tweaks
sudo apt install -y pantheon-tweaks
```

---

## Additional GNOME settings

```
sudo apt install gnome-tweaks gnome-tweak-tool gnome-shell-common
```
---

## KeePassXC

```
sudo add-apt-repository ppa:phoerious/keepassxc
sudo apt install keepassxc
```

---

## Firefox via official Mozilla PPA repository

Add repository

```
sudo add-apt-repository ppa:mozillateam/ppa
```

Install Firefox

```
sudo apt install -t 'o=LP-PPA-mozillateam' firefox
```
 
Create the file `/etc/apt/preferences.d/mozillateamppa`

```
sudo vi /etc/apt/preferences.d/mozillateamppa
```

Add the following content in the file:

```
Package: firefox*
Pin: release o=LP-PPA-mozillateam
Pin-Priority: 501
```

### Firefox Elementary Theme

https://github.com/Zonnev/elementaryos-firefox-theme

### Rework Ublock

Import the following to **Ublock**:   
https://easylist-downloads.adblockplus.org/cntblock.txt

It kills all Yandex adds (including mail UI)

---

## Installation from DEBs

Open **Terminal** from the folder where the DEB file is stored and run

Install

```
sudo dpkg -i <app-file-name>.deb
```

Remove

```
sudo apt remove <app-name>
```

Remove with all config files

```
sudo apt purge <app-name>.deb
```

---

## Fonts

```
sudo apt install ttf-mscorefonts-installer
```

```
sudo apt install xfonts-terminus fonts-terminus ttf-dejavu fonts-liberation fonts-liberation2 fonts-crosextra-carlito fonts-crosextra-caladea fonts-cantarell
```

---

## OPT Folder

Extract from an archive to OPT

```
sudo tar xvf ~/app-name.tar.bz2 -C /opt/
```

Remove from OPT

```
sudo rm -fr /opt/app-name
```

Install Telegram

```
sudo tar xvf <app-archive-fullname> -C /opt/
```

---

## Audacity

```
sudo add-apt-repository ppa:ubuntuhandbook1/audacity
```

or Flatpak

---

## gThumb

```
sudo add-apt-repository ppa:ubuntuhandbook1/apps
sudo apt update
sudo apt install gthumb
```

---

## GIMP

```
sudo add-apt-repository ppa:ubuntuhandbook1/gimp
sudo apt update
sudo apt install gimp
```

may be not necessary since we have this:

https://www.photopea.com/

---

## qBittorrent

```
sudo add-apt-repository ppa:qbittorrent-team/qbittorrent-stable
sudo apt update
sudo apt install qbittorrent
```

---

## Foliate

```
sudo add-apt-repository ppa:apandada1/foliate
sudo apt update
sudo apt install foliate
```

---

## KSnip

⚠️ I prefer installation via [DEB file](https://github.com/ksnip/ksnip/releases)

via APT is for older UBUNTU versions only

```
sudo add-apt-repository ppa:nemonein/ksnip
sudo apt update
sudo apt install ksnip
```

---

## Drawing

```
sudo add-apt-repository ppa:cartes/drawing
sudo apt update
```

---

## Conky

```
sudo apt install conky conky-all
sudo apt install lm-sensors
```

Extract [files](https://disk.yandex.ru/d/exuqS3j7mH3XrQ) to `~/home/.Conky`

Add fonts for clocks to `~/home/.fonts`

Add to autostart:

```
conky -c /home/dedared/.Conky/default/conky.conf
```
```
.Conky/revolutionary_clocks/rev_midi/start_conky.sh
```

---

## Add support of GTK for QT

```
sudo apt install qt5-style-plugins qt5ct
```

In the file `/etc/profile.d/qt-style-override.sh`

remove the string `export QT_STYLE_OVERRIDE=adwaita`

In the file `/etc/profile.d/qt-qpa-platformtheme.sh`

must be `export QT_QPA_PLATFORMTHEME=qt5ct`

---

## Correct jibberish coding

1. Check locale:

  ```
  locale -a
  ```

2. If it doesn't have **ru_RU.cp1251**, open as admin:

  ```
  ~/var/lib/locales/supported.d/ru
  ```
  
3. Add:

```
ru_RU.CP1251 CP1251
ru_RU.KOI8-R KOI8-R
```

4. Save and run:

```
sudo locale-gen
```

It must result with:

```
Generating locales...
  en_US.UTF-8... done
  ru_RU.CP1251... done
  ru_RU.KOI8-R... done
  ru_RU.UTF-8... up-to-date
  ru_UA.UTF-8... up-to-date
Generation complete.
```

4. Check locale again:

```
locale -a
```

Must be like this:

```
en_US.utf8
POSIX
ru_RU.cp1251
ru_RU.koi8r
ru_RU.utf8
ru_UA.utf8
```
