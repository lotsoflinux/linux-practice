# Chapter 12 — Advanced Topics

This chapter goes deeper into advanced Linux concepts that are essential for real-world operations, debugging, and automation.

## 🔥 Advanced topics included
- **Systemd & services** (unit files, targets, journal)
- **Kernel tuning & sysctl** (performance tuning, network settings)
- **cgroups & namespaces** (resource isolation, containers)
- **SELinux/AppArmor basics** (security enforcement)
- **Networking deep dives** (iptables/nftables, routing, tunnels)
- **Performance analysis** (perf, strace, eBPF basics)
- **Logging pipelines** (rsyslog, logrotate, journald)
- **Automation & configuration management** (Ansible, cron, systemd timers)
- **Storage & filesystems** (LVM, RAID, quotas, mounting)

---

## ✅ Exercises (pick a path)
- Inspect systemd units: `systemctl list-units --type=service`
- Explore journal: `journalctl -xe`
- View kernel parameters: `sysctl -a | grep -E "(net|fs|vm)"`
- Use `perf stat` on a command: `perf stat -d sleep 1`
- Trace a command with strace: `strace -o /tmp/ls.strace ls`
- Inspect cgroups: `cat /sys/fs/cgroup/unified/cgroup.controllers`
- View current iptables rules: `sudo iptables -L -n -v`
- Create a simple cron job: `echo "* * * * * date >> /tmp/cron-test.log" | crontab -`

---

## 📝 Files in this folder
- `systemd-example.service` — sample systemd service unit.
- `sysctl-optim.conf` — example sysctl settings for performance.
- `cron-example.txt` — example crontab entry.

---

## 🧪 Try it in a real Linux environment (WSL/Docker)
```bash
cd /workspace/12-advanced
cat systemd-example.service
sudo sysctl -p sysctl-optim.conf
```