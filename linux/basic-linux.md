# 🐧 Basic Linux Commands

> essential commands yang wajib dikuasai — dikelompokkan per kategori.

---

## 🌐 Networking

```bash
ping google.com              # Test internet connectivity
curl https://api.com         # Test API endpoints
wget https://file.com/file   # Download files
netstat -tulpn               # Check listening ports
ifconfig                     # Check IP (older systems)
ip a                         # Check IP (modern systems)
ssh user@192.168.1.1         # Remote secure connection
scp file user@host:/path     # Secure copy files
```

---

## 💻 System (OS)

```bash
pwd                         # Print working directory
ls                          # List files
ls -la                      # List all (including hidden)
cd /var/log                 # Change directory
cd ..                       # Go up one level
cd ~                        # Go to home directory
top                         # Real-time system monitor
htop                        # Better system monitor
ps aux                      # All running processes
ps aux | grep nginx         # Find specific process
kill 1234                   # Kill process by PID
killall nginx               # Kill all nginx processes
uname -a                    # System information
hostname                    # Show hostname
whoami                      # Current user
```

---

## 📂 File Operations

```bash
cp file.txt backup/         # Copy file
cp -r folder backup/        # Copy folder recursively
mv old.txt new.txt          # Rename file
mv file.txt /tmp/           # Move file
rm file.txt                 # Delete file
rm -rf folder/              # Delete folder (be careful!)
mkdir newfolder             # Create directory
mkdir -p path/to/folder     # Create nested directories
cat file.txt                # View file content
less file.txt               # View file (paginated)
nano file.txt               # Edit file (beginner-friendly)
vim file.txt                # Edit file (advanced)
touch file.txt              # Create empty file
chmod 755 script.sh         # rwxr-xr-x permissions
chmod +x script.sh          # Make executable
chown user:group file       # Change owner
```

---

## 🔐 Security

```bash
sudo command                # Run as superuser
sudo su                     # Switch to root
chmod 600 private.key       # Secure private files (rw owner only)
chmod 644 file.txt          # Standard file permissions (rw-r--r--)
chmod 700 ~/.ssh            # Secure SSH directory
ssh-keygen -t rsa           # Generate SSH key pair
ssh-keygen -t ed25519       # Generate modern SSH key
ufw status                  # Check firewall status
ufw enable                  # Enable firewall
ufw allow 22                # Allow SSH port
ufw allow 80/tcp            # Allow HTTP
history                     # View command history
history | grep sudo         # Search command history
export HISTSIZE=0           # Disable history (security)
```

---

## 🔍 Troubleshooting

```bash
tail -f /var/log/syslog    # Monitor logs live
tail -n 100 error.log      # View last 100 lines
grep "error" log.txt       # Search for text in file
grep -r "TODO" .           # Search recursively in all files
find . -name "*.log"       # Find files by name
find . -type f -mtime -7   # Find files modified in last 7 days
df -h                      # Disk space (human readable)
du -sh folder/             # Folder size
free -h                    # Memory usage
systemctl status nginx     # Check service status
systemctl restart nginx    # Restart service
systemctl enable nginx     # Enable service at boot
journalctl -xe             # View system logs
journalctl -u nginx        # View specific service logs
netstat -tulpn | grep :80  # Check what's using port 80
lsof -i :8080              # Check process using port 8080
```

---

*x.com/xeenau · #keeplearning*
