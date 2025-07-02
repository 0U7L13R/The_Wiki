# Nmap Beginner Cheatsheet

---

## What is Nmap?

Nmap (Network Mapper) is a tool used to discover hosts and services on a computer network by sending packets and analyzing responses.

Tool name: `nmap`  
Website: https://nmap.org

---

## Basic Syntax
```bash
nmap [options] <target>
```

- `<target>` can be an IP address, hostname, or a range

---

## Common Scan Types

### Ping Scan
Check if a host is up:
```bash
nmap -sn 192.168.1.0/24
```

### Port Scan
Scan most common 1000 ports:
```bash
nmap 192.168.1.1
```

### Specific Port
```bash
nmap -p 22 192.168.1.1
```

### Multiple Ports
```bash
nmap -p 22,80,443 192.168.1.1
```

---

## Scan Techniques

### TCP Connect Scan
```bash
nmap -sT 192.168.1.1
```

### SYN Scan (default, needs root)
```bash
nmap -sS 192.168.1.1
```

---

## Service and Version Detection
```bash
nmap -sV 192.168.1.1
```

---

## OS Detection
```bash
nmap -O 192.168.1.1
```

---

## Aggressive Scan (includes -O -sV and more)
```bash
nmap -A 192.168.1.1
```

---

## Scan a Range of IPs
```bash
nmap 192.168.1.1-100
```

## Scan an Entire Subnet
```bash
nmap 192.168.1.0/24
```

---

## Output Options

### Save to file
```bash
nmap -oN output.txt 192.168.1.1
```

### Save all formats
```bash
nmap -oA scan_results 192.168.1.1
```

---

## Useful Options

- `-v` → Verbose output
- `-Pn` → Skip host discovery (treat all as online)
- `--open` → Show only open ports
- `-T4` → Faster execution (aggressive timing)

---

## Scripts (Nmap Scripting Engine)

### Run default scripts
```bash
nmap -sC 192.168.1.1
```

### Run specific script
```bash
nmap --script=http-title 192.168.1.1
```

---

