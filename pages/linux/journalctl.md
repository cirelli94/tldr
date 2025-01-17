# journalctl

> Query the systemd journal.

- Show all messages from this boot:

`journalctl -b`

- Show all messages from last boot:

`journalctl -b -1`

- Follow new messages (like `tail -f` for traditional syslog):

`journalctl -f`

- Show all messages by a specific unit:

`journalctl -u {{unit}}`

- Filter messages within a time range (either timestamp or placeholders like "yesterday"):

`journalctl --since {{now|today|yesterday|tomorrow}} --until {{YYYY-MM-DD HH:MM:SS}}`

- Show all messages by a specific process:

`journalctl _PID={{pid}}`

- Show all messages by a specific executable:

`journalctl {{path/to/executable}}`

- Show all messages of a specified priority or above (0: emerg, 1: alert, 2: crit, 3: err, 4: warning, 5: notice, 6: info, 7: debug):

`journalctl -p err` or `journalctl -p 3`
