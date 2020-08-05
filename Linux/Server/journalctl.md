---
title: journalctl
description: journalctl may be used to query the contents of the systemd journal as written by systemd-journald.service.
published: true
date: 2020-08-05T03:01:44.953Z
tags: linux, server
editor: markdown
---

Journal logs are located in `/var/log/journal`.

Determine journal logs disk usage:

```bash
$ journalctl --disk-usage
```

You can control the size of this directory using this parameter in your `/etc/systemd/journald.conf`:

```
SystemMaxUse=500M
```

To limit log files to a specific size systemd provides a vacuum feature to "suck out" older information from log files. The parameters allowed are:

```
 --vacuum-size=BYTES   Reduce disk usage below specified size
 --vacuum-files=INT    Leave only the specified number of journal files
 --vacuum-time=TIME    Remove journal files older than specified time
 ```