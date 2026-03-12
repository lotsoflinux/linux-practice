# Chapter 7 — Logs & Monitoring

Learn where Linux stores logs and how to search them.

## ✅ Exercises
- View system logs: `journalctl -xe` (systemd) or `tail -n 50 /var/log/syslog`
- Follow a log file: `tail -f /var/log/messages`
- Search logs: `grep -i error /var/log/syslog`
- Use `dmesg` to view kernel messages.

## 📋 Example commands
```bash
cd /workspace/07-logs-monitoring
cat system.log | head
grep "ERROR" system.log
``` 

## 📝 Files in this folder
- `system.log` — dummy system log file.

---

## 🧪 Try it in a real Linux environment (WSL/Docker)
```bash
cd /workspace/07-logs-monitoring
grep -i "error" system.log
```