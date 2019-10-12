# wmakerconf-2-12-2.deb

[[wmakerconf]](https://sourceforge.net/projects/wmakerconf/) is a GTK+ based configuration tool for Window Maker
 Interactive graphical configuration utility for Window Maker. It
 permits configuration of Window Maker using a mouse driven point and
 click interface, avoiding direct manual editing of its configuration
 files.  This tool is similar in spirit to WPrefs.app, but is instead
 written using the GTK+ toolkit.

Unfortunately, it has been unsupported for a decade or more. wmakerconf relies on 
libwraster.so.3

In the attached file, I edited the deb to accept libwraster6 as a dependency, so that it will install. However, it really does need libwraster3 to run.

Thus, in your debian system, you must either somehow figure out how to install libwraster.so.3, or else:

```
sudo ln -s /usr/lib/x86_64-linux-gnu/libwraster.so.6.0.0 /usr/lib/x86_64-linux-gnu/libwraster.so.3
```

Download the attached files. Install with:

```
sudo dpkt -i wmakerconf-data_2.12-1_all.deb && sudo dpkg -i wmakerconf-2-12-2.deb
```

This is a dirty hack, but it works on my system. It may break yours, so this project comes with no guarantees or warranty.
