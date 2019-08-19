# Installing rng-tools package
Linux rng-tools installation instructions

## YUM package manager

### YUM online installation

Download and install rng-tools rpm.

```bash
sudo yum install -y rng-tools
```

Enable and start rngd service.

```bash
sudo systemctl enable rngd
sudo systemctl start rngd
```

### YUM offline installation

Installation of locally available rpm.

If the system(s) do not have sufficient network connectivity to allow for an online installation, you can download the rpm package, copy to the system and install using the locally available rpm.

Download the rpm from the distribution provider.

[Redhat Enterprise Linux](https://access.redhat.com/solutions/6996)
[CentOS 6](http://mirror.centos.org/centos/6/os/x86_64/Packages/)
[CentOS 7](http://mirror.centos.org/centos/7/os/x86_64/Packages/)

```
sudo yum localinstall -y /tmp/rng-tools-$VERSION.rpm
```

## APT package manager

Installtion using APT.

### apt-get online installation

```bash
sudo apt-get rng-tools
```

### APT offline installation


rng-tools package can be downloaded from:
[Ubuntu 16.04](https://packages.ubuntu.com/xenial/rng-tools)
[Ubuntu 18.04](https://packages.ubuntu.com/bionic/rng-tools)

```bash
sudo dpkg -i /tmp/rng-tools_$VERSION.deb
```

## Starting Systemd service

Start rngd systemd service Redhat Enterprise Linux 7+, CentOS 7+
The service name in RHEL=based distributions is `rngd`.
```bash
sudo systemctl start rngd
```

Start rng-tools systemd service in Ubuntu.
The service name in Ubuntu is `rng-tools`.
```bash
sudo systemctl start rng-tools
```

## CentOS 6.x - Enable and start rngd service

```
sudo chkconfig rngd on
sudo service rngd start
```

## Examples

[Ubuntu 16.04 online](examples/Ubuntu-16-apt-get.log)
[Ubuntu 16.04 offline](examples/Ubuntu-16-dpkg.log)
[Ubuntu 18.04 online](examples/Ubuntu-18-apt-get.log)
[Ubuntu 18.04 offline](examples/Ubuntu-18-dpkg.log)
[CentOS 6.10 online](examples/CentOS-6.10-yum.log)
[CentOS 6.10 offline](examples/CentOS-6.10-yum-localinstall.log)
[CentOS 7.6.1810 online](examples/CentOS-7.6.1810-yum.log)
[CentOS 7.6.1810 offline](examples/CentOS-7.6.1810-yum-localinstall.log)
