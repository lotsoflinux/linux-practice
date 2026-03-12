# Chapter 2 — Filesystem & Paths

This chapter covers filesystem navigation, creating/deleting files and directories, and understanding paths.

## ✅ Exercises
- Move between directories: `cd ..`, `cd /`, `cd ~/`
- Create directories: `mkdir -p data/logs`
- Create files: `touch sample.log`
- Copy/move files: `cp`, `mv`
- Remove files/directories: `rm`, `rm -rf`
- Explore with `find` and `tree` (if installed).

## 📋 Example commands
```bash
pwd
ls -la
mkdir -p data/logs
cp sample.log data/logs/
find . -name "*.log"
``` 

## 📝 Files in this folder
- `sample.log` — dummy log file.
- `data/` — sample subfolder for nested files.

---

## 🧪 Try it in a real Linux environment (WSL/Docker)
```bash
cd /workspace/02-filesystem
ls -la
cat sample.log
mkdir -p data/logs
cp sample.log data/logs/
```