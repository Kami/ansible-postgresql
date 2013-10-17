# Ansible PostgreSQL playbook

This is an Ansible playbook for deploying PostgreSQL 9.1, 9.2 or 9.3.

This playbook was tested on Ubuntu 12.04 x86_64.

## Features

* Install PostgreSQL
* Install development headers (optional)
* Install pgbouncer (optional)

## Notes

* pgbouncer uses md5 authentication but doesn't install a userlist.txt file
  (you need to do this as part of your other playbook)

## Requirements

This playbook requires Ansible 1.2 or higher.

## group_vars

Variables which can be configured are located in the `group_vars/all` file.

Supported PostgreSQL versions:

* `9.1`
* `9.2`
* `9.3`

## Running playbook

```bash
ansible-playbook -i ansible.host setup.yml
```

## License

This playbook is distributed under the
[Apache 2.0 license](http://www.apache.org/licenses/LICENSE-2.0.html).
