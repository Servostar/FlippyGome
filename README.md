# FlippyGome
Hacky solution for getting auto screen rotation to work under GNOME-Wayland.
It works by pressing a key combination in the background, rotating the screen.
The system service detects changes in the sensor using `iio-sensor-proxy`, calculates the amount of keypresses
and then executes the strokes with `ydotool`.

## Requirements
- iio-sensor-proxy
- ydotool

Install ydotool for RHEL/CentOS/Fedora:
```bash
sudo dnf install ydotool
```

## Install
Run
```bash
gsettings set org.gnome.mutter.keybindings rotate-monitor ['XF86RotateWindows', '<Control>F8']
```
in order to install the keybind required to rotate the screen itself.
Clone this repository.
Then run `install.sh`.
Done.
