## Ansible Desktop Setup for Debian 9

Become a root user and install the following packages:

```bash
apt-get install sudo dirmngr
adduser <username> sudo
```

Add the following lines to `/etc/apt/sources.list`

```bash
# jessie security updates
deb http://security.debian.org/debian-security jessie/updates main

# ansible
deb http://ppa.launchpad.net/ansible/ansible/ubuntu trusty main
```

Then run these commands:

```bash
sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 93C4A3FD7BB9C367
sudo apt-get update
sudo apt-get install ansible
```

Finally, run the following to configure your workstation:

```bash
sudo ansible-pull -U https://github.com/vagmcs/ansible-desktop.git
```

