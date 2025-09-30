# Ansible Role: `gcoop-libre.fernet`




See details of changes in [`CHANGELOG.md`](CHANGELOG.md).

## Requirements

- `cryptography`
- `openssl`
- `pyinstaller`
- `python3-pip`
- `python3-virtualenv`

## Role Variables

Available variables with default values in `defaults/main.yml`.

## Dependencies

None.

## Example Playbook

If you want to pinning apt packages.

```yaml
---

- name: Install Fernet
  hosts: [all]

  roles:
    - role: gcoop-libre.fernet
```

## Example Build Commands

This _role_ generate a _random_ **Fernet Encryption Key** and build
_Pipe Encrypt_ (`pe`) and _Pipe Decrypt_ (`pd`) commands:


```bash

echo TestEncryptDecrypt | pe
gAAAAABo23gUKjNPoJ3OVYhEl4r628vBC_hT4BdjEUoPKMEwnwfC9TKlMT32l9noX37A-VweaOgzVMl2SCMGy2oaPcmARsxjcFy3plgMYFNdJu1KTWRAI30=

echo gAAAAABo23gUKjNPoJ3OVYhEl4r628vBC_hT4BdjEUoPKMEwnwfC9TKlMT32l9noX37A-VweaOgzVMl2SCMGy2oaPcmARsxjcFy3plgMYFNdJu1KTWRAI30= | pd
TestEncryptDecrypt

echo TestEncryptDecrypt | pe | pd
TestEncryptDecrypt

```

## License

GNU General Public License, GPLv3.

## Author Information

This role was created in 2025 by
 [Osiris Alejandro Gomez](https://osiux.com/), worker cooperative of
 [gcoop Cooperativa de Software Libre](https://www.gcoop.coop/).
