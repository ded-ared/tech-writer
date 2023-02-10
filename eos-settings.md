# Elementary OS: settings
-----------------------------------

## Disk Partition

| Order | Size     | File System | Mount       | Flags     |
|-------|----------|-------------|-------------|-----------|
| 1     | 512 Mb   | fat32       | /boot/efi   | boot, esp |
| 2     | 50-55 Gb | btrfs       | /           |           |
| 3     | 8 GB     | linux-swap  |             | swap      |
| 4     | All      | btrfs       | /home       |           |

⚠️ Объем под ROOT и SWAP, а также файловую систему под ROOT и HOME выбирайте по своим потребностям и на свое усмотрение.

-----

## Добавить возможность устанавливать программы через репозитории РРА:

```sudo apt install -y software-properties-common software-properties-gtk```

**Далее для установки использовать:**

Найти программу

```sudo apt search <program-name>```

Установить

```sudo apt install <program-name>```

Удалить

```sudo apt remove <program-name>```

```sudo spt purge <program-name>```

-----

## Скрыть меню GRUB при загрузке ОС.

1. Открыть от имени администратора файл:   
```/etc/default/grub```

2. Добавить в него строку:   
```GRUB_RECORDFAIL_TIMEOUT=0```

3. Выполнить:   
```sudo update-grub```

-----

## Pantheon Tweaks для расширенной настройки ОС

```
sudo add-apt-repository -y ppa:philip.scott/pantheon-tweaks
sudo apt install -y pantheon-tweaks
```

---

## Дополнительные настройки из GNOME

*(Там есть очень нужные настройки обработки шрифтов)*

```
sudo apt install gnome-tweaks gnome-tweak-tool gnome-shell-common
```

## Менеджер паролей KeePassXC

```
sudo add-apt-repository ppa:phoerious/keepassxc
sudo apt install keepassxc
```
---

## Firefox через официальный PPA репозиторий Mozilla:

```
sudo add-apt-repository ppa:mozillateam/ppa
```

Установить Firefox следующей командой:

```
sudo apt install -t 'o=LP-PPA-mozillateam' firefox
```

Здесь нужно с помощью параметра ```-t``` явно указывать откуда устанавливать программу, потому что по умолчанию у snap приоритет выше.   
После установки можно поднять приоритет этого репозитория.   
Для этого создать файл `/etc/apt/preferences.d/mozillateamppa`

```
sudo vi /etc/apt/preferences.d/mozillateamppa
```
Добавить в него следующее содержание:

```
Package: firefox*
Pin: release o=LP-PPA-mozillateam
Pin-Priority: 501
```

### Допилить **ublock**

Импортировать в него:   
https://easylist-downloads.adblockplus.org/cntblock.txt

Это отключает рекламу в сервисах Яндекса (в почте в том числе). Со стандартными настройками ее не вытравишь.

---

## Установка программ из DEB пакетов

Чтобы установить программу из DEB пакета, нужно зайти в терминал из той папки, в которой пакет находится.

Установить deb-пакет   
```
sudo dpkg -i имя_пакета.deb
```

Удалить deb-пакет   
```
sudo apt remove имя_пакета.deb
```

Удалить пакет со всеми его настройками:   
```
sudo apt purge имя_пакета.deb
```

---

## Шрифты

```
sudo apt install ttf-mscorefonts-installer

sudo apt install xfonts-terminus fonts-terminus ttf-dejavu fonts-liberation fonts-liberation2 fonts-crosextra-carlito fonts-crosextra-caladea fonts-cantarell
```

---

## Защищенные папки

Внести из архива в защищенную папку

```
sudo tar xvf ~/app-name.tar.bz2 -C /opt/
```

Удалить из защищенной папки

```
sudo rm -fr /opt/app-name
```

Например, так можно установить Telegram:

```
sudo tar xvf /home/dedared/Софт/Linux Apps/tsetup.4.6.0.tar.xz -C /opt/
```

---

## Audacity (Music Editor)

```
audacity 302
sudo add-apt-repository ppa:ubuntuhandbook1/audacity
```

или через Flatpak

---

## gThumb (Image Viewer)

```
gthumb
sudo add-apt-repository ppa:ubuntuhandbook1/apps
sudo apt update
sudo apt install gthumb
```

---

## GIMP (Image Editor)

```
sudo add-apt-repository ppa:ubuntuhandbook1/gimp
sudo apt update
sudo apt install gimp
```

не особо надо, есть вот это:

https://www.photopea.com/

---

## qBittorrent

```
sudo add-apt-repository ppa:qbittorrent-team/qbittorrent-stable
sudo apt update
sudo apt install qbittorrent
```

---

## Foliate (Reader)

```
sudo add-apt-repository ppa:apandada1/foliate
sudo apt update
sudo apt install foliate
```

---

## KSnip (Screenshoter)

⚠️ Надо [скачать deb пакет!!!](https://github.com/ksnip/ksnip/releases)

Через репозиторий только для UBUNTU до 21 версии

```
sudo add-apt-repository ppa:nemonein/ksnip
sudo apt update
sudo apt install ksnip
```

Если косячный, лучше установить Shutter, репозиторий есть уже в системе,
хотя, он еще более косячный.
Нет нормального скриншотера для Линукса вообще

---

## Drawing (Paint)

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

В автозагрузку добавить комманды:

```
conky -c /home/dedared/.Conky/default/conky.conf

.Conky/revolutionary_clocks/rev_midi/start_conky.sh
```

Шрифты для часов положить в папку: ~/home/.fonts   
Если папки такой нет, создать.

---

## Подключить поддержку тем GTK для QT приложений

```
sudo apt install qt5-style-plugins qt5ct
```

В файле:

```
/etc/profile.d/qt-style-override.sh
```

удалить строку:

```
export QT_STYLE_OVERRIDE=adwaita
```
В файле

```
/etc/profile.d/qt-qpa-platformtheme.sh
```

должно быть так:

```
export QT_QPA_PLATFORMTHEME=qt5ct
```

---

Исправление кракозябр в Линуксе

1. Проверяем локали:
locale -a

2. Если там не будет ru_RU.cp1251 то:

sudo io.elementary.code /var/lib/locales/supported.d/ru

Вместо кода любой текстовик, откроется блокнот и там (если нет) добавить:

ru_RU.CP1251 CP1251
ru_RU.KOI8-R KOI8-R

3. Сохранить и после выполнить:

sudo locale-gen

Должно снизу вылезти такое:

Generating locales...
  en_US.UTF-8... done
  ru_RU.CP1251... done
  ru_RU.KOI8-R... done
  ru_RU.UTF-8... up-to-date
  ru_UA.UTF-8... up-to-date
Generation complete.

4. Затем проверить снова:

locale -a

Должно быть примерно так:

en_US.utf8
POSIX
ru_RU.cp1251
ru_RU.koi8r
ru_RU.utf8
ru_UA.utf8

=======================================

