# ansible-role-openhab

A brief description of the role goes here.

# Requirements

None

# Role Variables

| Variable | Description | Default |
|----------|-------------|---------|
| `openhab_user` | User of `openhab` | `{{ __openhab_user }}` |
| `openhab_group` | Group of `openhab` | `{{ __openhab_group }}` |
| `openhab_extra_groups` | A list of extra group for `openhab_user` | `[]` |
| `openhab_log_dir` | Path to log directory | `{{ __openhab_log_dir }}` |
| `openhab_db_dir` | Path to database directory | `{{ __openhab_db_dir }}` |
| `openhab_service` | Service name of `openhab` | `{{ __openhab_service }}` |
| `openhab_package_name` | Package name of `openhab` | `{{ __openhab_package_name }}` |
| `openhab_extra_packages` | A list of extra packages to install | `[]` |
| `openhab_conf_dir` | Path to configuration directory | `{{ __openhab_conf_dir }}` |
| `openhab_configs` | See below | `[]` |
| `openhab_flags` | | `""` |


### `openhab_configs`

This is a list of configuration items. An item is a representation of a
configuration file. Files are created under `openhab_conf_dir`. An item is a
dict of the following keys and values.

| Key | Description | Mandatory? |
|-----|-------------|------------|
| `name` | Relative path to configuration file. An example: if the value is `services/foo.cfg`, the path will be `{{ openhab_conf_dir }}/services/foo.cfg`. | Yes |
| `state` | Create a file if the value is `present` or delete it if `absent`. | No |
| `content` | Raw content of the file. | No |

## Debian

| Variable | Default |
|----------|---------|
| `__openhab_user` | `openhab` |
| `__openhab_group` | `openhab` |
| `__openhab_log_dir` | `/var/log/openhab` |
| `__openhab_package_name` | `openhab2` |
| `__openhab_service` | `openhab2` |
| `__openhab_db_dir` | `/var/lib/openhab2` |
| `__openhab_conf_dir` | `/etc/openhab2` |

## FreeBSD

| Variable | Default |
|----------|---------|
| `__openhab_user` | `openhab` |
| `__openhab_group` | `openhab` |
| `__openhab_log_dir` | `/var/log/openhab` |
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
