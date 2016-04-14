# Role Name: NTP

Installs NTP on RedHat/CentOS.

## Requirements

None.

## Role Variables

### `defaults/main.yml`
*default lower priority variables for this role*

* `ntp_enabled: true`
* `ntp_timezone: Asia/Shanghai`

* `ntp_servers:`
    ```
      - ntp.fudan.edu.cn prefer
      - ntp.api.bz
      - 127.127.1.0
    ```

### `vars/RedHat.yml`

* `ntp_daemon: ntpd`

## Dependencies

None.

## Example Playbook

    - name: Install NTP
      hosts: servers
      vars:
        ntp_timezone: Asia/Shanghai
        ntp_servers:
          - 192.168.100.1
      roles:
        - ntp

## License

MIT / BSD

## Author Information

z@zstack.net
