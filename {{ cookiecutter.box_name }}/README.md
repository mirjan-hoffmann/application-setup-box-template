# {{ cookiecutter.app_name }} Setup

Install and update {{ cookiecutter.app_name }} automatically via [Ansible](https://www.ansible.com/). Integrate it into your CI/CD process or test it locally with [Vagrant](https://www.vagrantup.com) and [VirtualBox](https://www.virtualbox.org).

## Integration into a CI/CD process

Scenario: Install {{ cookiecutter.app_name }} automatically on an existing system like your Test/Prod system.

TODO will follow soon

## Local installation with Vagrant for testing

Scenario: To test {{ cookiecutter.app_name }} a little bit with minimal effort, you can use a local installation in the local VirtualBox VM via Vargant. This is also suitable for developers to perform "system tests" for their changes.

Prerequisites
* [Git](https://git-scm.com/downloads)
* [Vagrant](https://www.vagrantup.com/downloads.html)
* [VirtualBox](https://www.virtualbox.org/wiki/Downloads)

Perform the following steps in the terminal (Linux / macOS) or in the GitBash (Windows):
```bash
git clone {{ cookiecutter.repo_url }}.git
cd {{ cookiecutter.box_name }}
vagrant up
```

When the installation is complete, {{ cookiecutter.app_name }} will be running on
* {{ cookiecutter.vagrant_box_ip }}

### Helpful Vagrant commands

* `vagrant up` - Creates a new VM and runs the Ansible playbook, if no VM exists. Turn on a shut down VM, if the VM was created before
* `vagrant halt` - Shuts down the VM
* `vagrant destroy` - Removes the VM
* `vagrant provision` - Re-runs the Ansible playbook without restarting the VM
* `vagrant reload --provision` - Restarts the VM and re-runs the Ansible playbook 
* `vagrant ssh` - SSH into the running VM

