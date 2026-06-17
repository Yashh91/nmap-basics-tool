## Step 1 — Open Terminal in Kali Linux

Press:

```
Ctrl+ Alt+ T
```

---

## Step 2 — Check if Nmap is Installed

Type:

```
nmap --version
```

If installed, it will show version details.

<img width="1676" height="296" alt="image" src="https://github.com/user-attachments/assets/c8818c97-72b7-4ca0-b8c3-c0806b6d5818" />


If not installed:

```
sudo apt install nmap
```

---

## Step 3 — Scan a Website or IP

Basic scan:

```
nmap scanme.nmap.org
```

This checks:

- Open ports
- Running services

Example output:

<img width="1457" height="599" alt="image" src="https://github.com/user-attachments/assets/2e3930dc-861a-4466-b547-0043b3eab3af" />


## 1. Scan Single IP

```
nmap  <target-ip> 
```

---

## 2. Scan Multiple IPs

```
nmap <ip1> <ip2> <ip3>
```

---

## 3. Scan Entire Network

```
nmap <network-ip>/24
```

This scans all devices in the network.

---

## 4. Fast Scan

```
nmap -F <target-ip>
```

Scans fewer ports quickly.

---

## 5. Service Version Detection

```
nmap -sV <target-ip>
```

Detects software versions.

Example:

```
80/tcp open http Apache httpd 2.4.49
```

---

## 6. Operating System Detection

```
sudo nmap -O <target-ip>
```

Detects:

- Linux
- Windows
- Android
- Router OS

---

## 7. Aggressive Scan

```
sudo nmap -A <target-ip>
```

Includes:

- OS detection
- Version detection
- Script scanning
- Traceroute

---

## 8. Scan Specific Ports

```
nmap -p <port1,port2> <target-ip>
```

Only scans:

- 80
- 443

## Example

```
nmap -p 80,443 scanme.nmap.org
```

---

## 9. Scan All Ports

```
nmap -p- <target-ip>
```

Scans all 65535 ports.

---

## 10. Save Results to File

```
nmap -oN <filename.txt> <target-ip>
```

## Example

```
nmap -oN result.txt scanme.nmap.org
```

Results saved in:

```
result.txt
```
