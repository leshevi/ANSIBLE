# ansible

`ansible --version`

```
  python version = 3.10.10 (main, Feb  8 2023, 00:00:00) [GCC 12.2.1 20221121 (Red Hat 12.2.1-4)] (/usr/bin/python)
  jinja version = 3.1.2
  libyaml = True
```

## ansible commands

`ansible all -m setup` - gather facts

`ansible yandex -m ping` - ping all hosts in group yandex

`ansible -i inventories/dev/hosts.yml  yandex -a "uname -a"` - uname -a all hosts

`ansible -i inventories/dev/hosts.yml all --list` - lists all hosts from inventory file

```
ansible yandex -a "sudo apt-get update"
ansible yandex -a "sudo apt-get -y upgrade"
ansible yandex -a "sudo apt-get -y autoclean"
```

## ansible playbook

`ansible-playbook playbook.yml` run playbook

## Molecule roles

`molecule init role -d docker ansible.role_system_update --lint-name=yamllint --verifier-name=testinfra --provisioner-name=ansible` - init
