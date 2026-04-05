## User Activity

| Command | What It Does |
|---------|---------------|
| `lastlog` | Shows last login time for every user |
| `faillog -a` | Shows failed login attempts per user |

## Network

| Command | What It Does |
|---------|---------------|
| `lsof -i -P -n` | Open network connections (no DNS, no port names) |
| `ss -tunap` | Detailed sockets with process names |

## Auditing

| Command | What It Does |
|---------|---------------|
| `auditctl -l` | List active audit rules |
| `ausearch -m USER_LOGIN -ts today` | Search today's user logins |

## File Changes

| Command | What It Does |
|---------|---------------|
| `debsums -c` | Find changed system files (Debian/Ubuntu) |
| `rpm -Va` | Verify all packages (RHEL/Fedora) |
| `getcap -r / 2>/dev/null` | Find files with Linux capabilities |

## Rootkits

| Command | What It Does |
|---------|---------------|
| `sudo chkrootkit` | Scan for rootkits |
| `sudo rkhunter -c` | Rootkit hunter scan |

## System Health

| Command | What It Does |
|---------|---------------|
| `systemd-analyze blame` | Show slow boot services |
| `journalctl --verify` | Check journal file integrity |
| `logwatch --detail High` | Daily log summary (install logwatch first) |

## SUID Files

| Command | What It Does |
|---------|---------------|
| `find / -perm -4000 -type f 2>/dev/null` | Find all SUID binaries |
| `find / -perm -2000 -type f 2>/dev/null` | Find all SGID binaries |

Most people Google basic commands. Attackers know that. They exploit the commands you forgot exist.
