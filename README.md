# Introduction
A script to block the websites I frequently visit which reduce my
productivity. A web extension does that too, I understand, but since I run on
extremely low computer resources, I usually get things done by shell scripts.

**NOTE:** Please do not use this directly for your system. This script modifies `/etc/hosts` file.

# How to use

### Take a backup of `/etc/hosts`

```
sudo cp /etc/hosts /etc/hosts.bak
```

### Understand what the script is doing

Please don't use this script blindly as this might have serious consequences.
There might be many settings which you would have done for your network and it
is super important to respect those because this script doesn't. This script is
just a non-generic hack to solve my personal problem.

### Fill up `1.txt` and `2.txt`

The files `1.txt` and `2.txt` are derived from the `/etc/hosts` file. `2.txt`
consists of the configs for IPv6 settings while `1.txt` contains the rest.

### Fill up `ban.txt`

Enter all the domains you want to blacklist here. Please respect the format
already given.

###  Install

```
sudo ./install
```

**Note:** This starts the script on boot so whenever you start your computer,
all the websites you mentioned in `ban.txt` would be blocked by default.

### Uninstall

```
sudo ./uninstall
```

### Unblock

To unblock:

```
sudo no-distract off
```

### Block

```
sudo no-distract on
```
