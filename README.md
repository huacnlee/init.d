```
   ______              __           __
  /\__  _\          __/\ \__       /\ \
  \/_/\ \/     ___ /\_\ \ ,_\      \_\ \
     \ \ \   /' _ `\/\ \ \ \/      /'_` \
      \_\ \__/\ \/\ \ \ \ \ \_  __/\ \L\ \
      /\_____\ \_\ \_\ \_\ \__\/\_\ \___,_\
      \/_____/\/_/\/_/\/_/\/__/\/_/\/__,_ /
```

Batch scripts for Ruby production environment install on Ubuntu Server.

[![wercker status](https://app.wercker.com/status/2dd2ff58518cae2dd75e4556e6d931c5/s/master "wercker status")](https://app.wercker.com/project/bykey/2dd2ff58518cae2dd75e4556e6d931c5)

## Requirements

* Ubuntu Server 14.04

## Usage

Install packages first

```bash
sudo apt-get update
sudo apt-get install -y curl
curl -sSL https://raw.githubusercontent.com/huacnlee/init.d/master/install_packages | sh
```

### Install Nginx

```bash
curl -sSL https://raw.githubusercontent.com/huacnlee/init.d/master/install_nginx | sh
```

### Install RVM + Ruby

```bash
curl -sSL https://raw.githubusercontent.com/huacnlee/init.d/master/install_rvm | sh
source ~/.rvm/scripts/rvm
rvm pkg install readline openssl
rvm install 2.3.0
rvm use 2.3.0 --default
gem sources --add https://gems.ruby-china.org/ --remove https://rubygems.org/
gem install bundler
```

### Install MongoDB

```bash
curl -sSL https://raw.githubusercontent.com/huacnlee/init.d/master/install_mongodb | sh
```

### Install Redis

```bash
curl -sSL https://raw.githubusercontent.com/huacnlee/init.d/master/install_redis | sh
```
