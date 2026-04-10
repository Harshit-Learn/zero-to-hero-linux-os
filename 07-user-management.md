

---

## 🐧 Day 7 - User Management in Linux

### 📌 Introduction to User Management in Linux

Linux is a **multi-user operating system**, meaning multiple users can work on the same system simultaneously.

👉 Proper user management ensures:

* Security 🔐
* Controlled access 🎯
* System stability ⚙️

---

### 📂 Important Files (Very Important for Interview)

| File           | Description                 |
| -------------- | --------------------------- |
| `/etc/passwd`  | Stores user account details |
| `/etc/shadow`  | Stores encrypted passwords  |
| `/etc/group`   | Stores group information    |
| `/etc/gshadow` | Stores secure group details |

---

## 🚀 Creating Users

### 🔹 Using `useradd` (Basic Command)

```bash id="d0t3vp"
useradd username
```

👉 Creates user **without home directory**

---

### 🔹 Create User with Home Directory

```bash id="9c1z5g"
useradd -m username
```

---

### 🔹 Assign Shell

```bash id="9z8rxt"
useradd -s /bin/bash username
```

---

### 🔹 Using `adduser` (Interactive – Debian/Ubuntu)

```bash id="o1p8fj"
adduser username
```

👉 Automatically:

* Creates home directory
* Sets password
* Asks user details

---

## 🔐 Managing Passwords

### 🔹 Set / Change Password

```bash id="v83kq1"
passwd username
```

---

### 🔹 Password Expiry (Important 🔥)

```bash id="n5g0te"
chage -M 90 username
```

👉 Password expires after 90 days

---

### 🔹 Lock / Unlock User

```bash id="nq1g6b"
passwd -l username
```

```bash id="2h6s8p"
passwd -u username
```

---

## ⚙️ Modifying Users

### 🔹 Change Username

```bash id="h3v4kc"
usermod -l new_username old_username
```

---

### 🔹 Change Home Directory

```bash id="7lbz5y"
usermod -d /new/home -m username
```

---

### 🔹 Change Shell

```bash id="1y7r6x"
usermod -s /bin/zsh username
```

---

## ❌ Deleting Users

### 🔹 Delete User Only

```bash id="u2r9bd"
userdel username
```

---

### 🔹 Delete User with Home Directory

```bash id="m5xk0v"
userdel -r username
```

---

## 👥 Working with Groups

### 🔹 Create Group

```bash id="b9d2qn"
groupadd groupname
```

---

### 🔹 Add User to Group

```bash id="h4r8zs"
usermod -aG groupname username
```

---

### 🔹 Check Groups

```bash id="s7v6py"
groups username
```

---

### 🔹 Change Primary Group

```bash id="k8f1tw"
usermod -g groupname username
```

---

## 🔥 Sudo Access (Very Important in DevOps)

### 🔹 Add User to Sudo Group

👉 Debian/Ubuntu:

```bash id="6u2x1q"
usermod -aG sudo username
```

👉 RHEL/CentOS:

```bash id="z3w9lp"
usermod -aG wheel username
```

---

### 🔹 Edit Sudoers File

```bash id="5q2v7o"
visudo
```

Add:

```bash id="0t8x9k"
username ALL=(ALL) NOPASSWD: /path/to/command
```

---

## 🔥 DevOps Interview Questions (Most Important)

1. Difference between `/etc/passwd` and `/etc/shadow`?
2. What happens if `/etc/shadow` is exposed?
3. Difference between `useradd` and `adduser`?
4. How do you give sudo access to a user?
5. What is `NOPASSWD` in sudoers?
6. Difference between primary group and secondary group?
7. How do you check which users have sudo access?
8. How do you lock a user without deleting it?
9. What is least privilege principle in Linux?
10. How do you manage users in production servers?

---

