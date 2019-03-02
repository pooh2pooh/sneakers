# My experience KDE on Manjaro
## Some Details
+ **OS:** [Manjaro](https://manjaro.org)
+ **Wallpaper:** [Mojave Night](https://hdqwalls.com/wallpaper/3840x2160/macos-mojave-night-mode-stock)
+ **KDE Shell:** Kvantum
+ **Kvantum Theme:** [Mojave Dark](https://store.kde.org/p/1252328/)
+ **Plasma Theme:** [Breeze Transparent Dark](https://store.kde.org/p/1170816/)
+ **GTK2/3 Theme:** Breath
+ **KDE Window Decorations:** [Mojave Dark Aurorae](https://www.opendesktop.org/p/1252329/)
+ **Icon Theme:** [Mojave CT](https://store.kde.org/p/1210856/)
+ **Top Bar and Dock:** KDE (default widget)

## Latest Preview


## Tips / Notes
**Attention!!!** 
I use small power hardware, my settings for `1 CPU 2Ghz, 2Gb RAM and 120 Gb SSD`
+ Use [Zswap](https://wiki.archlinux.org/index.php/Zswap) and 4Gb swap partition
+ My config `/etc/sysctl.d/99-sysctl.conf` [see kernel docs, for help](https://www.kernel.org/doc/Documentation/sysctl/vm.txt)
```
vm.swappiness = 30
vm.vfs_cache_pressure = 50
vm.dirty_background_ratio = 10
vm.dirty_ratio = 40
vm.dirty_writeback_centisecs = 500
```
+ I rarely use debugging information. `~/.bash_profile` add:
```
QT_LOGGING_RULES='*=false'
export QT_LOGGING_RULES
```
+ Use `kdebugdialog5` terminal command, disable any debugging information.
+ Edit `/etc/systemd/journald.conf` [see systemd docs, for help](https://www.freedesktop.org/software/systemd/man/journald.conf)
```
Storage=volatile
RuntimeMaxUse=10M
```
+ You can open an issue if you have any questions / problems.

