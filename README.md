## Ansible Role - Minimal CentOS

![Ansible Lint](https://github.com/hubvu/minimal-centos-ansible/workflows/Ansible%20Lint/badge.svg?branch=main)

### What is this?

* This is a simple Ansible role that checks and removes unneeded packages from a minimal CentOS installation.

```
.
├── ansible.cfg
├── become-secret
├── hosts
├── LICENSE.md
├── minimal_centos.yaml
├── README.md
├── roles
│   └── minimal_centos
│       ├── defaults
│       │   └── main.yml
│       ├── handlers
│       │   └── main.yml
│       ├── meta
│       │   └── main.yml
│       ├── README.md
│       ├── tasks
│       │   └── main.yml
│       ├── tests
│       │   ├── inventory
│       │   └── test.yml
│       └── vars
│           └── main.yml
└── site.yaml
```

### Optional Dependency

* The `minimal_centos.yaml` playbook uses [Ansible Vault](https://docs.ansible.com/ansible/latest/user_guide/vault.html) to encrypt and store sensitive content at rest - such as the `ansible_sudo_pass` variable. This would then require passing the `--ask-vault-pass` flag when running the playbook to decrypt your vault and access secret to become `sudo`. 

### How to get started?

1. Clone the repository > `git clone git@github.com:hubvu/minimal-centos-ansible.git`
2. Navigate into the working directory > `cd ../minimal-centos-ansible/`
3. [Optional] - if you are using Ansible Vault, ensure that you have created the secret and added it to the `minimal_centos.yaml` playbook.
4. Run the `site.yaml` playbook > `ansible-playbook site.yaml --ask-vault-pass --inventory-file hosts` or `ansible-playbook site.yaml --ask-become-pass --inventory-file hosts` if you are not using Ansible Vault.
