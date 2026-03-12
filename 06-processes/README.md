# Chapter 6 — Processes & System Resources

Learn how to inspect running processes, resource usage, and manage jobs.

## ✅ Exercises
- List processes: `ps aux`, `ps -ef`
- View real-time CPU/memory: `top` or `htop` (if installed)
- Search for a process: `ps aux | grep sshd`
- Kill a process: `kill <pid>`, `pkill -f <name>`
- Check load averages: `uptime`

## 📋 Example commands
```bash
cd /workspace/06-processes
ps aux | head
top -b -n 1 | head -n 20
uptime
``` 

## 📝 Files in this folder
- `proc-info.txt` — dummy file describing /proc usage.

---

## 🧪 Try it in a real Linux environment (WSL/Docker)
```bash
cd /workspace/06-processes
cat proc-info.txt
ps aux | grep -E "(bash|ssh|python)" | head
```