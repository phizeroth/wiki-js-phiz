---
title: journalctl
description: journalctl may be used to query the contents of the systemd journal as written by systemd-journald.service.
published: true
date: 2020-08-05T03:58:12.233Z
tags: linux, server
editor: markdown
---

Journal logs are located in `/var/log/journal`.

Determine journal logs disk usage:

<div class="code-toolbar">
  <pre class="prismjs language-shell-session no-line-numbers"><code>
		$ journalctl --disk-usage
  </code></pre>
</div>

You can control the size of this directory using this parameter in your `/etc/systemd/journald.conf`:

<div class="code-toolbar">
  <pre class="prismjs language- no-line-numbers"><code>
		SystemMaxUse=500M
  </code></pre>
</div>

To limit log files to a specific size systemd provides a vacuum feature to "suck out" older information from log files. The parameters allowed are:

<div class="code-toolbar">
  <pre class="prismjs language- no-line-numbers"><code>
		--vacuum-size=BYTES   Reduce disk usage below specified size
		--vacuum-files=INT    Leave only the specified number of journal files
		--vacuum-time=TIME    Remove journal files older than specified time
  </code></pre>
</div>