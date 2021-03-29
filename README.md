# Ansible amtega.lvm_vg role

This is an [Ansible](http://www.ansible.com) role which manage lvm volume groups through the lvg module.

## Requirements


[Ansible 2.7+](http://docs.ansible.com/ansible/latest/intro_installation.html)

## Role Variables
>

A list of all the default variables for this role is available in `defaults/main.yml`.


## Usage


This is an example playbook:

```yaml
---

- hosts: all
  roles:
    - amtega.lvm_vg
  vars:
      lvm_vg_test:
            - vg: testing
              pvs: /dev/sdb1
              pesize: "4"
              state: present
          lvm_vg_load_from_hostvars: yes
```

## Testing

Tests are based on [molecule with vagrant virtual machines](https://molecule.readthedocs.io/en/latest/installation.html).
Required amtega.parted module to prepare tasks.

```shell
cd amtega.lvm_vg

molecule test --all
```

## License

Copyright (C) 2021 AMTEGA - Xunta de Galicia

This role is free software: you can redistribute it and/or modify it under the terms of:

GNU General Public License version 3, or (at your option) any later version; or the European Union Public License, either Version 1.2 or – as soon they will be approved by the European Commission ­subsequent versions of the EUPL.

This role is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU General Public License for more details or European Union Public License for more details.

## Author Information

- José Enrique Mourón Regueira.
