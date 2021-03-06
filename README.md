# MacGesture 2 ![tweet](https://img.shields.io/twitter/url/https/github.com/CodeFalling/MacGesture.svg?style=social)

[Chinese version 中文版](https://github.com/MacGesture/MacGesture/blob/release/README_zh-Hans.md)

![logo](logo.png)

Configurable global mouse gesture for macOS.

** Multiple issues are reported in Sierra. Please file issues and roll back to earlier versions before we fix all of them. **

You can read this README in About section.

# Feature

- Global mouse gesture recognition

- Filter app by their bundle name (as a consequence, the apps without bundle identifiers are skipped and filtering by process name is on the road map)

- Configure and send shortcut by gesture

# Preview

![Preview](https://cloud.githubusercontent.com/assets/5436704/14278725/bb126d36-fb5b-11e5-9fe8-5990ea4c1c28.gif)

# The format of gesture

| Gesture | Acronym |
|---------|---------|
| Left    | L       |
| Up      | U       |
| Right   | R       |
| Down    | D       |
| Mouse L | Z       |
| Wheel U | u       |
| Wheel D | d       |

Gesture can contain wildcard matching('?' and '*').

The first rule matching will take effect.

Z is the acronym of pinyin of '左' which means 'left' in English.
So to distinguish 'clicking the left mouse' from 'dragging your mouse left-ward',
we chose 'Z'.

Wheel directions may vary according to system configurations or some system tweaks (Karabiner's Reverse Vertical Scrolling, for example).

# Q&A

Feel free to open issue

# Download

Download the latest zip from https://github.com/MacGesture/MacGesture/releases

# Tips

* If you want to achieve something like this:

Right click, drag upwards, then every 'u' triggers a 'Next Tab', every 'd' triggers a 'Prev Tab', without releasing right mouse.

Then, create a rule like this:

| Gesture | Filter             | Action             | Note       | Trigger on every match |
|---------|--------------------|--------------------|------------|------------------------|
|U*d      | \*safari\|\*chrome | "shift-command-\]" | "Next Tab" | Checked                |
|U*u      | \*safari\|\*chrome | "shift-command-\[" | "Prev Tab" | Checked                |

* If you want to export and import MacGesture preferences:

Recommended way:

Use the buttons 'Import' and 'Export' in the ‘General' Panel.

Geek-ish way: (the underlying way as well)

Open a terminal, Do this in your old computer:

``` shell
defaults read com.codefalling.MacGesture backup.plist
```

And then copy that file to your new computer, then:

``` shell
defaults import com.codefalling.MacGesture backup.plist
```

You should get your preferences back now. If is doesn't, file an issue on the project home.

# License

This project is under GNU General Public License.

Icon is designed by [DanRabbit](http://www.iconarchive.com/artist/danrabbit.html) under [GNU General Public License](https://en.wikipedia.org/wiki/GNU_General_Public_License).

# Contributor

- [CodeFalling](https://github.com/codefalling)
- [jiegec](https://github.com/jiegec)
- [zhangciwu](https://github.com/zhangciwu)

# Discuss

讨论可以加入qq群：498035635 (You can join the discussion in QQ Group 498035635).
