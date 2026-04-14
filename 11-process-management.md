
# 🐧 Day 11 - Process Management in Linux

## Process Management in Linux

### Introduction to Process Management
A process is an instance of a running program. Linux provides multiple utilities to monitor, manage, and control processes effectively. Each process has a unique Process ID (PID) and belongs to a parent process.

---

## Index of Commands Covered

### Viewing Processes
- ps aux – View all running processes  
- ps -u username – View processes for a specific user  
- ps -C processname – Show a process by name  
- pgrep processname – Find a process by name and return its PID  
- pidof processname – Find the PID of a running program  

---

### Managing Processes
- kill PID – Terminate a process by PID  
- pkill processname – Terminate a process by name  
- kill -9 PID – Force kill a process  
- pkill -9 processname – Kill all instances of a process  
- kill -STOP PID – Stop a running process  
- kill -CONT PID – Resume a stopped process  
- renice -n 10 -p PID – Lower priority of a process  
- renice -n -5 -p PID – Increase priority of a process (requires root)  

---

### Background & Foreground Processes
- command & – Run a command in the background  
- jobs – List background jobs  
- fg %jobnumber – Bring a job to the foreground  
- Ctrl + Z – Suspend a running process  
- bg %jobnumber – Resume a suspended process in the background  

---

### Monitoring System Processes
- top – Interactive process viewer  
- htop – User-friendly process viewer (requires installation)  
- nice -n 10 command – Run a command with a specific priority  
- renice -n -5 -p PID – Change priority of an existing process  

---

### Daemon Process Management
- systemctl list-units --type=service – List all system daemons  
- systemctl start service-name – Start a daemon/service  
- systemctl stop service-name – Stop a daemon/service  
- systemctl enable service-name – Enable a service at startup  

---

## Viewing Process Details

### Using ps
Show processes for a specific user:
```

ps -u username

```id="p1"

Show a process by name:
```

ps -C processname

```id="p2"

---

### Using pgrep
Find a process by name and return its PID:
```

pgrep processname

```id="p3"

---

### Using pidof
Find the PID of a running program:
```

pidof processname

```id="p4"

---

## Managing Processes

### Killing Processes
To terminate a process by PID:
```

kill PID

```id="p5"

To terminate using process name:
```

pkill processname

```id="p6"

Force kill a process:
```

kill -9 PID

```id="p7"

Kill all instances of a process:
```

pkill -9 processname

```id="p8"

---

### Stopping & Resuming Processes
Stop a running process:
```

kill -STOP PID

```id="p9"

Resume a stopped process:
```

kill -CONT PID

```id="p10"

---

### Changing Process Priority
View process priorities:
```

top  # Look at the NI column

```id="p11"

Change priority of a running process:
```

renice -n 10 -p PID  # Lower priority (positive values)
renice -n -5 -p PID  # Higher priority (negative values, root required)

```id="p12"

---

## Running Processes in the Background

Run a command in the background:
```

command &

```id="p13"

List background jobs:
```

jobs

```id="p14"

Bring a job to the foreground:
```

fg %jobnumber

```id="p15"

Send a running process to the background:
```

Ctrl + Z  # Suspend process
bg %jobnumber  # Resume in background

```id="p16"

---

## Monitoring System Processes

### Using top
Interactive process viewer:

- Press k and enter a PID to kill a process.  
- Press r to renice a process.  
- Press q to quit.  

---

### Using htop
A user-friendly alternative to top:
```

htop

```id="p17"

Allows mouse-based interaction for process management.

---

### Using nice & renice
Run a command with a specific priority:
```

nice -n 10 command

```id="p18"

Change the priority of an existing process:
```

renice -n -5 -p PID

```id="p19"

---

## Daemon Processes

Daemon processes run in the background without user intervention. List all system daemons:
```

systemctl list-units --type=service

```id="p20"

Start a daemon:
```

systemctl start service-name

```id="p21"

Stop a daemon:
```

systemctl stop service-name

```id="p22"

Enable a service at startup:
```

systemctl enable service-name

```id="p23"

---

## Conclusion

Process management is crucial for system performance and stability. By using tools like ps, top, htop, kill, and nice, you can efficiently control and monitor Linux processes.

---

# 🎯 Interview Questions

### Basic Questions
1. What is a process in Linux?
2. What is PID?
3. What is the difference between process and program?

### Command-Based Questions
4. What does `ps aux` do?
5. Difference between `kill` and `pkill`?
6. What is the use of `top` command?

### Advanced Questions
7. What is the difference between `kill` and `kill -9`?
8. What are foreground and background processes?
9. What is process priority (nice value)?

### DevOps-Oriented Questions
10. How do you troubleshoot high CPU usage in Linux?
11. What tools do you use to monitor processes?
12. How do you manage services using systemctl?
```

---

