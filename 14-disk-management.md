
# 🐧 Day 14 - Disk and Storage Management in Linux

## Introduction to Disk and Storage Management
Managing disks and storage efficiently is crucial for system performance and stability. Linux provides various commands to monitor, partition, format, mount, and manage disk storage.

---

## Index of Commands Covered

### Viewing Disk Information
- lsblk – Display block devices  
- fdisk -l – List disk partitions  
- blkid – Show UUIDs of devices  
- df -h – Check disk space usage  
- du -sh /path – Show size of a directory  

---

### Partition Management
- fdisk /dev/sdX – Create and manage partitions  
- parted /dev/sdX – Alternative to fdisk for GPT disks  
- mkfs.ext4 /dev/sdX1 – Format a partition as ext4  
- mkfs.xfs /dev/sdX1 – Format a partition as XFS  

---

### Mounting and Unmounting
- mount /dev/sdX1 /mnt – Mount a partition  
- umount /mnt – Unmount a partition  
- mount -o remount,rw /mnt – Remount a partition as read-write  

---

### Logical Volume Management (LVM)
- pvcreate /dev/sdX – Create a physical volume  
- vgcreate vg_name /dev/sdX – Create a volume group  
- lvcreate -L 10G -n lv_name vg_name – Create a logical volume  
- mkfs.ext4 /dev/vg_name/lv_name – Format an LVM partition  
- mount /dev/vg_name/lv_name /mnt – Mount an LVM partition  

---

### Swap Management
- mkswap /dev/sdX – Create a swap partition  
- swapon /dev/sdX – Enable swap space  
- swapoff /dev/sdX – Disable swap space  

---

## Viewing Disk Information

### Using lsblk
List all block devices:
```

lsblk

```id="d1"

---

### Using fdisk
View partition details:
```

fdisk -l

```id="d2"

---

### Using df
Check available disk space:
```

df -h

```id="d3"

---

### Using du
Find the size of a directory:
```

du -sh /var/log

```id="d4"

---

## Partition Management

### Creating a Partition with fdisk
```

fdisk /dev/sdX

```
Follow the interactive prompts to create a partition.

---

### Formatting a Partition
Format as ext4:
```

mkfs.ext4 /dev/sdX1

```id="d5"

Format as XFS:
```

mkfs.xfs /dev/sdX1

```id="d6"

---

## Mounting and Unmounting

### Mount a Partition
```

mount /dev/sdX1 /mnt

```id="d7"

---

### Unmount a Partition
```

umount /mnt

```id="d8"

---

### Remount a Partition
```

mount -o remount,rw /mnt

```id="d9"

---

## LVM Management

### Create a Physical Volume
```

pvcreate /dev/sdX

```id="d10"

---

### Create a Volume Group
```

vgcreate vg_name /dev/sdX

```id="d11"

---

### Create a Logical Volume
```

lvcreate -L 10G -n lv_name vg_name

```id="d12"

---

### Format and Mount the Logical Volume
```

mkfs.ext4 /dev/vg_name/lv_name
mount /dev/vg_name/lv_name /mnt

```id="d13"

---

## Swap Management

### Create a Swap Partition
```

mkswap /dev/sdX

```id="d14"

---

### Enable Swap
```

swapon /dev/sdX

```id="d15"

---

### Disable Swap
```

swapoff /dev/sdX

```id="d16"

---

## Additional Notes - When to Use fdisk, mount, or Both

### Check Available Disks
Before creating or mounting anything, always check what block devices exist:
```

lsblk

```id="d17"

Example output:
```

NAME	MAJ:MIN	RM	SIZE	RO	TYPE	MOUNTPOINT
sda	8:0	0	100G	0	disk
├─sda1	8:1	0	96G	0	part	/
└─sda2	8:2	0	4G	0	part	[SWAP]
sdb	8:16	0	20G	0	disk

```

sda → existing disk (already partitioned)  
sdb → new disk, no partitions yet  

---

### When to use fdisk
Use fdisk when:

- The disk is brand new and has no partitions  
- You want to create /dev/sdb1, /dev/sdb2, etc.  

Inside fdisk:
- Press n → create a new partition  
- Press w → write changes  

Then confirm:
```

lsblk

```id="d18"

---

### When to Use mount
Use mount when: The partition already exists and is formatted You just want to make it accessible

```

sudo mkdir /mnt/mydisk
sudo mount /dev/sdb1 /mnt/mydisk

```id="d19"

Now your disk is available at /mnt/mydisk.

---

### When to Use fdisk + mount (Full Setup)
Use fdisk + mkfs + mount when: The disk is completely new You need to partition → format → mount it

```

# 1. Check available disks

lsblk

# 2. Create partition

sudo fdisk /dev/sdb

# 3. Format the partition

sudo mkfs.ext4 /dev/sdb1

# 4. Mount it

sudo mkdir /data
sudo mount /dev/sdb1 /data

```id="d20"

---

## Quick Reference

| Use Case | Command(s) |
|----------|------------|
| View disks and partitions | lsblk |
| Partition a new disk | fdisk |
| Mount an existing partition | mount |
| Full setup (new disk) | fdisk + mkfs + mount |

---

# 🎯 Interview Questions

### Basic Questions
1. What is disk management in Linux?
2. What is the use of `lsblk`?
3. Difference between `df` and `du`?

### Command-Based Questions
4. How do you create a partition in Linux?
5. How do you format a disk?
6. What is the use of `mount` and `umount`?

### Advanced Questions
7. What is LVM in Linux?
8. Difference between ext4 and XFS?
9. What is swap space?

### DevOps-Oriented Questions
10. How do you handle disk full issues in production?
11. How do you add a new disk to a running server?
12. Why is LVM used in production environments?
```

---


