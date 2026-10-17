# Persona Shell for Zorin OS

One command to get [Persona-Quickshell](https://github.com/Yujonpradhananga/Persona-Quickshell)
(the Persona 3 Reload style desktop by Yujon Pradhananga) on Zorin OS.

It adds a new choice, **Persona Shell (Hyprland)**, to the login screen. Your normal Zorin desktop is not changed.

## Install

Open a terminal (Ctrl+Alt+T), paste this, press Enter, and type your password when asked:

```bash
bash <(curl -fsSL https://raw.githubusercontent.com/JupiterianSoul/persona-shell-zorin/main/install.sh)
```

It takes 10–30 minutes (it downloads a few GB). When it says **All done!**:

1. Log out.
2. On the login screen, click your name, then the **gear icon** at the bottom right.
3. Choose **Persona Shell (Hyprland)** and log in.

A file with all the keys is put on your desktop. The main ones ("Super" is the Windows key):

| Keys | Does |
|---|---|
| Super + Space | search and open apps |
| Super + Enter | terminal |
| Super + E | files |
| Alt + F4 | close window |
| Super + Shift + E | log out |

## Going back to normal Zorin

Log out, and pick **Zorin Desktop** with the gear icon instead.

## Update or remove

From a terminal in normal Zorin:

- `persona-shell-update`: update Hyprland and the shell (also after an NVIDIA driver update)
- `persona-shell-uninstall`: remove everything this installed

## If something goes wrong

Pick **Zorin Desktop** at login, then send these files to whoever gave you the link:
`~/.local/share/persona-shell/install.log` and `~/.local/share/persona-shell/session.log`.

## What it does

Zorin's own packages are too old for this shell, so Hyprland and Quickshell come from
[Nix](https://nixos.org), with [nixGL](https://github.com/nix-community/nixGL) for graphics drivers.
The shell is pinned to a tested commit and slightly patched: the Cava visualizer is removed (it needs a hand-built
plugin), and apps opened from its launcher get a clean environment so normal Zorin apps work.
