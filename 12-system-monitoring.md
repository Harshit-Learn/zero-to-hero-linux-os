
# 🐧 Day 12 - Linux System Monitoring

## Linux System Monitoring

### Introduction to System Monitoring
Monitoring system resources is essential to ensure optimal performance, detect issues, and troubleshoot problems in Linux. Various tools allow us to monitor CPU, memory, disk usage, network activity, and running processes.

---

## Index of Commands Covered

### CPU and Memory Monitoring
- top – Real-time system monitoring  
- htop – Interactive process viewer (requires installation)  
- vmstat – Report system performance statistics  
- free -m – Show memory usage  

---

### Disk Monitoring
- df -h – Check disk space usage  
- du -sh /path – Show disk usage of a specific directory  
- iostat – Display CPU and disk I/O statistics  

---

### Network Monitoring
- ifconfig – Show network interfaces (deprecated, use ip a)  
- ip a – Show network interface details  
- netstat -tulnp – Show active connections and listening ports  
- ss -tulnp – Alternative to netstat for socket statistics  
- ping hostname – Test network connectivity  
- traceroute hostname – Show network path to a host  
- nslookup domain – Get DNS resolution details  

---

### Log Monitoring
- tail -f /var/log/syslog – Live monitoring of system logs  
- journalctl -f – Live system logs for systemd-based distros  
- dmesg | tail – View kernel logs  

---

## CPU and Memory Monitoring

### Using top
To view real-time CPU and memory usage:
```

top

```id="m1"

Press q to quit.

---

### Using htop
A user-friendly alternative:
```

htop

```id="m2"

Use arrow keys to navigate and F9 to kill processes.

---

### Using vmstat
To check CPU, memory, and I/O stats:
```

vmstat 1 5  # Update every 1 sec, show 5 updates

```id="m3"

---

### Checking Memory Usage
```

free -m

```id="m4"

Shows free and used memory in megabytes.

---

## Disk Monitoring

### Using df
Check available disk space:
```

df -h

```id="m5"

---

### Using du
Find the size of a directory:
```

du -sh /var/log

```id="m6"

---

### Using iostat
Check disk and CPU usage:
```

iostat

```id="m7"

---

## Network Monitoring

### Checking Network Interfaces
```

ip a  # Show IP addresses and interfaces

```id="m8"

---

### Viewing Open Ports and Connections
```

netstat -tulnp  # Show listening ports
ss -tulnp  # Alternative to netstat

```id="m9"

---

### Testing Connectivity
```

ping google.com  # Test internet connection
traceroute google.com  # Trace the path to Google

```id="m10"

---

### Checking DNS Resolution
```

nslookup example.com

```id="m11"

---

## Log Monitoring

### Live Monitoring of System Logs
```

tail -f /var/log/syslog  # Follow logs in real-time
journalctl -f  # Systemd logs

```id="m12"

---

### Checking Kernel Logs
```

dmesg | tail

```id="m13"

---

# 🎯 Interview Questions

### Basic Questions
1. What is system monitoring in Linux?
2. Why is system monitoring important?
3. What resources can be monitored in Linux?

### Command-Based Questions
4. What is the use of `top` command?
5. Difference between `top` and `htop`?
6. What does `free -m` show?

### Disk & Network Questions
7. Difference between `df` and `du`?
8. What is `netstat` used for?
9. What is the use of `ping` command?

### Advanced Questions
10. How do you check logs in Linux?
11. What is `journalctl`?
12. How do you troubleshoot network issues in Linux?

### DevOps-Oriented Questions
13. How do you monitor a production server?
14. What tools do you use for real-time monitoring?
15. How do you debug high memory or CPU usage?
```

---


