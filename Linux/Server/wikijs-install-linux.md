---
title: Wiki.js Installation
description: Wiki.js installation on a Linux/Nginx server
published: true
date: 2020-08-06T06:42:32.711Z
tags: linux, server, wiki.js
editor: markdown
---

This is a basic Node server install on Linux / Nginx on port 3000. For a Docker install, go to https://docs.requarks.io/install/docker. Thanks to my overall inexperience I could **not** for the life of me get Nginx to serve both the Docker *and* the rest of the static website.

## Basic Linux Installation

PostgreSQL is highly recommended by Wiki.js for best performance and future compatibility.
### Install PostgreSQL
```shell-session
$ sudo apt install postgresql libpq-dev postgresql-client postgresql-client-common
```

### Install Wiki.js
```shell-session
$ sudo mkdir /var/wiki;
cd /var/wiki;
sudo wget https://github.com/Requarks/wiki/releases/download/2.4.107/wiki-js.tar.gz;   
sudo tar xzf /var/wiki/wiki-js.tar.gz -C /var/wiki
```

### Copy default config file and modify
```shell-session
$ sudo mv /var/wiki/config.sample.yml /var/wiki/config.yml
$ sudo vim /var/wiki/config.yml
```

config.yml:
```yaml
# Database
port: 3000
db:
	type: postgres
  host: localhost
  port: 5432
  user: wikijs
  pass: <db_password>
  db: wiki
  ssl: false
 
# SSL/TLS Settings
ssl:
	enabled: true
  port: 3443
  provider: letsencrypt
  domain: wiki.phiz.io
  subscriberEmail: <my@email.com>
```

### Set up PostgreSQL database

Create database user `wikijs` and enter a password (same as <db_password> in the config.yml):
```shell-session
$ sudo su postgres;
createuser --pwprompt wikijs
```

Create the database:
```shell-session
$ createdb -O wikijs wiki
```

## Nginx reverse proxy to the subdomain

Create a `wiki.phiz.io` file entry in `/etc/nginx/sites-available/`:
```nginx
server {
    server_name  wiki.phiz.io;

    location / {
        proxy_set_header Host $http_host;
        proxy_set_header X-Real-IP $remote_addr;
        proxy_pass http://localhost:3000;
        proxy_http_version 1.1;
        proxy_set_header Upgrade $http_upgrade;
        proxy_set_header Connection "upgrade";
        proxy_next_upstream error timeout http_502 http_503 http_504;
    }
}
```

Symlink to sites-enabled:
```shell-session
$ sudo ln -s /etc/nginx/sites-available/wiki.phiz.io /etc/nginx/sites-enabled/wiki.phiz.io
```

Reload Nginx:
```shell-session
$ service nginx restart
```

Finally, add an **A record** to your DNS panel for the subdomain, pointing to the server host IP address.
<br />

### Set up SSL certificate
Run `sudo certbot` and select the subdomain to generate a certificate. Choose option 2 to always redirect http to https.
<br />

## Start the Wiki.js server

The server can be started simply with `node server`. However, for long-term deployment it should be run as a service or with a process manager such as `pm2`:
```shell-session
$ pm2 start server
```

Wiki.js should now be accessible at https://wiki.phiz.io!
<br />

## References
- [Linux | Wiki.js Docs *Official guide for installation, which does not include instructions for PostgreSQL setup*](https://docs.requarks.io/install/linux)
- [Simple PostgreSQL setup for Wiki.js? *Excxellent answer by /u/chronos280 describing basic Wiki.js setup with PostgreSQL*](https://www.reddit.com/r/selfhosted/comments/hhmec4/simple_postgresql_setup_for_wikijs/fwdqi8t/)
{.links-list}