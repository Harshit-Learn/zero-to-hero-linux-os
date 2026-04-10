

---

## 🐧 Day 9 - Vim Editor Shortcuts

### 📌 VI / Vim Editor

Vim is a **powerful terminal-based text editor** 🔥
👉 Mostly used in:

* Servers
* Production environments
* DevOps workflows

---

## ⚙️ Modes in Vim (Very Important 🔥)

| Mode         | Description                          |
| ------------ | ------------------------------------ |
| Normal Mode  | Default mode (navigation & commands) |
| Insert Mode  | Used for writing/editing text        |
| Command Mode | Used for save, quit, search          |

👉 Switch:

* `i` → Insert mode
* `Esc` → Normal mode
* `:` → Command mode

---

## 🧭 Basic Navigation

```bash id="n1a2v3"
h → left
l → right
j → down
k → up
```

```bash id="b4c5d6"
0 → start of line
^ → first non-blank char
$ → end of line
```

```bash id="e7f8g9"
w → next word
b → previous word
```

```bash id="h1i2j3"
gg → start of file
G → end of file
:n → go to line n
```

---

## ✍️ Insert Mode Shortcuts

```bash id="k4l5m6"
i → insert before cursor
I → beginning of line
a → after cursor
A → end of line
```

```bash id="n7o8p9"
o → new line below
O → new line above
Esc → exit insert mode
```

---

## ✂️ Editing Text

```bash id="q1r2s3"
x → delete char
X → delete before cursor
```

```bash id="t4u5v6"
dw → delete word
dd → delete line
```

```bash id="w7x8y9"
d$ → delete to end
d0 → delete to start
D → delete to end
```

```bash id="z1a2b3"
u → undo
Ctrl + r → redo
```

```bash id="c4d5e6"
yy → copy line
yw → copy word
p → paste after
P → paste before
```

---

## 🔍 Search & Replace (Very Important 🔥)

```bash id="f7g8h9"
/pattern → search forward
?pattern → search backward
```

```bash id="i1j2k3"
n → next result
N → previous result
```

```bash id="l4m5n6"
:%s/old/new/g → replace all
:s/old/new/g → replace in line
```

---

## 📂 Working with Files

```bash id="o7p8q9"
:e filename → open file
:w → save
:wq → save & exit
:q! → quit without saving
```

---

## 🖥️ Split Screen (DevOps Useful 🔥)

```bash id="r1s2t3"
:split file → horizontal split
:vsplit file → vertical split
```

```bash id="u4v5w6"
Ctrl + w + w → switch window
```

---

## 🔥 DevOps Interview Questions (Most Important)

1. Why is Vim preferred over GUI editors in servers?
2. Difference between Normal, Insert, and Command mode?
3. How do you save and exit in Vim?
4. What is the use of `:%s/old/new/g`?
5. How do you search text in Vim?
6. How do you undo/redo changes?
7. How do you copy-paste in Vim?
8. How do you open multiple files in Vim?
9. Why is Vim important in production environments?
10. What will happen if you forget to save before exit?

---


