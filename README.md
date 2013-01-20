# Steps used to create the VM

The configuration steps for participants are in the file
[PARTICIPANTS.md](/railsbridge-montreal/virtual_machine/blob/master/PARTICIPANTS.md).

## Notes about the VM

- Username: railsbridge
- Password: ruby rocks
- Hostname: rbvm

## Install Ubuntu

- Create new VM with
  - 20Gb resizable disk
- Modify the new VM's settings
  - Add second network adapter, set to "host only"
  - In the port mappings for 3000, 4000 and 5000 in 1st network adapter.
    No need to specify IP addresses.
- Install Ubuntu Desktop on it

## Install the dev tools

```shell
sudo apt-get install -y autoconf automake bison build-essential curl git-core libapr1 libaprutil1 libc6-dev libltdl-dev libreadline6 libreadline6-dev libsqlite3-0 libsqlite3-dev libssl-dev libtool libxml2-dev libxslt-dev libxslt1-dev libyaml-dev ncurses-dev openssl sqlite3 zlib1g zlib1g-dev
sudo apt-get install -y aptitude htop zerofree
curl -L https://get.rvm.io | bash -s stable --ruby
gem install rails heroku therubyracer
```

## Set up the machine just so

### Network address

```shell
sudo vi /etc/network/interfaces
```

And add

```
iface eth1 inet static
address 10.10.10.10
netmask 255.255.255.0
gateway 10.10.10.1
```

## Shrink the disk size before sharing

- zero out all the unused blocks. From inside the VM. Check out this
[article](http://dantwining.co.uk/2011/07/18/how-to-shrink-a-dynamically-expanding-guest-virtualbox-image/)

# Reference

- [RailsBridge Installfest](http://installfest.railsbridge.org/installfest/)
- [RVM](http://rvm.io)
