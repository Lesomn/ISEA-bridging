# ISEA Lab Journal

Hello. New to Linux, github, and cloud stuff.

---

## Contents

- [Day 1a](#day-1a)
- [Day 1b](#day-1b)

---

## Day 1a

### Setting up GitHub

First thing I did was make a GitHub account and set up this repo so I could keep track of everything.

What I did:
- Signed up for GitHub
- Made this repo (`ISEA-labs`)
- Cloned it down to my laptop
- Started writing this README

```bash
git clone https://github.com/<my-username>/ISEA-labs.git
cd ISEA-labs
git add .
git commit -m "Initial commit"
git push
```

**What I learned:**
> _(Github Add/Commit/Push/etc.)_

---

### Installing Ubuntu with VirtualBox

I installed Ubuntu as a virtual machine so I didn't have to touch my actual PC.

What I did:
- Downloaded the Ubuntu ISO from ubuntu.com
- Installed VirtualBox
- Made a new VM (gave it 8GB RAM and 25GB disk space)
- Popped the ISO in and ran through the installer

`![VM setup](images/vm-setup.png)`

**What I learned / issues I hit:**
> _(Lots of issues, lots of freezing on loading screen. It's a hassle. I had to use 8000mb and 4 cores with 128 video memory to get it to work.)_

---

### Getting comfortable with Ubuntu

Just practicing the basics of moving around in the terminal.

```bash
pwd
ls -l
cd /var/log
mkdir test-folder
touch test-file.txt
man ls
```

Folders I poked around in:
| Folder | What's in it |
|---|---|
| `/etc` | config files for the system |
| `/var` | logs and other changing data |
| `/home` | my user files |

**What I learned:**
> _(Stuff in var/log.)_

---

## Day 1b

### Linux services

Learning how to check on and control background services (the stuff running quietly that keeps things working).

```bash
systemctl list-units --type=service
sudo systemctl start nginx
sudo systemctl stop nginx
sudo systemctl status nginx
```

`![service status](images/service-status.png)`

**What I learned:**
> _(What service is being tested.)_

---

### Permissions

This one took a bit to click, but here's what I practiced:

```bash
ls -l file.sh
chmod 755 file.sh
chown user:group file.txt
```

Quick cheat sheet I made for myself:
| Number | Means |
|---|---|
| 4 | read |
| 2 | write |
| 1 | execute |
| 7 | read + write + execute |
| 5 | read + execute |

**What I learned:**
> _(Permission and Ownership are necessary but really annoying.)_

---

### Finding stuff in the filesystem

```bash
find /home -name "*.txt"
grep -r "error" /var/log/
```

**What I learned:**
> _(Flags are useful.)_

---
