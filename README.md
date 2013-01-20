# Steps used to create the VM

The remaining configuration steps for participants are in the file
[PARTICIPANTS.md](./PARTICIPANTS.md).

## Notes

Username: railsbridge
Password: ruby rocks

## Install Ubuntu

- Create new VM with 20Gb resizable disk, and install Ubuntu Desktop on it
- Install all the dev tools

```shell
sudo apt-get install -y autoconf automake bison build-essential curl git-core libapr1 libaprutil1 libc6-dev libltdl-dev libreadline6 libreadline6-dev libsqlite3-0 libsqlite3-dev libssl-dev libtool libxml2-dev libxslt-dev libxslt1-dev libyaml-dev ncurses-dev openssl sqlite3 zlib1g zlib1g-dev
sudo apt-get install -y aptitude htop
curl -L https://get.rvm.io | bash -s stable --ruby
gem install rails bundler heroku
```

## Shrink the disk size before sharing

- zero out all the unused blocks. From inside the VM:

```shell
sudo aptitude install zerofree
zerofree
```
# Reference

- [RailsBridge Installfest](http://installfest.railsbridge.org/installfest/)
- [RVM](http://rvm.io)
