# Hydra Cheatsheet

---

## What is Hydra?

Hydra is a powerful **brute-force login cracker**. It's used by security professionals to test the strength of passwords across many protocols (like SSH, FTP, HTTP, etc.).

Tool name: `hydra`  
Website: https://github.com/vanhauser-thc/thc-hydra

---

## Basic Syntax
```bash
hydra [options] -L <userlist> -P <passlist> <protocol>://<target>
```

- `-L` → File with **usernames**
- `-P` → File with **passwords**
- `<protocol>` → Examples: ssh, ftp, http-get, etc.
- `<target>` → IP address or hostname

---

## Example Commands

### SSH Brute Force
```bash
hydra -L users.txt -P passwords.txt ssh://192.168.1.100
```

### FTP Brute Force
```bash
hydra -L usernames.txt -P passwords.txt ftp://192.168.1.50
```

### HTTP Basic Auth
```bash
hydra -L users.txt -P passwords.txt http-get://192.168.1.80/protected
```

---

## Username & Password Lists

You can create simple lists:
```bash
echo "admin" > users.txt
echo "1234" > passwords.txt
```

Or use common ones like:
- `/usr/share/wordlists/rockyou.txt` (Kali Linux)

---

## Useful Options

- `-V` → Show each attempt (verbose)
- `-t` → Number of parallel tasks (e.g., `-t 4`)
- `-f` → Exit after first successful login
- `-o` → Output results to a file

### Example with options:
```bash
hydra -L users.txt -P passwords.txt -t 4 -V -f ssh://192.168.1.10
```
