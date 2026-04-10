
---

## 🐧 Day 10 - File Permissions in Linux

### 📌 Introduction to File Permissions

Linux me har file/directory ke liye **access control hota hai** 🔐

👉 3 types of users:

* **Owner (User)** → file ka creator
* **Group** → same group ke users
* **Others** → baki sab users

---

## 🔢 Permission Types (Very Important 🔥)

| Permission | Symbol | Value | Meaning             |
| ---------- | ------ | ----- | ------------------- |
| Read       | r      | 4     | File dekh sakte ho  |
| Write      | w      | 2     | Modify kar sakte ho |
| Execute    | x      | 1     | Run kar sakte ho    |

---

## 🔍 Check Permissions

```bash id="a1p2q3"
ls -l filename
```

Example:

```bash id="b4r5s6"
-rwxr--r-- 1 user group 1234 myfile.sh
```

👉 Breakdown:

* `rwx` → Owner
* `r--` → Group
* `r--` → Others

---

## ⚙️ Change Permissions (chmod)

### 🔹 Symbolic Mode

```bash id="c7t8u9"
chmod u+x filename
```

👉 User ko execute permission

```bash id="d1v2w3"
chmod g-w filename
```

👉 Group se write remove

```bash id="e4x5y6"
chmod o=r filename
```

👉 Others → read only

```bash id="f7z8a9"
chmod u=rwx,g=rx,o= filename
```

👉 Full control setup

---

### 🔹 Numeric Mode (Most Asked 🔥)

```bash id="g1b2c3"
chmod 755 filename
```

👉 Owner: rwx, Group: r-x, Others: r-x

```bash id="h4d5e6"
chmod 644 filename
```

👉 Common for files

```bash id="i7f8g9"
chmod 700 filename
```

👉 Private file (only owner)

---

## 👤 Change Ownership (chown)

```bash id="j1h2i3"
chown user filename
```

```bash id="k4j5k6"
chown user:group filename
```

```bash id="l7l8m9"
chown -R user:group directory/
```

---

## 👥 Change Group (chgrp)

```bash id="m1n2o3"
chgrp group filename
```

```bash id="n4p5q6"
chgrp -R group directory/
```

---

## 🔥 Special Permissions (Very Important 🔥🔥)

### 🔹 SetUID

```bash id="o7r8s9"
chmod u+s filename
```

👉 File run hoga **owner permission se**

---

### 🔹 SetGID

```bash id="p1t2u3"
chmod g+s directory/
```

👉 New files inherit group

---

### 🔹 Sticky Bit

```bash id="q4v5w6"
chmod +t directory/
```

👉 Only owner can delete files (example: `/tmp`)

---

## ⚙️ Default Permissions (umask)

```bash id="r7x8y9"
umask
```

```bash id="s1z2a3"
umask 022
```

👉 Default:

* File → 644
* Directory → 755

---

## 🔥 DevOps Interview Questions (MOST IMPORTANT)

1. Difference between `chmod 777` and `chmod 755`? ⚠️
2. Why should we avoid `777` in production?
3. What is umask and how it works?
4. Difference between `chown` and `chgrp`?
5. What is SetUID, SetGID, Sticky Bit?
6. Why `/tmp` has sticky bit?
7. How do you secure sensitive files in `/etc`?
8. What happens if permissions are wrong in production?
9. How do you give access to only one user?
10. Real scenario: app not running → how permissions check karoge?

---

