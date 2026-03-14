# 🐧 Linux Command-Line Cheat Sheet
Complete all-in-one reference for freshers and new joiners.  
Created for the **lotsoflinux** GitHub community.

## 1. Navigation & Help
pwd  
ls -lah  
cd ~  
cd ..  
cd /etc  
mkdir mydir  
mkdir -p parent/child  
rmdir emptydir  
command --help  
man command  
whatis command  
apropos keyword  

## 2. Files & Content
touch file.txt  
cp source dest  
cp -r dir dir_copy  
mv old new  
rm file  
rm -rf dir  
cat file  
tac file  
nl file  
less file  
head -n 20 file  
tail -n 50 file  
tail -f /var/log/syslog  

## 3. Text Processing (grep / sed / awk / sort / uniq / cut / tr)
grep -i "error" app.log  
grep -Rin "pattern" .  
sed -i 's/old/new/g' file  
sed -n '10,20p' file  
awk '{print $1,$3}' file  
awk -F, '$3 > 100' data.csv  
sort file  
sort -n numbers.txt  
sort file | uniq  
sort file | uniq -c | sort -nr  
cut -d, -f1,3 data.csv  
tr '[:lower:]' '[:upper:]' < in.txt  
find . -name "*.tmp" -print0 | xargs -0 rm -f  

## 4. Search (find / locate)
locate sshd_config  
find /var -name "*.log"  
find . -type f -size +100M  
find . -mtime -1  
find . -name "*.sh" -exec chmod +x {} \;  

## 5. Permissions & Ownership
ls -l  
chmod 644 file  
chmod +x script.sh  
chmod -R 755 dir  
sudo chown user:group file  
sudo chown -R www-data:www-data /var/www  
chmod u+s binfile  
chmod g+s shareddir  
chmod +t /tmp  

## 6. Users & Groups
whoami  
id  
who  
w  
last  
sudo adduser alice  
sudo passwd alice  
sudo groupadd devs  
sudo usermod -aG devs alice  
sudo userdel -r alice  
sudo groupdel devs  

## 7. Processes & Jobs
ps aux  
ps -ef  
pstree -p  
top  
kill PID  
kill -9 PID  
pkill -f pattern  
killall process  
command &  
jobs  
fg %1  
bg %1  
disown %1  

## 8. System Info & Hardware
uname -a  
cat /etc/os-release  
lscpu  
free -h  
vmstat 1  
lspci  
lsusb  
lsblk  
lshw -short  
uptime  
hostnamectl  
timedatectl  

## 9. Disk, Filesystems & I/O
df -h  
du -sh .  
du -sh * | sort -h  
mount  
sudo mount /dev/sdb1 /mnt  
sudo umount /mnt  
sudo fsck /dev/sdb1  
sudo mkfs.ext4 /dev/sdb1  
sudo mkswap /dev/sdb2  
swapon --show  
iostat 1  

## 10. Networking
ip addr  
ip route  
ip link  
hostname -I  
ping -c 4 8.8.8.8  
traceroute example.com  
mtr example.com  
dig example.com  
nslookup example.com  
ss -tulpen  
sudo lsof -i -P -n | grep LISTEN  
curl -I https://example.com  
wget https://example.com/file.tar.gz  

## 11. Package Management (APT / DNF / Pacman)
### APT (Debian/Ubuntu)
sudo apt update  
sudo apt upgrade  
sudo apt install pkg  
sudo apt remove pkg  
apt list --installed | grep name  
### DNF/YUM (RHEL/Fedora)
sudo dnf update  
sudo dnf install pkg  
sudo dnf remove pkg  
dnf list installed | grep name  
### Pacman (Arch)
sudo pacman -Syu  
sudo pacman -S pkg  
sudo pacman -R pkg  
pacman -Qi pkg  

## 12. Services (systemd)
systemctl status nginx  
sudo systemctl start nginx  
sudo systemctl stop nginx  
sudo systemctl restart nginx  
sudo systemctl enable nginx  
sudo systemctl disable nginx  
journalctl -u nginx  

## 13. Logs
journalctl -b  
journalctl -k  
journalctl -u ssh  
journalctl --since "1 hour ago"  
tail -f /var/log/syslog  
tail -f /var/log/messages  
less /var/log/auth.log  

## 14. Compression / Archive
tar -czf archive.tar.gz dir  
tar -xzf archive.tar.gz  
tar -tzf archive.tar.gz  
zip -r archive.zip dir  
unzip archive.zip  
gzip file  
gunzip file.gz  
bzip2 file  
bunzip2 file.bz2  
xz file  
unxz file.xz  

## 15. Shell & Environment
export PATH="$HOME/bin:$PATH"  
alias ll='ls -lah'  
source ~/.bashrc  
history | tail  
!42  

## 16. SSH & SCP
ssh user@host  
ssh-keygen -t ed25519  
ssh-copy-id user@host  
scp file.txt user@host:/tmp/  
scp -r dir/ user@host:/var/www/  

## 17. Git Essentials
git config --global user.name "Name"  
git config --global user.email "you@example.com"  
git init  
git clone https://github.com/lotsoflinux/repo.git  
git status  
git add .  
git commit -m "msg"  
git log --oneline --graph --decorate  
git switch -c feature  
git merge feature  
git push origin main  
git pull --rebase origin main  
git restore --staged file  
git reset --hard HEAD~1  

## 18. Cron Jobs
crontab -e  
crontab -l  
# Every day at 02:30  
30 2 * * * /usr/bin/backup.sh  
# Every 5 minutes  
*/5 * * * * /usr/bin/check.sh  

## 19. Editors (nano / vim)
nano file.txt  
vim file.txt  
# i=insert, :w=save, :q=quit, :wq=save+quit  

## 20. Docker Basics
docker pull ubuntu  
docker images  
docker run -it ubuntu bash  
docker ps  
docker stop container  
docker rm container  
docker run -v "$(pwd)":/work -w /work -p 8080:80 nginx  

## 21. Python Virtual Environments
python3 -m venv .venv  
source .venv/bin/activate  
pip install requests  
deactivate  

## 22. Useful Keyboard Shortcuts
Ctrl+A → Start of line  
Ctrl+E → End of line  
Alt+B → Back a word  
Alt+F → Forward a word  
Ctrl+U → Delete to start  
Ctrl+K → Delete to end  
Ctrl+R → History search  
Ctrl+L → Clear  
Ctrl+C → Cancel  
Ctrl+D → Exit  

## 23. Practice Ideas
# 1. Create directory tree & assign permissions  
# 2. Search logs for ERROR counts using grep/awk  
# 3. Archive & restore a project using tar  
# 4. Log disk usage daily via cron  
# 5. Create a simple systemd service  