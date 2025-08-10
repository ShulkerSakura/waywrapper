# waywrapper

🔧 Enable Wayland for Electron/Chromium apps on Linux.

Many apps (Edge, VS Code, etc.) still run on X11 by default — causing blurry text, lag, or rendering bugs.  
`waywrapper` fixes that by adding `--ozone-platform-hint=wayland` safely.

---

## ✅ Quick Start

```bash
# Install
sudo curl -L https://git.io/waywrapper -o /usr/local/bin/waywrapper
sudo chmod +x /usr/local/bin/waywrapper

# Wrap Edge (example)
sudo waywrapper --set-binary-path /opt/microsoft/msedge/msedge
sudo waywrapper --set-binary-path /opt/microsoft/msedge/microsoft-edge
sudo waywrapper --update
```
Now Edge runs natively on Wayland.

---

## 🚀 Commands

| Command | Description |
|--------|-------------|
| `--set-binary-path /path` | Add binary to wrap |
| `--update` | Apply wrapper (backup → add script) |
| `--update --dry-run` | Preview changes |
| `--update --force` | Rebuild existing wrappers |
| `--list` | Show registered binaries |
| `--remove-binary-path /path` | Remove from list |
| `--help` | Show usage |
| `--version` | Show version |
> ⚠️ Run all write commands with `sudo`.

---

## ⚠️ Important: VS Code Warning

Do Not Patch VS Code, it doesn't need to patch and patch will causes bad option error.  
