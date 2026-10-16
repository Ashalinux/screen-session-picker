<div align="center">

# Screen Session Picker

**An interactive terminal menu to list and attach to your GNU screen sessions.**

![Bash](https://img.shields.io/badge/Bash-4%2B-4EAA25?logo=gnubash&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-only-FCC624?logo=linux&logoColor=black)
![License](https://img.shields.io/badge/license-MIT-green)

</div>

No more `screen -ls` and copying PIDs: run `screens`, pick a session with the arrow keys and you're attached. Detach (`Ctrl+A`, `D`) and you're right back in the menu.

## ✨ Features

- Lists all running screen sessions, sorted by PID
- Arrow-key navigation via `dialog`
- Returns to the menu after detaching
- Waits gracefully when no sessions are running
- Optional custom `dialogrc` color theme

## 📦 Installation

```bash
sudo apt install screen dialog
sudo cp bin/screens /usr/local/bin/screens
sudo chmod +x /usr/local/bin/screens
# optional theme
sudo cp etc/dialogrc /etc/dialogrc
```

## 🚀 Usage

```bash
screens
```

Press `Ctrl+C` to quit.

> ℹ️ The script reads sessions from `/var/run/screen/S-root/`, so it's meant to run as **root**. Change the path in `bin/screens` for other users.

## 📄 License

Released under the [MIT License](LICENSE).
