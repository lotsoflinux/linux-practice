# linux-practice

A hands‑on project workspace for practicing Linux skills on a Windows machine.

## 🚀 Goal
This repo is designed to help you learn and practice the most important Linux topics while working from Windows. You can use **WSL2**, **Docker Desktop (Linux containers)**, or any Linux VM, and follow along with the chapters below.

---

## 🧰 Setup (Windows → Linux)

### Option A — WSL2 (recommended)
1. Install WSL:
   - Open PowerShell as Administrator and run:
     ```powershell
     wsl --install
     wsl --set-default-version 2
     ```
2. Install a Linux distribution (Ubuntu is common):
   ```powershell
   wsl --install -d ubuntu
   ```
3. Launch the distro (from Start menu) and create a user.
4. From PowerShell, open the repo in WSL:
   ```powershell
   wsl -d ubuntu -- cd /mnt/d/linux-practice/linux-practice && bash
   ```

✅ Once inside WSL, you can run all standard Linux commands and work in this repo.

### Option B — Docker Desktop (Linux containers)
1. Install Docker Desktop for Windows: https://www.docker.com/get-started
2. Ensure **Use the WSL 2 based engine** is enabled in Settings → General.
3. Open **PowerShell** and run a temporary Linux container shell:
   ```powershell
   docker run --rm -it -v d:/linux-practice/linux-practice:/workspace -w /workspace ubuntu:24.04 bash
   ```
4. Inside the container, you can run Linux commands and explore the repo in `/workspace`.

> ⚠️ Note: Files created in the container persist in the mounted folder (`/workspace`) on your Windows disk.

### Option C — Other ways
- Use **Git Bash** for basic shell commands (limited Linux features).
- Use a full Linux VM (VirtualBox, Hyper-V, VMware).

---

## 📚 Chapters (11 topics)
Each chapter folder contains exercises, example files, and commands you can run locally.

1. **Shell Basics** (`01-shell-basics/`)
2. **Filesystem & Paths** (`02-filesystem/`)
3. **Permissions & Users** (`03-permissions-users/`)
4. **Package Management** (`04-package-management/`)
5. **Networking** (`05-networking/`)
6. **Processes & System Resources** (`06-processes/`)
7. **Logs & Monitoring** (`07-logs-monitoring/`)
8. **Shell Scripting** (`08-scripting/`)
9. **Containers & Docker** (`09-containers-docker/`)
10. **Troubleshooting & Tools** (`10-troubleshooting-tools/`)
11. **Linux Cheat Sheet** (`11-cheat-sheet/`)

---

## ✅ How to use this repo
1. Open a Linux shell (WSL/Docker).  
2. `cd /workspace` (or the path where this repo lives inside your Linux environment).  
3. Browse the chapter folders and read their `README.md` files.  
4. Run example commands and inspect the dummy files (logs, configs, scripts).

---

## 🔍 Quick reference (examples)
- List files: `ls -la`  
- Read a file: `cat 01-shell-basics/example.txt`  
- Search text: `grep -R "TODO" .`  
- Find large files: `du -sh * | sort -h`  
- Check disk usage: `df -h`  
- Show process tree: `ps aux --forest`  
- Launch interactive shell in Docker: `docker run --rm -it -v $(pwd):/workspace -w /workspace ubuntu:24.04 bash`

---

## 🧩 Tips
- If you are using WSL, install the Windows Terminal (recommended) and set up a profile for your distro.
- If you use Docker, you can run the same commands inside the container shell and return to Windows when done.
- Keep this repo synced to avoid losing changes when switching between environments.