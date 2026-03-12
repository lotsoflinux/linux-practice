# Chapter 4 — Package Management

Package management is how software is installed, updated, and removed.

## ✅ Exercises
- Update package cache: `sudo apt update` (Debian/Ubuntu) or `sudo yum check-update` (RHEL/CentOS).
- Install a package: `sudo apt install -y curl`.
- Remove a package: `sudo apt remove -y curl`.
- Query installed packages: `dpkg -l | grep curl`.

> 🔥 Note: In Docker containers, you may need to run `apt update` before installing packages.

## 📋 Example commands
```bash
sudo apt update
sudo apt install -y curl
curl --version
sudo apt remove -y curl
```

## 📝 Files in this folder
- `pkg-list.txt` — dummy list representing installed packages.

---

## 🧪 Try it in a real Linux environment (WSL/Docker)
```bash
cd /workspace/04-package-management
cat pkg-list.txt
sudo apt update
```
