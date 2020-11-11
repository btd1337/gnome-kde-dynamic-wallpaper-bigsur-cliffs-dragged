# Time based GNOME macOS Bigsur Cliffs Dragged wallpaper with real scheludes</br>& Azimuth Elevation based / Time based KDE macOS Bigsur Cliffs Dragged wallpaper

Bigsur Cliffs Dragged dynamic wallpaper is 8 based images wallpaper.</br>
Bigsur Cliffs Dragged dynamic wallpaper is useable as Gnome/KDE background which changes during the day/night.</br>
For Gnome, it's a timed based wallpaper with real scheludes with 90 minutes transitions.</br>
For KDE, the 1st version is a Azimuth Elevation wallpaper based on real Azimuth Elevation of the Sun for the Catalina island on 21/06/2019.</br>
For KDE, the 2nd version is  a timed based wallpaper with real scheludes.</br></br>


<p align="center">
  <img width="478" height="326" src="gnome-kde-dynamic-wallpaper-catalina.gif">
</p>


# Dependencies
* Gnome
  * gnome-shell
  * gnome-backgrounds
* KDE
  * plasma5-wallpapers-dynamic for Archlinux 
  * or [home: KAMiKAZOW:KDE](https://software.opensuse.org//download.html?project=home%3AKAMiKAZOW%3AKDE&package=plasma5-dynamic-wallpaper) for Opensuze
  - or [GitHub: zzag/dynamic-wallpaper](https://github.com/zzag/dynamic-wallpaper) for others distros

# Parameters
## Gnome
None but you must sync your system clock time (presented both in local time and UTC) as well as the RTC (hardware clock).
## KDE
Select "Dynamic" wallpaper type, put your real coordinates and your timer for the solar version.
You must sync your system clock time (presented both in local time and UTC) as well as the RTC (hardware clock) for the timed version.


# Installation
## Users of Arch Linux
Arch Linux users  need only clone and build this repository.

```
git clone https://github.com/btd1337/gnome-kde-bigsur-cliffs-dragged-dynamic-wallpaper.git
cd gnome-kde-bigsur-cliffs-dragged-dynamic-wallpaper
makepkg -si
```

## Users of other distros
Users of other distros can manually complete these 7 steps:

1) Copy `catalina` directory from this repo  to `/usr/share/dynamicwallpapers/bigsur-cliffs-dragged-solar/contents/images` and make it readable by running the following as the root user:
```
mkdir -p /usr/share/dynamicwallpapers/bigsur-cliffs-dragged-solar/contents/images && 
cp catalina/* /usr/share/dynamicwallpapers/bigsur-cliffs-dragged-solar/contents/images && 
chmod 755 /usr/share/dynamicwallpapers/bigsur-cliffs-dragged-solar/contents/images && 
chmod 644 /usr/share/dynamicwallpapers/bigsur-cliffs-dragged-solar/contents/images/*
```

2) Create `/usr/share/dynamicwallpapers/bigsur-cliffs-dragged-timed/contents/images` and make it readable by running the following as the root user:
```
mkdir -p /usr/share/dynamicwallpapers/bigsur-cliffs-dragged-timed/contents && 
chmod 755 /usr/share/dynamicwallpapers/bigsur-cliffs-dragged-timed/contents  && 
ln -s /usr/share/dynamicwallpapers/bigsur-cliffs-dragged-solar/contents/images /usr/share/dynamicwallpapers/bigsur-cliffs-dragged-timed/contents/images 
```


3) Link `catalina` directory from `/usr/share/dynamicwallpapers` to `/usr/share/backgrounds/macOS` by running the following as the root user:
```
mkdir -p /usr/share/backgrounds/macOS &&
ln -s /usr/share/dynamicwallpapers/bigsur-cliffs-dragged-solar/contents/images /usr/share/backgrounds/macOS/bigsur-cliffs-dragged
```

4) Copy `bigsur-cliffs-dragged-solar.json` from this repo  to `/usr/share/dynamicwallpapers/bigsur-cliffs-dragged-solar/metadata.json` and make it readable by running the following as the root user:
```
cp bigsur-cliffs-dragged-solar.json /usr/share/dynamicwallpapers/catalina-solar/metadata.json && 
chmod 644 /usr/share/dynamicwallpapers/catalina-solar/metadata.json
```

5) Copy `bigsur-cliffs-dragged-timed.json` from this repo  to `/usr/share/dynamicwallpapers/bigsur-cliffs-dragged-timed/metadata.json` and make it readable by running the following as the root user:
```
cp bigsur-cliffs-dragged-timed.json /usr/share/dynamicwallpapers/bigsur-cliffs-dragged-timed/metadata.json && 
chmod 644 /usr/share/dynamicwallpapers/bigsur-cliffs-dragged-timed/metadata.json
```

6) Copy `bigsur-cliffs-dragged-timed.xml` from this repo  to `/usr/share/backgrounds/macOS` and make it readable by running the following as the root user:
```
cp bigsur-cliffs-dragged-timed.xml /usr/share/backgrounds/macOS/bigsur-cliffs-dragged-timed.xml && 
chmod 644 /usr/share/backgrounds/macOS/bigsur-cliffs-dragged-timed.xml
```

7) Copy `bigsur-cliffs-dragged.xml` from this repo  to `/usr/share/gnome-background-properties` and make it readable by running the following as the root user:
```
mkdir -p /usr/share/gnome-background-properties && 
cp bigsur-cliffs-dragged.xml /usr/share/gnome-background-properties/bigsur-cliffs-dragged.xml && 
chmod 644 /usr/share/gnome-background-properties/bigsur-cliffs-dragged.xml
```
