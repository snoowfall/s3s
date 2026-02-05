<img width="230" height="169" alt="sss" src="https://github.com/user-attachments/assets/9e435e92-ed76-45f3-9a04-426fd708291c" />

# S³ / SSS

Wrote this simple tool for switching the screen off and on after a keypress. It's mainly aimed at Hyprland, as in it's current state it will try running
```
hyprctl dispatch dpms off
```
(and dpms on respectively).

## Editing to your needs

If you're not using Hyprland, the tool is pointless without changing lines 40 & 54 to your respective dpms dispatchers.

## Building

#### What you'll need:
- gcc
- libinput
- libudev
- pkg-config

That's it. ```libinput``` comes preinstalled when using Hyprland.

Run:
```
git clone https://github.com/snoowfall/sss.git
```

```
cd ./sss/
```

```
gcc sss.c -o sss $(pkg-config --cflags --libs libinput) -ludev
```
You should now see ```sss``` in that folder. Copy it to ```/bin/``` (or similar) to use it directly via the command line.
