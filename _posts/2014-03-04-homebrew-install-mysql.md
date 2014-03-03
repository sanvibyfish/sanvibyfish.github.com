---
layout: post
title: "通过 Homebrew 安装 MySQL 的方法"
description: ""
category: ""
tags: []
comments: true
---
###1. install from brew
```
$ brew install mysql
```

###2. 创建或修改/usr/local/etc/my.cnf 下面这个是个例子
```
[client]
port = 3306
socket = /tmp/mysql.sock
default-character-set = utf8

[mysqld]
collation-server = utf8_unicode_ci
character-set-server = utf8
init-connect ='SET NAMES utf8'
max_allowed_packet = 64M
bind-address = 127.0.0.1
port = 3306
socket = /tmp/mysql.sock
innodb_file_per_table=1

[mysqld_safe]
timezone = '+0:00'
```

###3. init database

```
$ unset TMPDIR
$ mysql_install_db --verbose --user=`whoami` --basedir="$(brew --prefix mysql)" --datadir=/usr/local/var/mysql --tmpdir=/tmp
```

###4. start mysql

```
$ mkdir -p ~/Library/LaunchAgents
$ cp /usr/local/Cellar/mysql/5.5.20/homebrew.mxcl.mysql.plist ~/Library/LaunchAgents/
$ launchctl load -w ~/Library/LaunchAgents/homebrew.mxcl.mysql.plist
```

###5. secure mysql

```
# 按照提示一步一步执行
$ mysql_secure_installation
```

###6. Change the root password if you need

```
$ mysqladmin -uroot -p'old_passowrd' password "new_password"
```