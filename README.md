# ansible-gutenberg-pi

This is an Ansible project that aims to allow me to configure my Raspberry Pi based printing server using CUPS.

## Playbooks

`main.yaml` is the main playbook, as the name would suggest. There are a couple more playbooks however:

- `update.yaml`: keeps packages up-to-date
- `debug_facts.yaml`: to display Ansible facts easily

## How to run

```
ansible-playbook main|update|debug_facts.yaml [--ask-pass] [--check]
```

> :warning: **Note**: Unless you set up a key (`authorized_keys`) beforehand, Ansible will require `--ask-pass` flag in order to establish a SSH connection.

## TODO:

- [x] SSH security concerns
- [x] Package update/upgrade
- [x] Raspberry Pi specific configurations
- [x] Configure current static IP in dhcpcd
- [x] cups
  - [x] windows (samba) discovery
    - [ ] samba hardening
    - [ ] expose share to network
  - [ ] macos/ios discovery
- [ ] printer-specific roles/plays
- [ ] sane?
- [ ] drop files to network folder to print?
