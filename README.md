# SSH Access Control Lab

This lab demonstrates how to configure the SSH server in Linux, allow access only to a specific user, and test the configuration.

## 📋 Lab Objectives

- Check SSH service status
- View SSH logs with `journalctl`
- Backup and edit the `sshd_config` file
- Restrict access using `AllowUsers`
- Restart SSH service and test access for allowed and denied users

---

## 🧪 Lab Steps & Screenshots

| Step | Description | Screenshot |
|------|-------------|------------|
| 1 | Check SSH service status | ![01](./screenshots/01_check-ssh-status.png) |
| 2 | Restart the SSH service | ![02](./screenshots/02_restart-ssh-service.png) |
| 3 | View SSH-related logs | ![03](./screenshots/03_ssh-journal-logs.png) |
| 4 | Backup `sshd_config` | ![04](./screenshots/04_backup-ssh-config.png) |
| 5 | Open `sshd_config` in nano | ![05](./screenshots/05_sshd-config-opened.png) |
| 6 | Confirm password authentication enabled | ![06](./screenshots/06_sshd-password-auth-enabled.png) |
| 7 | Add `AllowUsers liv` directive | ![07](./screenshots/07_sshd-allowusers-liv.png) |
| 8 | Restart SSH service after config edit | ![08](./screenshots/10_sshd-restarted.png) |
| 9 | Log in via SSH as `liv` (success) | ![09](./screenshots/11_ssh-login-liv-success.png) |
| 10 | Attempt SSH login as other user (denied) | ![10](./screenshots/12_ssh-denied-for-other-user.png) |
| 11 | Final SSH login verification | ![11](./screenshots/13_ssh-final-verification.png) |

---

## ✅ Result

Access is successfully restricted to the `liv` user via SSH. Other users are denied, as expected.

---

## 💬 Notes

- OS: Debian-based (VirtualBox)
- Commands used: `systemctl`, `journalctl`, `nano`, `ssh`, `cp`, `sudo`
- Backup file created: `/etc/ssh/sshd_config.bak`

