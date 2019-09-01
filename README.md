# ansible-role-openhab

A brief description of the role goes here.

# Requirements

None

# Role Variables

| Variable | Description | Default |
|----------|-------------|---------|
| `openhab_user` | | `openhab` |
| `openhab_group` | | `openhab` |
| `openhab_extra_groups` | | `[]` |
| `openhab_log_dir` | | `/var/log/openhab` |
| `openhab_db_dir` | | `{{ __openhab_db_dir }}` |
| `openhab_service` | | `{{ __openhab_service }}` |
| `openhab_package_name` | | `{{ __openhab_package_name }}` |
| `openhab_extra_packages` | | `[]` |
| `openhab_conf_dir` | | `{{ __openhab_conf_dir }}` |
| `openhab_conf_file` | | `{{ __openhab_conf_dir }}/openhab.conf` |
| `openhab_flags` | | `""` |


## Debian

| Variable | Default |
|----------|---------|
| `__openhab_package_name` | `openhab2` |
| `__openhab_service` | `openhab2` |
| `__openhab_db_dir` | `/var/lib/openhab2` |
| `__openhab_conf_dir` | `/etc/openhab2` |

## FreeBSD

| Variable | Default |
|----------|---------|
| `__openhab_package_name` | `openhab2` |
| `__openhab_service` | `openhab2` |
| `__openhab_db_dir` | `/var/db/openhab2` |
| `__openhab_conf_dir` | `/usr/local/etc/openhab2` |

# Dependencies

None

# Example Playbook

```yaml
```

# License

```
Copyright (c) 2019 Tomoyuki Sakurai <y@trombik.org>

Permission to use, copy, modify, and distribute this software for any
purpose with or without fee is hereby granted, provided that the above
copyright notice and this permission notice appear in all copies.

THE SOFTWARE IS PROVIDED "AS IS" AND THE AUTHOR DISCLAIMS ALL WARRANTIES
WITH REGARD TO THIS SOFTWARE INCLUDING ALL IMPLIED WARRANTIES OF
MERCHANTABILITY AND FITNESS. IN NO EVENT SHALL THE AUTHOR BE LIABLE FOR
ANY SPECIAL, DIRECT, INDIRECT, OR CONSEQUENTIAL DAMAGES OR ANY DAMAGES
WHATSOEVER RESULTING FROM LOSS OF USE, DATA OR PROFITS, WHETHER IN AN
ACTION OF CONTRACT, NEGLIGENCE OR OTHER TORTIOUS ACTION, ARISING OUT OF
OR IN CONNECTION WITH THE USE OR PERFORMANCE OF THIS SOFTWARE.
```

# Author Information

Tomoyuki Sakurai <y@trombik.org>

This README was created by [qansible](https://github.com/trombik/qansible)
