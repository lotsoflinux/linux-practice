# Chapter 10 — Troubleshooting & Tools

This chapter collects useful tools and techniques for diagnosing issues.

## ✅ Exercises
- Read kernel messages: `dmesg | tail`
- Use `strace` to trace a command (may require installing `strace`):
  ```bash
  strace -o /tmp/ls.strace ls
  ```
- View sysctl settings: `sysctl -a | head`
- Test network resolution: `dig +short example.com` (requires `dnsutils`/`bind-utils`).

## 📋 Example commands
```bash
cd /workspace/10-troubleshooting-tools
dmesg | tail
sysctl -a | head
``` 

## 📝 Files in this folder
- `sysctl.conf` — example sysctl config file.

---

## 🧪 Try it in a real Linux environment (WSL/Docker)
```bash
cd /workspace/10-troubleshooting-tools
cat sysctl.conf
```