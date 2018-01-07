# `dotfiles-rust-role`

[![Build Status](https://travis-ci.org/thecjharries/dotfiles-rust-role.svg?branch=master)](https://travis-ci.org/thecjharries/dotfiles-rust-role)

## Requirements

Fedora 27 is recommended.

## Role Variables

Defaults are below.

```yml
---
owning_user: "{{ ansible_user }}"
owning_group: "{{ ansible_user }}"
root_dir: "/home/{{ ansible_user }}"
config_dir: "{{ root_dir }}/.config"

rustup_src_path: /opt/installers/rustup
```

Additionally, these `vars` are set:

```yml
---
rust_packages:
  - exa
```

## Dependencies

```yml
---
- src: git+https://github.com/thecjharries/dotfiles-common-software-role.git
```

## Example Playbook

```yml
---
- hosts: all

  roles:
    - role: dotfiles-rust-role
```

## License

ISC