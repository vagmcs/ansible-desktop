## Ansible Desktop Setup for Debian 9

Become a root user and do the following:

```bash
apt-get install sudo dirmngr git
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
apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 93C4A3FD7BB9C367
apt-get update
apt-get install ansible
```

Finally, run the `main.yml` playbook to configure your workstation:

```bash
sudo ansible-playbook main.yml
```

