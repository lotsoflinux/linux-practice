# Chapter 5 — Networking

This chapter shows basic networking commands and how to inspect network interfaces.

## ✅ Exercises
- Check network interfaces: `ip addr`, `ifconfig` (if installed)
- Test connectivity: `ping 8.8.8.8`, `curl https://example.com`
- Check listening ports: `ss -tulpn` or `netstat -tulpn`
- Download a file: `curl -LO https://example.com`

## 📋 Example commands
```bash
cd /workspace/05-networking
ip addr
ping -c 3 8.8.8.8
curl -I https://example.com
ss -tulpn | head
``` 

## 📝 Files in this folder
- `net-scan.sh` — dummy script to demonstrate scanning commands.

---

## 🧪 Try it in a real Linux environment (WSL/Docker)
```bash
cd /workspace/05-networking
bash net-scan.sh
```