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
curl -sSL https://git.io/vVHhe | bash
```

### Install Nginx

```bash
curl -sSL https://git.io/vVHhf | bash
```

### Install RVM + Ruby

```bash
curl -sSL https://git.io/vVHhJ | bash
gem sources --add https://gems.ruby-china.org/ --remove https://rubygems.org/
gem install bundler
```

### Install MongoDB

```bash
curl -sSL https://git.io/vVHhT | bash
```

### Install Redis

```bash
curl -sSL https://git.io/vVHhk | bash
```

### Install ElasticSearch

```bash
curl -sSL https://git.io/vVHhm | bash
sudo service elasticsearch status
```
