# GNOME Dynamic Wallpapers

In GNOME you can use dynamic wallpapers. My favourites are those, which change with the time of day.

All you need for a dynamic wallpaper are two or more pictures and an xml-file, that describes the transition-type and timings. The XML can be created with a GUI app.

## Create your own

GUI for creating Wallpapers: [Dynamic Wallpaper Editor](https://github.com/maoschanz/dynamic-wallpaper-editor)

recommended: place xml and pictures to:
- `usr/share/backgrounds/yourwallpaper/` (all users)
- `~/.local/share/backgrounds/yourwallpaper/` (just for you)

## Add them to Wallpaper-Settings GUI

create new xml file:
- `usr/share/gnome-background-properties/yourwallpaper.xml` (all users)
- `~/.local/share/gnome-background-properties/yourwallpaper.xml` (just for you)

xml file:
```xml
<?xml version="1.0"?>
<!DOCTYPE wallpapers SYSTEM "gnome-wp-list.dtd">
<wallpapers>
  <wallpaper deleted="false">
    <name>YOURWALLPAPERNAME</name>
    <filename>/path/to/your/wallpaper.xml</filename>
    <options>zoom</options>
  </wallpaper>
</wallpapers>
```

## Dynamic Wallpapers from the community

https://github.com/saint-13/Linux_Dynamic_Wallpapers

