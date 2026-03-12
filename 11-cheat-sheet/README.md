# Chapter 11 — Linux Cheat Sheet

This chapter is a quick-reference cheat sheet covering the most common Linux commands you'll use daily. Use this folder as a go-to reference when you're practicing other chapters.

## 📌 Common patterns
- Use `man <command>` (manual) or `--help` for usage info.
- Use pipes `|` to connect commands.
- Use `&&` to chain commands only if the previous one succeeded.
- Use `>` / `>>` to redirect output to files.

---

## 📁 Files & Directories
- List files (show hidden): `ls -la`
- Show current directory: `pwd`
- Change directory: `cd /path/to/dir`
- Create dir: `mkdir -p /tmp/mydir`
- Copy/move/remove: `cp`, `mv`, `rm -rf`
- Show file contents: `cat`, `less`, `head`, `tail`

> Example:
```bash
cd /workspace/01-shell-basics
ls -la
cat example.txt
tail -n 5 example.txt
```

---

## 🧩 Searching & Text Processing
- Find files: `find . -name "*.log"`
- Search inside files: `grep -R "ERROR" .`
- Extended regex search: `grep -E "foo|bar" file.txt` or `egrep "foo|bar" file.txt`
- Stream editing: `sed -n '1,5p' file.txt` or `sed 's/foo/bar/g' file.txt`
- Field processing: `awk '{print $1}' file.txt`
- Count words/lines: `wc -l file.txt`
- Sort/uniq: `sort`, `uniq -c`
- View columns: `cut -d',' -f1`

> Example:
```bash
grep -i "error" -R . | head
sed -n '1,5p' 01-shell-basics/example.txt
awk '{print $1}' 02-filesystem/sample.log | head
``` 

---

## 🧠 Process & System
- List processes: `ps aux`, `ps -ef`
- Show resource usage: `top`, `htop` (if installed)
- Kill by PID/name: `kill <pid>`, `pkill -f <name>`
- Check load: `uptime`
- Disk usage: `df -h`, `du -sh *`

> Example:
```bash
ps aux | grep bash
df -h
du -sh ./* | sort -h | head
```

---

## 🌐 Networking
- Check interfaces: `ip addr`, `ip route`
- Test connectivity: `ping -c 3 8.8.8.8`
- HTTP request: `curl -I https://example.com`
- DNS lookup: `dig +short example.com` (if installed)
- List listening ports: `ss -tulpn`

> Example:
```bash
ip addr
curl -I https://example.com
ss -tulpn | head
```

---

## 🧰 Package Management (Debian/Ubuntu)
- Update indexes: `sudo apt update`
- Install/remove: `sudo apt install -y <pkg>`, `sudo apt remove -y <pkg>`
- Search packages: `apt search <term>`
- Show package info: `apt show <pkg>`

> Example:
```bash
sudo apt update
sudo apt install -y curl
curl --version
```

---

## 🧪 Shell Scripting Basics
- Make executable: `chmod +x script.sh`
- Run: `./script.sh` or `bash script.sh`
- Use `set -euo pipefail` for safer scripts.
- Common patterns:
  - Variables: `name="value"`
  - Conditionals: `if [[ ... ]]; then ... fi`
  - Loops: `for x in *; do ...; done`

---

## 🔍 Help & Documentation
- Manual pages: `man <command>`
- Show help: `<command> --help`
- Search man pages: `apropos <topic>`

---

## 🧪 Try it in a real Linux environment (WSL/Docker)
```bash
cd /workspace/11-cheat-sheet
cat README.md
man ls
grep -R "TODO" .. | head
```
