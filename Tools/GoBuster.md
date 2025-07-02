# Gobuster Cheatsheet

---

## What is Gobuster?

Gobuster is a tool used to brute-force URIs (directories and files) on web servers. It helps discover hidden content by using wordlists.

Tool name: `gobuster`  
Website: https://github.com/OJ/gobuster

---

## Basic Syntax
```bash
gobuster dir -u <URL> -w <wordlist>
```

- `dir` → Mode for directory/file enumeration
- `-u` → Target URL
- `-w` → Wordlist to use (e.g., common.txt)

---

## Example Commands

### Directory brute force
```bash
gobuster dir -u http://192.168.1.10 -w /usr/share/wordlists/dirb/common.txt
```

### With file extension
```bash
gobuster dir -u http://192.168.1.10 -w /usr/share/wordlists/dirb/common.txt -x php,html,txt
```

### Increase threads
```bash
gobuster dir -u http://example.com -w custom.txt -t 50
```

---

## Useful Options

- `-x` → File extensions to search (comma-separated)
- `-t` → Number of threads (default is 10)
- `-o` → Output results to a file
- `-q` → Suppress unnecessary output
- `-b` → Status codes to ignore (e.g., `-b 404`)

---

## Wordlists

Common wordlists are found in:
```
/usr/share/wordlists/
```

Popular choices:
- `dirb/common.txt`
- `SecLists/Discovery/Web-Content/common.txt`

---

## Modes of Operation

- `dir` → Directory brute-forcing
- `dns` → Subdomain brute-forcing
- `vhost` → Virtual host brute-forcing
- `s3` → AWS bucket enumeration
- `fuzz` → General purpose fuzzing

---

