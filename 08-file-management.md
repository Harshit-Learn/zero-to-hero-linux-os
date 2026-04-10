

---

## 🐧 Day 8 - File Management in Linux

### 📌 File and Directory Management

Linux me file management is **core skill** for DevOps 🔥
👉 Daily use + troubleshooting + automation sab me use hota hai

---

## 📂 Basic Navigation Commands

### 🔹 List Files

```bash id="a1b2c3"
ls
```

👉 Files & directories show karta hai

---

### 🔹 Change Directory

```bash id="d4e5f6"
cd /path/to/directory
```

---

### 🔹 Current Directory

```bash id="g7h8i9"
pwd
```

---

## 📁 Create & Delete

### 🔹 Create Directory

```bash id="j1k2l3"
mkdir new_folder
```

---

### 🔹 Remove Empty Directory

```bash id="m4n5o6"
rmdir empty_folder
```

---

### 🔹 Delete File

```bash id="p7q8r9"
rm file.txt
```

---

### 🔹 Delete Folder (Important ⚠️)

```bash id="s1t2u3"
rm -r folder
```

👉 Recursive delete (dangerous command 🚨)

---

## 📄 Copy & Move

### 🔹 Copy File

```bash id="v4w5x6"
cp file1.txt file2.txt
```

---

### 🔹 Copy Directory

```bash id="y7z8a9"
cp -r dir1 dir2
```

---

### 🔹 Move / Rename

```bash id="b1c2d3"
mv old_name new_name
```

---

## 📖 File Viewing Commands

### 🔹 View File

```bash id="e4f5g6"
cat file.txt
```

---

### 🔹 Reverse View

```bash id="h7i8j9"
tac file.txt
```

---

### 🔹 Scroll View (Most Used 🔥)

```bash id="k1l2m3"
less file.txt
```

---

### 🔹 Limited View

```bash id="n4o5p6"
more file.txt
```

---

### 🔹 First 10 Lines

```bash id="q7r8s9"
head -n 10 file.txt
```

---

### 🔹 Last 10 Lines (Logs 🔥)

```bash id="t1u2v3"
tail -n 10 file.txt
```

---

## ✏️ File Editing

### 🔹 Nano (Beginner Friendly)

```bash id="w4x5y6"
nano file.txt
```

---

### 🔹 VI Editor (Important 🔥)

```bash id="z7a8b9"
vi file.txt
```

---

## 📝 Write to File

### 🔹 Overwrite File

```bash id="c1d2e3"
echo 'Hello' > file.txt
```

👉 Old data delete ho jayega

---

### 🔹 Append Data

```bash id="f4g5h6"
echo 'Hello' >> file.txt
```

👉 Data add hoga (safe)

---

## 🔥 DevOps Interview Questions (Most Important)

1. Difference between `rm` and `rm -r`?
2. Why is `rm -rf` dangerous?
3. Difference between `cp` and `mv`?
4. What is the use of `tail -f` in real-time logs?
5. Difference between `cat`, `less`, and `more`?
6. How do you monitor logs in production?
7. What happens when you use `>` vs `>>`?
8. How do you safely delete files in production?
9. What is the use of `head` and `tail`?
10. Which editor is preferred in servers and why (`vi` vs `nano`)?

---

