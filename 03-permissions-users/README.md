# Chapter 3 — Permissions & Users

This chapter explains Unix permissions, ownership, and basic user/group concepts.

## ✅ Exercises
- Check file permissions: `ls -l`
- Change permissions: `chmod 644 file.txt`, `chmod u+x script.sh`
- Change ownership (requires sudo): `sudo chown $(whoami):$(whoami) file.txt`
- See current user: `whoami`, `id`
- List groups: `groups`

## 📋 Example commands
```bash
cd /workspace/03-permissions-users
ls -l
chmod 700 secret.sh
chmod 644 info.txt
ls -l
```

## 📝 Files in this folder
- `info.txt` — file for permission changes.
- `secret.sh` — dummy script showing execute permission.

---

## 🧪 Try it in a real Linux environment (WSL/Docker)
```bash
cd /workspace/03-permissions-users
ls -l
chmod +x secret.sh
./secret.sh
```