# DevStack PXE 

This repo contains PXE related configuration files, for booting a Ubuntu 14.04 node
and having it automatically configure itself for use with DevStack.

[For more information, check out my blog post](http://coreitpro.com/2015/11/11/devstack-home-lab-pt1.html)


# Ansible roles

[ansible-sshd is used to set up sshd configuration after the initial
install](https://github.com/nickjj/ansible-sshd), and will be
required.

To install `ansible-sshd` do the following:

```
ansible-galaxy install nickjj.sshd
```

Invocation: 

```
ansible-playbook -b -v -k -K -i inventory/inventory.yml playbooks/playbook.yml
```
