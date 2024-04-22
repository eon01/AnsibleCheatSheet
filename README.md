<div align="center">
    <h1>The Ansible Cheat Sheet</h1>
    <p>A cheat sheet for Ansible, the automation tool.</p>
    <p>Let's create the largest and most comprehensive cheat sheet for Ansible. If you have a tip or trick that you think should be included, please contribute.</p>
</div>

<br/>

<div align="center">
    <img src="https://img.shields.io/github/stars/eon01/AnsibleCheatSheet?style=social"/>
    <img src="https://img.shields.io/github/forks/eon01/AnsibleCheatSheet?style=social"/>
    <img src="https://img.shields.io/github/watchers/eon01/AnsibleCheatSheet?style=social"/>
    <img src="https://img.shields.io/github/last-commit/eon01/AnsibleCheatSheet?style=social"/>
    <img src="https://img.shields.io/github/contributors/eon01/AnsibleCheatSheet?style=social"/>
</div>

<br/>

<div align="center">

![X (formerly Twitter) URL](https://img.shields.io/twitter/url?url=https%3A%2F%2Fgithub.com%2Feon01%2FAnsibleCheatSheet)
![X (formerly Twitter) Follow](https://img.shields.io/twitter/follow/%40joinFAUN)

</div>

# Sponsors

## ❤️ The ansible Workshop: Hands-On Learning For Rapid Mastery

In "The Ansible Workshop," you will deep dive into the world of Ansible, the amazing automation tool that converts complex IT tasks into a set of easy, simple-to-repeat steps. This guide is your roadmap to mastering Ansible, whether you are a novice just starting to use Ansible or an intermediate user who has already used Ansible and is looking for additional information and tricks to enhance your skills.

You can get it on [Amazon](https://amzn.to/3watGU8)

## 📩 DevOpsLinks: The Ultimate DevOps Newsletter

[DevOpsLinks](https://faun.dev/newsletter/devopslinks) - The Ultimate DevOps Newsletter. Curated DevOps news, tutorials, tools, jobs, podcasts, and more. Delivered to your inbox every week.

## 🛍️ ByteVibe: Show off your love for all things TECH

If you're seeking a cozy sweatshirt to wear during your extended coding sessions or a mug to exhibit your passion for programming, [you can find it all here](https://bytevibe.co/)

## 💌 Sponsorship

If you would like to sponsor this project, please contact me at aymen at faun dot dev.

# Call for Contributions

Let's create the largest and most comprehensive list of Ansible tools and resources. If you have a tool or resource that you think should be included, please contribute.

# Table of Contents

- [Sponsors](#sponsors)
  - [❤️ The ansible Workshop: Hands-On Learning For Rapid Mastery](#️-the-ansible-workshop-hands-on-learning-for-rapid-mastery)
  - [📩 DevOpsLinks: The Ultimate DevOps Newsletter](#-devopslinks-the-ultimate-devops-newsletter)
  - [🛍️ ByteVibe: Show off your love for all things TECH](#️-bytevibe-show-off-your-love-for-all-things-tech)
  - [💌 Sponsorship](#-sponsorship)
- [Call for Contributions](#call-for-contributions)
- [Table of Contents](#table-of-contents)
- [The Ansible Cheat Sheet](#the-ansible-cheat-sheet)
  - [Installing Ansible](#installing-ansible)
    - [On Linux](#on-linux)
    - [On macOS](#on-macos)
    - [On Windows](#on-windows)
  - [Configuring Ansible](#configuring-ansible)
  - [Inventory](#inventory)
    - [Setting Up the Inventory File (INI)](#setting-up-the-inventory-file-ini)
    - [Setting Up the Inventory File (YAML)](#setting-up-the-inventory-file-yaml)
  - [Ansible Host Variables](#ansible-host-variables)
  - [Testing Your Setup](#testing-your-setup)
  - [Playbook Structure](#playbook-structure)
  - [Playbook Keywords](#playbook-keywords)
  - [Common Modules](#common-modules)
    - [Running a Command](#running-a-command)
    - [Running a Shell Command](#running-a-shell-command)
    - [Running a Raw Command](#running-a-raw-command)
    - [Copying a File](#copying-a-file)
    - [Installing a Package](#installing-a-package)
    - [Restarting a Service](#restarting-a-service)
    - [Copying a File with Permissions](#copying-a-file-with-permissions)
    - [Copying a File with Permissions and Context](#copying-a-file-with-permissions-and-context)
  - [Playbooks](#playbooks)
    - [Running a Playbook](#running-a-playbook)
    - [Running a Playbook with Inventory](#running-a-playbook-with-inventory)
    - [Running a Playbook with Inventory and Limit](#running-a-playbook-with-inventory-and-limit)
    - [Running a Playbook with Limit](#running-a-playbook-with-limit)
    - [Running a Playbook with Tags](#running-a-playbook-with-tags)
    - [Running a Playbook with Skip Tags](#running-a-playbook-with-skip-tags)
    - [Running a Playbook with Extra Variables](#running-a-playbook-with-extra-variables)
    - [Running a Playbook with a Vault Password File](#running-a-playbook-with-a-vault-password-file)
    - [Running a Playbook with Ask Vault Password](#running-a-playbook-with-ask-vault-password)
    - [Running a Playbook with Ask Sudo Password](#running-a-playbook-with-ask-sudo-password)
    - [Running a Playbook with Ask Pass](#running-a-playbook-with-ask-pass)
    - [Running a Playbook in Check Mode](#running-a-playbook-in-check-mode)
    - [Running a Playbook in Diff Mode](#running-a-playbook-in-diff-mode)
    - [Running a Playbook in Verbose Mode](#running-a-playbook-in-verbose-mode)
    - [Running a Playbook in Extra Verbose Mode](#running-a-playbook-in-extra-verbose-mode)
    - [Running a Playbook in Extra Extra Verbose Mode](#running-a-playbook-in-extra-extra-verbose-mode)
    - [Running a Playbook in Extra Extra Extra Verbose Mode](#running-a-playbook-in-extra-extra-extra-verbose-mode)
    - [Running a Playbook in Extra Extra Extra Extra Verbose Mode](#running-a-playbook-in-extra-extra-extra-extra-verbose-mode)
    - [Running a Playbook with Forks](#running-a-playbook-with-forks)
    - [Running a Playbook with Timeout](#running-a-playbook-with-timeout)
  - [Jinja2](#jinja2)
    - [Using Jinja2](#using-jinja2)
    - [Using Jinja2 with Filters](#using-jinja2-with-filters)
    - [Jinja2 Template](#jinja2-template)
    - [Jinja2 Template with Variables](#jinja2-template-with-variables)
    - [Templates with Loops](#templates-with-loops)
    - [Templates with Conditionals](#templates-with-conditionals)
    - [Templates with Filters](#templates-with-filters)
  - [Host Patterns](#host-patterns)
  - [Debugging](#debugging)
    - [Syntax Check a Playbook](#syntax-check-a-playbook)
    - [Check if Hosts Are Reachable](#check-if-hosts-are-reachable)
    - [Check if Hosts Are Reachable with SSH](#check-if-hosts-are-reachable-with-ssh)
    - [Check if Hosts Are Reachable with WinRM](#check-if-hosts-are-reachable-with-winrm)
    - [Check if Hosts Are Reachable Locally](#check-if-hosts-are-reachable-locally)
    - [Verbose Mode](#verbose-mode)
    - [Debug Mode](#debug-mode)
    - [Capture Output](#capture-output)
    - [Capture Output and Show Only Specific Fields](#capture-output-and-show-only-specific-fields)
    - [Capture Output and Show Only Specific Fields with Jinja2](#capture-output-and-show-only-specific-fields-with-jinja2)
  - [Gathering Facts](#gathering-facts)
    - [Gathering Facts for All Hosts](#gathering-facts-for-all-hosts)
    - [Gathering Facts for a Specific Host](#gathering-facts-for-a-specific-host)
    - [Gathering Facts for a Specific Host and Saving to a File](#gathering-facts-for-a-specific-host-and-saving-to-a-file)
  - [Variables](#variables)
    - [Setting a Variable](#setting-a-variable)
    - [Setting a Variable with Multiple Lines](#setting-a-variable-with-multiple-lines)
    - [Setting a Variable with Multiple Lines and Indentation](#setting-a-variable-with-multiple-lines-and-indentation)
  - [Conditionals](#conditionals)
    - [When](#when)
    - [When with Multiple Conditions](#when-with-multiple-conditions)
  - [Loops](#loops)
    - [Looping Over a List](#looping-over-a-list)
    - [Looping Over a Dictionary](#looping-over-a-dictionary)
    - [Looping Over a Dictionary Using "with\_dict"](#looping-over-a-dictionary-using-with_dict)
    - [Looping Over a List with "with\_items"](#looping-over-a-list-with-with_items)
  - [Handlers](#handlers)
    - [Using Handlers](#using-handlers)
    - [Using Handlers with Multiple Tasks](#using-handlers-with-multiple-tasks)
    - [Using Handlers with Multiple Tasks and Different Handlers](#using-handlers-with-multiple-tasks-and-different-handlers)
  - [Conditional Execution](#conditional-execution)
    - [Using "ignore\_errors" to Continue Execution Even After Failures](#using-ignore_errors-to-continue-execution-even-after-failures)
    - [Using "changed\_when" to Control When a Task Is Considered Changed](#using-changed_when-to-control-when-a-task-is-considered-changed)
    - [Using "failed\_when" to Control When a Task Is Considered Failed](#using-failed_when-to-control-when-a-task-is-considered-failed)
    - [Failing a Playbook with "fail"](#failing-a-playbook-with-fail)
  - [Vault](#vault)
    - [Editing an Encrypted File](#editing-an-encrypted-file)
    - [Updating Encryption Password](#updating-encryption-password)
    - [Viewing an Encrypted File](#viewing-an-encrypted-file)
    - [Encrypting a File](#encrypting-a-file)
    - [Encrypting a File with a Password File](#encrypting-a-file-with-a-password-file)
    - [Decrypting a File](#decrypting-a-file)
    - [Encrypting a String](#encrypting-a-string)
    - [Encrypting a String with a Password File](#encrypting-a-string-with-a-password-file)
  - [Asynchronous Tasks](#asynchronous-tasks)
    - [Running a Task Asynchronously](#running-a-task-asynchronously)
    - [Checking the Status of Asynchronous Tasks](#checking-the-status-of-asynchronous-tasks)
  - [Roles](#roles)
    - [Creating a Role](#creating-a-role)
    - [Using a Role](#using-a-role)
    - [Using a Role with Variables](#using-a-role-with-variables)
    - [Using a Role with Multiple Variables](#using-a-role-with-multiple-variables)
    - [Using a Role with Tags](#using-a-role-with-tags)
  - [Ansible Galaxy](#ansible-galaxy)
    - [Searching for Roles](#searching-for-roles)
    - [Installing a Role](#installing-a-role)
    - [Installing a Role with a Specific Version](#installing-a-role-with-a-specific-version)
  - [Ansible Collections](#ansible-collections)
    - [Installing a Collection](#installing-a-collection)
    - [Installing a Collection with a Specific Version](#installing-a-collection-with-a-specific-version)
    - [Installing a Collection from a File](#installing-a-collection-from-a-file)
    - [Installing a Collection from a Directory](#installing-a-collection-from-a-directory)
  - [Resources About Ansible](#resources-about-ansible)
    - [Official Ansible Documentation](#official-ansible-documentation)
    - [Ansible Blogs and Articles](#ansible-blogs-and-articles)
    - [Ansible Community and Forums](#ansible-community-and-forums)
    - [Ansible GitHub Repository](#ansible-github-repository)
    - [Ansible Videos](#ansible-videos)
    - [Ansible Tools](#ansible-tools)
    - [IDE Extensions](#ide-extensions)
      - [VSCode](#vscode)
      - [PyCharm](#pycharm)
      - [Sublime](#sublime)
      - [Vim](#vim)
    - [Newsletters](#newsletters)

# The Ansible Cheat Sheet

## Installing Ansible

### On Linux

```bash
# Ubuntu/Debian
sudo apt update
sudo apt install ansible
# On Red Hat-based systems (Fedora, CentOS)
sudo yum install ansible
```

Or use pip:

```bash
pip install ansible
```

Or use pipx:

```bash
pipx install ansible
```

### On macOS

Use Homebrew:

```bash
brew install ansible
```

### On Windows

Ansible can be run from inside a Windows Subsystem for Linux (WSL) instance. First, ensure that WSL is installed, then install Ansible in the Linux distribution of your choice, following the Linux installation steps.

## Configuring Ansible

Default Ansible configuration settings can be overridden using environment variables. The same variables can be used to override settings in the `ansible.cfg` file in ini format. Typically, environment variables are in capital letters, while the corresponding configuration settings are in lowercase.

| Environment Variable | ansible.cfg Variable | ansible.cfg Section | Description |
|----------------------|----------------------|---------------------|-------------|
| `ANSIBLE_CONFIG` | N/A | N/A | Specifies the path to the Ansible configuration file. |
| `ANSIBLE_DEBUG` | `debug` | `[defaults]` | Enables or disables debug output. Set to `True` for verbose debug information. |
| `ANSIBLE_INVENTORY` | `inventory` | `[defaults]` | Path to the inventory file or script. |
| `ANSIBLE_NOCOLOR` | `nocolor` | `[defaults]` | Disables colored output in Ansible. |
| `ANSIBLE_FORCE_COLOR` | `force_color` | `[defaults]` | Forces colored output even when not in a TTY. |
| `ANSIBLE_HOST_KEY_CHECKING` | `host_key_checking` | `[defaults]` | Enables or disables SSH host key checking. |
| `ANSIBLE_REMOTE_USER` | `remote_user` | `[defaults]` | Default remote user for SSH connections. |
| `ANSIBLE_PRIVATE_KEY_FILE` | `private_key_file` | `[defaults]` | Specifies the private key file for SSH. |
| `ANSIBLE_TIMEOUT` | `timeout` | `[defaults]` | Connection timeout duration in seconds. |
| `ANSIBLE_ROLES_PATH` | `roles_path` | `[defaults]` | Specifies the path to Ansible roles. |
| `ANSIBLE_LIBRARY` | `library` | `[defaults]` | Path to custom module directories. |
| `ANSIBLE_RETRY_FILES_ENABLED` | `retry_files_enabled` | `[defaults]` | Enables or disables the creation of retry files. |
| `ANSIBLE_VAULT_PASSWORD_FILE` | `vault_password_file` | `[defaults]` | Path to the Ansible vault password file. |
| `ANSIBLE_VAULT_IDENTITY_LIST` | `vault_identity_list` | `[defaults]` | List of vault identities for decryption. |
| `ANSIBLE_STDOUT_CALLBACK` | `stdout_callback` | `[defaults]` | Sets the default callback plugin for output formatting. |
| `ANSIBLE_CALLBACK_WHITELIST` | `callback_whitelist` | `[defaults]` | List of callback plugins allowed to execute. |
| `ANSIBLE_FORKS` | `forks` | `[defaults]` | Number of parallel processes to use. |
| `ANSIBLE_ASK_VAULT_PASS` | `ask_vault_pass` | `[defaults]` | Determines whether Ansible prompts for the vault password by default. |
| `ANSIBLE_TRANSPORT` | `transport` | `[defaults]` | Specifies the connection type (e.g., SSH, WinRM). |
| `ANSIBLE_GATHERING` | `gathering` | `[defaults]` | Configures the default fact gathering behavior. |
| `ANSIBLE_GATHER_SUBSET` | `gather_subset` | `[defaults]` | Specifies a subset of facts to gather. |
| `ANSIBLE_SSH_ARGS` | `ssh_args` | `[ssh_connection]` | Extra arguments to pass to the SSH command. |
| `ANSIBLE_SSH_RETRIES` | `retries` | `[ssh_connection]` | Specifies the number of attempts Ansible will make to connect via SSH before giving up. |
| `ANSIBLE_BECOME` | `become` | `[privilege_escalation]` | Enables or disables privilege escalation. The default is `False`. |
| `ANSIBLE_BECOME_METHOD` | `become_method` | `[privilege_escalation]` | The method used for privilege escalation, the default is `sudo`. |
| `ANSIBLE_BECOME_USER` | `become_user` | `[privilege_escalation]` | The user to become on privilege escalation, the default is `root`. |
| `ANSIBLE_BECOME_ASK_PASS` | `become_ask_pass` | `[privilege_escalation]` | Prompts for a password for privilege escalation, the default is `False`. |
| `ANSIBLE_GALAXY_SERVER` | `server` | `[galaxy]` | Specifies the default Galaxy server from which roles are installed. |
| `ANSIBLE_INVENTORY_ENABLED` | `inventory_enabled` | `[inventory]` | Specifies the enabled inventory plugins. The default is `[‘host_list’, ‘script’, ‘auto’, ‘yaml’, ‘ini’, ‘toml’]`. |

For more detailed information on these configurations, consult the [official Ansible documentation](https://docs.ansible.com/ansible/latest/reference_appendices/config.html#ansible-configuration-settings).

## Inventory

### Setting Up the Inventory File (INI)

```ini
[web]
192.168.1.2 ansible_ssh_user=ubuntu

[db]
192.168.1.3 ansible_ssh_user=root
```

### Setting Up the Inventory File (YAML)

```yaml
all:
  hosts:
    192.168.1.2:
      ansible_ssh_user: ubuntu
    192.168.1.3:
      ansible_ssh_user: root
```

Replace the IP addresses and `ansible_ssh_user` with your server details.

## Ansible Host Variables

| Variable | Description |
|----------|-------------|
| `ansible_connection` | The type of connection to the host. The default is 'smart'. It supports SSH (`smart`, `ssh`, `paramiko`) and other types. |
| `ansible_host` | The hostname or IP to connect to, if different from the alias. |
| `ansible_port` | The connection port number. The default is 22 for SSH. |
| `ansible_user` | The username for connecting to the host. |
| `ansible_password` | The password for authentication (use vault for security). |
| `ansible_ssh_private_key_file` | The private key file for SSH, useful for multiple keys. |
| `ansible_ssh_common_args` | The common arguments appended to sftp, scp, ssh commands. |
| `ansible_sftp_extra_args` | The extra arguments for the sftp command line. |
| `ansible_scp_extra_args` | The extra arguments for the scp command line. |
| `ansible_ssh_extra_args` | The extra arguments for the ssh command line. |
| `ansible_ssh_pipelining` | Whether to use SSH pipelining, overrides ansible.cfg setting. |
| `ansible_ssh_executable` | Overrides the default system ssh, added in version 2.2. |
| `ansible_become` | Forces privilege escalation, equivalent to `ansible_sudo` or `ansible_su`. |
| `ansible_become_method` | Sets the privilege escalation method. |
| `ansible_become_user` | Sets the user for privilege escalation. |
| `ansible_become_password` | Sets the privilege escalation password (use vault for security). |
| `ansible_become_exe` | Sets the executable for the escalation method. |
| `ansible_become_flags` | Flags for the selected escalation method, can be set in ansible.cfg. |
| `ansible_shell_type` | The shell type of the target system. The default is Bourne (sh) compatible. |
| `ansible_python_interpreter` | The Python interpreter path on the target host. |
| `ansible_*_interpreter` | The generic interpreter setting, works like `ansible_python_interpreter`. New in version 2.1. |
| `ansible_shell_executable` | The shell executable Ansible uses on the target, overrides ansible.cfg. |

This table provides a summary of the host-specific variables in Ansible. For detailed information and examples, refer to the [official Ansible documentation](https://docs.ansible.com/ansible/latest/user_guide/intro_inventory.html#host-variables).

## Testing Your Setup

To ensure that Ansible can communicate with your managed nodes, use the `ping` module:

```bash
ansible all -m ping -i inventory
```

## Playbook Structure

```yaml
---
- name: Playbook Name
  hosts: all
  become: yes
  become_user: root
  become_method: sudo
  vars:
    my_var: 123
  vars_files:
    - vars.yml
  tasks:
    - name: Task Name
      command: echo "Hello World!"
```

## Playbook Keywords

| Keyword | Description |
|---------|-------------|
| `name` | The name of the playbook or task. |
| `hosts` | The hosts or host groups to run the playbook on. |
| `become` | Whether to run tasks with privilege escalation. |
| `become_user` | The user to become when using privilege escalation. |
| `become_method` | The method to use for privilege escalation (e.g., sudo). |
| `remote_user` | The user to connect as on the remote host. |
| `vars` | The variables to be used in the playbook. |
| `vars_files` | The files containing variables to be used in the playbook. |
| `tasks` | The list of tasks to be executed. |
| `handlers` | The list of handlers to be executed upon notification. |
| `pre_tasks` | The list of tasks to be executed before roles. |
| `post_tasks` | The list of tasks to be executed after the main tasks. |
| `roles` | The list of roles to be included and executed. |
| `serial` | The number of hosts to process in each playbook run. |
| `max_fail_percentage` | The maximum failure percentage allowed to continue the playbook. |
| `any_errors_fatal` | Whether any error is enough to stop the playbook. |
| `ignore_errors` | Whether to ignore errors on a task. |
| `gather_facts` | Whether to gather facts at the beginning of the playbook. |
| `no_log` | Whether to disable logging for a task. |
| `force_handlers` | Whether to run handlers even if a task fails. |
| `tags` | The tags associated with tasks or roles for selective running. |
| `check_mode` | Whether to run the playbook in check mode (dry run). |
| `diff` | Whether to show differences in tasks where supported. |
| `connection` | The connection type to use (e.g., `ssh`, `local`, `winrm`). |
| `timeout` | The connection timeout duration in seconds. |
| `gather_subset` | The subset of facts to gather (Possible values: `all`, `min`, `hardware`, `network`, `virtual`, `ohai`, and `facter`). |

For detailed information and examples, refer to the [official Ansible documentation](https://docs.ansible.com/ansible/latest/user_guide/playbooks_keywords.html).

## Common Modules

### Running a Command

**Ad-hoc**:

```bash
ansible all -m command -a "uptime"
```

**Playbook**:

```yaml
---
- name: Run a Command
  hosts: all
  tasks:
    - name: Run a Command
      command: uptime
```

### Running a Shell Command

**Ad-hoc**:

```bash
ansible all -m shell -a "echo $TERM"
```

**Playbook**:

```yaml
---
- name: Run a Shell Command
  hosts: all
  tasks:
    - name: Run a Shell Command
      shell: echo $TERM
```

### Running a Raw Command

**Ad-hoc**:

```bash
ansible all -m raw -a "echo $TERM"
```

**Playbook**:

```yaml
---
- name: Run a Raw Command
  hosts: all
  tasks:
    - name: Run a Raw Command
      raw: echo $TERM
```

### Copying a File

**Ad-hoc**:

```bash
ansible all -m copy -a "src=/etc/hosts dest=/tmp/hosts"
```

**Playbook**:

```yaml
---
- name: Copy a File
  hosts: all
  tasks:
    - name: Copy a File
      copy:
        src: /etc/hosts
        dest: /tmp/hosts
```

### Installing a Package

**Ad-hoc**:

```bash
ansible all -m apt -a "name=nginx state=present"
```

**Playbook**:

```yaml
---
- name: Install a Package
  hosts: all
  tasks:
    - name: Install a Package
      apt:
        name: nginx
        state: present
```

### Restarting a Service

**Ad-hoc**:

```bash
ansible all -m service -a "name=nginx state=restarted"
```

**Playbook**:

```yaml
---
- name: Restart a Service
  hosts: all
  tasks:
    - name: Restart a Service
      service:
        name: nginx
        state: restarted
```

### Copying a File with Permissions

**Ad-hoc**:

```bash
ansible all -m copy -a "src=/etc/hosts dest=/tmp/hosts owner=root group=root mode=0644"
```

**Playbook**:

```yaml
---
- name: Copy a File with Permissions
  hosts: all
  tasks:
    - name: Copy a File with Permissions
      copy:
        src: /etc/hosts
        dest: /tmp/hosts
        owner: root
        group: root
        mode: 0644
```

### Copying a File with Permissions and Context

**Ad-hoc**:

```bash
ansible all -m copy -a "src=/etc/hosts dest=/tmp/hosts owner=root group=root mode=0644 seuser=system_u serole=object_r"
```

**Playbook**:

```yaml
---
- name: Copy a File with Permissions and Context
  hosts: all
  tasks:
    - name: Copy a File with Permissions and Context
      copy:
        src: /etc/hosts
        dest: /tmp/hosts
        owner: root
        group: root
        mode: 0644
        seuser: system_u
        serole: object_r
```

## Playbooks

### Running a Playbook

```bash
ansible-playbook playbook.yml
```

### Running a Playbook with Inventory

```bash
ansible-playbook playbook.yml -i inventory
```

### Running a Playbook with Inventory and Limit

```bash
ansible-playbook playbook.yml -i inventory --limit "web"
```

### Running a Playbook with Limit

```bash
ansible-playbook playbook.yml --limit "web"
```

### Running a Playbook with Tags

```bash
ansible-playbook playbook.yml --tags "install,configure"
```

### Running a Playbook with Skip Tags

```bash
ansible-playbook playbook.yml --skip-tags "configure"
```

### Running a Playbook with Extra Variables

```bash
ansible-playbook playbook.yml --extra-vars "my_var=123"
```

### Running a Playbook with a Vault Password File

```bash
ansible-playbook playbook.yml --vault-password-file ~/.vault_pass.txt
```

### Running a Playbook with Ask Vault Password

```bash
ansible-playbook playbook.yml --ask-vault-pass
```

### Running a Playbook with Ask Sudo Password

```bash
ansible-playbook playbook.yml --ask-become-pass
```

### Running a Playbook with Ask Pass

```bash
ansible-playbook playbook.yml --ask-pass
```

### Running a Playbook in Check Mode

```bash
ansible-playbook playbook.yml --check
```

### Running a Playbook in Diff Mode

```bash
ansible-playbook playbook.yml --diff
```

### Running a Playbook in Verbose Mode

```bash
ansible-playbook playbook.yml -v
```

### Running a Playbook in Extra Verbose Mode

```bash
ansible-playbook playbook.yml -vv
```

### Running a Playbook in Extra Extra Verbose Mode

```bash
ansible-playbook playbook.yml -vvv
```

### Running a Playbook in Extra Extra Extra Verbose Mode

```bash
ansible-playbook playbook.yml -vvvv
```

### Running a Playbook in Extra Extra Extra Extra Verbose Mode

```bash
ansible-playbook playbook.yml -vvvvv
```

### Running a Playbook with Forks

```bash
ansible-playbook playbook.yml --forks 50
```

### Running a Playbook with Timeout

```bash
ansible-playbook playbook.yml --timeout 30
```

## Jinja2

### Using Jinja2

```yaml
---
- name: Using Jinja2
  hosts: localhost
  vars:
    my_var: 123
  tasks:
    - name: Using Jinja2
      debug:
        msg: "{{ my_var }}"
```

### Using Jinja2 with Filters

```yaml
---
- name: Using Jinja2 with Filters
  hosts: localhost
  vars:
    my_var: 123
  tasks:
    - name: Using Jinja2 with Filters
      debug:
        msg: "{{ my_var | string }}"
```

### Jinja2 Template

```yaml
---
- name: Jinja2 Template
  hosts: localhost
  vars:
    my_var: 123
  tasks:
    - name: Jinja2 Template
      template:
        src: template.j2
        dest: /tmp/template.txt
```

### Jinja2 Template with Variables

```yaml
---
- name: Jinja2 Template with Variables
  hosts: localhost
  vars:
    my_var: 123
  tasks:
    - name: Jinja2 Template with Variables
      template:
        src: template.j2
        dest: /tmp/template.txt
```

The "template.j2" file:

```jinja2
Hello World! This is my_var: {{ my_var }}
```

### Templates with Loops

```yaml
---
- name: Templates with Loops
  hosts: localhost
  vars:
    my_list:
      - 123
      - 456
      - 789
  tasks:
    - name: Templates with Loops
      template:
        src: template.j2
        dest: /tmp/template.txt
```

The "template.j2" file:

```jinja2
{% for item in my_list %}
{{ item }}
{% endfor %}
```

### Templates with Conditionals

```yaml
---
- name: Templates with Conditionals
  hosts: localhost
  vars:
    my_var: 123
  tasks:
    - name: Templates with Conditionals
      template:
        src: template.j2
        dest: /tmp/template.txt
```

The "template.j2" file:

```jinja2
{% if my_var == 123 %}
Hello World!
{% endif %}
```

### Templates with Filters

```yaml
---
- name: Templates with Filters
  hosts: localhost
  vars:
    my_var: 123
  tasks:
    - name: Templates with Filters
      template:
        src: template.j2
        dest: /tmp/template.txt
```

The "template.j2" file:

```jinja2
Hello, World! This is my_var: {{ my_var | string }}
```

## Host Patterns

| Pattern | Description |
|---------|-------------|
| `all` | All hosts in the inventory. |
| `*` | Same as `all`. |
| `group1` | All hosts in the group `group1`. |
| `group1:group2` | All hosts in the groups `group1` and `group2`. |
| `group1:&group2` | All hosts in both `group1` and `group2`. |
| `group1:!group2` | All hosts in `group1` that are not in `group2`. |
| `group1:&group2:!group3` | All hosts in both `group1` and `group2` that are not in `group3`. |
| `group1:group2:&group3` | All hosts in both `group1` and `group2` that are also in `group3`. |
| `group1:group2:!group3:&group4` | All hosts in both `group1` and `group2` that are not in `group3` and are also in `group4`. |

## Debugging

### Syntax Check a Playbook

```bash
ansible-playbook playbook.yml --syntax-check
```

### Check if Hosts Are Reachable

```bash
ansible all -m ping
```

### Check if Hosts Are Reachable with SSH

```bash
ansible all -m ping -c ssh
```

### Check if Hosts Are Reachable with WinRM

```bash
ansible all -m ping -c winrm
```

### Check if Hosts Are Reachable Locally

```bash
ansible all -m ping -c local
```

### Verbose Mode

```bash
ansible all -m ping -v
ansible all -m ping -vv
ansible all -m ping -vvv
ansible all -m ping -vvvv
ansible all -m ping -vvvvv
```

### Debug Mode

```bash
ANSIBLE_DEBUG=1 ansible all -m ping
```

### Capture Output

```yaml
---
- name: Capture Output
  hosts: all
  tasks:
    - name: Capture Output
      command: echo "Hello World!"
      register: output
    - debug:
        var: output
```

### Capture Output and Show Only Specific Fields

```yaml
---
- name: Capture Output and Show Only Specific Fields
  hosts: all
  tasks:
    - name: Capture Output and Show Only Specific Fields
      command: echo "Hello World!"
      register: output
    - debug:
        var: output.stdout
```

### Capture Output and Show Only Specific Fields with Jinja2

```yaml
---
- name: Capture Output and Show Only Specific Fields with Jinja2
  hosts: all
  tasks:
    - name: Capture Output and Show Only Specific Fields with Jinja2
      command: echo "Hello World!"
      register: output
    - debug:
        msg: "{{ output.stdout }}"
```

## Gathering Facts

### Gathering Facts for All Hosts

```bash
ansible all -m setup
```

### Gathering Facts for a Specific Host

```bash
ansible all -m setup -a "filter=ansible_eth*"
```

### Gathering Facts for a Specific Host and Saving to a File

```bash
ansible all -m setup -a "filter=ansible_eth*" --tree /tmp/facts
```

## Variables

### Setting a Variable

```yaml
---
- name: Setting a Variable
  hosts: localhost
  vars:
    my_var: 123
  tasks:
    - name: Setting a Variable
      debug:
        var: my_var
    - name: Setting a Variable (debug)
      debug:
        msg: "{{ my_var }}"
```

### Setting a Variable with Multiple Lines

```yaml
---
- name: Setting a Variable with Multiple Lines
  hosts: localhost
  vars:
    my_var: >
      Hello
      World!
  tasks:
    - name: Setting a Variable with Multiple Lines
      debug:
        var: my_var
    - name: Setting a Variable with Multiple Lines (debug)
      debug:
        msg: "{{ my_var }}"
```

### Setting a Variable with Multiple Lines and Indentation

```yaml
---
- name: Setting a Variable with Multiple Lines and Indentation
  hosts: localhost
  vars:
    my_var: |
      Hello
      World!
        This is indented.
  tasks:
    - name: Setting a Variable with Multiple Lines and Indentation
      debug:
        var: my_var
    - name: Setting a Variable with Multiple Lines and Indentation (debug)
      debug:
        msg: "{{ my_var }}"
```

## Conditionals

### When

```yaml
---
- name: When
  hosts: localhost
  vars:
    my_var: 123
  tasks:
    - name: When
      debug:
        msg: "Hello World!"
      when: my_var == 123
```

### When with Multiple Conditions

```yaml
---
- name: When with Multiple Conditions
  hosts: localhost
  vars:
    my_var: 123
  tasks:
    - name: When with Multiple Conditions
      debug:
        msg: "Hello World!"
      when:
        - my_var == 123
        - my_var != 456
```

## Loops

### Looping Over a List

```yaml
---
- name: Looping Over a List
  hosts: localhost
  vars:
    my_list:
      - 123
      - 456
      - 789
  tasks:
    - name: Looping Over a List
      debug:
        msg: "{{ item }}"
      loop: "{{ my_list }}"
```

### Looping Over a Dictionary

```yaml
---
- name: Looping Over a Dictionary
  hosts: localhost
  vars:
    my_dict:
      key1: 123
      key2: 456
      key3: 789
  tasks:
    - name: Looping Over a Dictionary
      debug:
        msg: "{{ item.key }}: {{ item.value }}"
      loop: "{{ my_dict | dict2items }}"
```

### Looping Over a Dictionary Using "with_dict"

```yaml
---
- name: Looping Over a Dictionary with Nested Items
  hosts: localhost
  vars:
    my_dict:
      key1:
        - 123
        - 456
        - 789
      key2:
        - 123
        - 456
        - 789
      key3:
        - 123
        - 456
        - 789
  tasks:
    - name: Looping Over a Dictionary with Nested Items
      debug:
        msg: "Key: {{ item.key }}, Values: {{ item.value }}"
      with_dict: "{{ my_dict }}"
```

### Looping Over a List with "with_items"

```yaml
---
- name: Looping Over a List with with_items
  hosts: localhost
  vars:
    my_list:
      - 123
      - 456
      - 789
  tasks:
    - name: Looping Over a List with with_items
      debug:
        msg: "{{ item }}"
      with_items: "{{ my_list }}"
```

## Handlers

### Using Handlers

```yaml
---
- name: Using Handlers
  hosts: localhost
  tasks:
    - name: Using Handlers
      debug:
        msg: "Hello World!"
      notify: My Handler
  handlers:
    - name: My Handler
      debug:
        msg: "This is my handler."
```

### Using Handlers with Multiple Tasks

```yaml
---
- name: Using Handlers with Multiple Tasks
  hosts: localhost
  tasks:
    - name: Using Handlers with Multiple Tasks
      debug:
        msg: "Hello World!"
      notify: My Handler
    - name: Using Handlers with Multiple Tasks
      debug:
        msg: "Hello World!"
      notify: My Handler
  handlers:
    - name: My Handler
      debug:
        msg: "This is my handler."
```

### Using Handlers with Multiple Tasks and Different Handlers

```yaml
---
- name: Using Handlers with Multiple Tasks and Different Handlers
  hosts: localhost
  tasks:
    - name: Using Handlers with Multiple Tasks and Different Handlers
      debug:
        msg: "Hello World!"
      notify: My Handler 1
    - name: Using Handlers with Multiple Tasks and Different Handlers
      debug:
        msg: "Hello World!"
      notify: My Handler 2
  handlers:
    - name: My Handler 1
      debug:
        msg: "This is my handler 1."
    - name: My Handler 2
      debug:
        msg: "This is my handler 2."
```

## Conditional Execution

### Using "ignore_errors" to Continue Execution Even After Failures
  
```yaml
---
- name: Using ignore_errors to Continue Execution Even After Failures
  hosts: localhost
  tasks:
    - name: Using ignore_errors to Continue Execution Even After Failures
      command: /bin/false
      ignore_errors: yes
    - name: Using ignore_errors to Continue Execution Even After Failures
      debug:
        msg: "Hello World!"
```

### Using "changed_when" to Control When a Task Is Considered Changed
  
```yaml
---
- name: Using changed_when to Control When a Task Is Considered Changed
  hosts: localhost
  tasks:
    - name: Using changed_when to Control When a Task Is Considered Changed
      command: /bin/false
      register: output
      changed_when: output.rc != 2
    - name: Using changed_when to Control When a Task Is Considered Changed
      debug:
        msg: "Hello World!"
```

### Using "failed_when" to Control When a Task Is Considered Failed
  
```yaml
---
- name: Example playbook with failed_when
  hosts: localhost
  tasks:
    - name: Example playbook with failed_when (will fail)
      command: /bin/false
      register: output
      # The normal exit code for /bin/false is 1             
      failed_when: output.rc == 2
    - name: Example playbook with failed_when
      debug:
        msg: "Hello World!"
```

### Failing a Playbook with "fail"

```yaml
---
- name: Failing a Playbook with fail
  hosts: localhost
  tasks:
    - name: Failing a Playbook with fail
      fail:
        msg: "This task will always fail."
```

## Vault

### Editing an Encrypted File

```bash
ansible-vault edit file.yml
```

### Updating Encryption Password

```bash
ansible-vault rekey file.yml
```

### Viewing an Encrypted File

```bash
ansible-vault view file.yml
```

### Encrypting a File

```bash
ansible-vault encrypt file.yml
```

### Encrypting a File with a Password File

```bash
ansible-vault encrypt file.yml --vault-password-file ~/.vault_pass.txt
```

### Decrypting a File

```bash
ansible-vault decrypt file.yml
```

### Encrypting a String

```bash
ansible-vault encrypt_string "Hello World!" --name "my_var"
```

### Encrypting a String with a Password File

```bash
ansible-vault encrypt_string "Hello World!" --name "my_var" --vault-password-file ~/.vault_pass.txt
```

## Asynchronous Tasks

### Running a Task Asynchronously

```yaml
---
- name: Running a Task Asynchronously
  hosts: localhost
  tasks:
    - name: Running a Task Asynchronously
      command: /bin/bash -c "for i in `seq 1 5`; do echo $i; sleep 1; done"
      async: 60
      poll: 0
```

### Checking the Status of Asynchronous Tasks

```yaml
---
- name: Rolling Update with Timeout
  hosts: localhost
  tasks:
    - name: Start the application update (async)
      command: /bin/bash -c "for i in `seq 1 5`; do echo $i; sleep 1; done"
      async: 60
      poll: 0 
      register: update_result

    - name: Wait for the update to complete
      async_status:
        jid: "{{ update_result.ansible_job_id }}"
      register: job_result
      until: job_result.finished
      retries: 60  # Check the status every 10 seconds (60 times)

    - name: Check if the update was successful
      debug:
        msg: "Update successful"
      when: job_result.finished                           
```

## Roles

### Creating a Role

```bash
ansible-galaxy init my_role
```

### Using a Role

```yaml
---
- name: Using a Role
  hosts: localhost
  roles:
    - my_role
```

### Using a Role with Variables

```yaml
---
- name: Using a Role with Variables
  hosts: localhost
  roles:
    - role: my_role
      vars:
        my_var: 123
```

### Using a Role with Multiple Variables

```yaml
---
- name: Using a Role with Multiple Variables
  hosts: localhost
  roles:
    - role: my_role
      vars:
        my_var1: 123
        my_var2: 456
```

### Using a Role with Tags

```yaml
---
- name: Using a Role with Tags
  hosts: localhost
  roles:
    - role: my_role
      tags:
        - install
        - configure
```

## Ansible Galaxy

### Searching for Roles

```bash
ansible-galaxy search nginx
```

### Installing a Role

```bash
ansible-galaxy install nginx
```

### Installing a Role with a Specific Version

```bash
ansible-galaxy install elastic.elasticsearch,7.15.0
```

## Ansible Collections

### Installing a Collection

```bash
ansible-galaxy collection install community.general
```

### Installing a Collection with a Specific Version

```bash
ansible-galaxy collection install community.general:8.1.0
```

### Installing a Collection from a File

```bash
ansible-galaxy collection install community.general-8.1.0.tar.gz
```

### Installing a Collection from a Directory

```bash
ansible-galaxy collection install community.general-8.1.0/
```

## Resources About Ansible

### Official Ansible Documentation

- [Ansible Documentation](https://docs.ansible.com/ansible/latest/index.html)

### Ansible Blogs and Articles

- [Ansible Blogs](https://www.ansible.com/blog)
- [Ansible Articles on Red Hat Developer](https://developers.redhat.com/topics/automation/all)

### Ansible Community and Forums

- [Ansible Community](https://www.ansible.com/community)
- [Ansible Mailing List](https://groups.google.com/g/ansible-project)
- [Ansible Subreddit](https://www.reddit.com/r/ansible/)

### Ansible GitHub Repository

- [Ansible Organization on GitHub](https://github.com/ansible)
- [Ansible GitHub Repository](https://github.com/ansible/ansible)

### Ansible Videos

- [Ansible YouTube Channel](https://www.youtube.com/@AnsibleAutomation)

### Ansible Tools

- [ansible/awx](https://github.com/ansible/awx): AWX provides a web-based user interface, REST API, and task engine built on top of Ansible. It is one of the upstream projects for the Red Hat Ansible Automation Platform.
- [ansible-semaphore/semaphore](https://github.com/ansible-semaphore/semaphore): A modern UI for Ansible.
- [ansible/molecule](https://github.com/ansible/molecule): Molecule aids in the development and testing of Ansible content: collections, playbooks, and roles.
- [dev-sec/ansible-collection-hardening](https://github.com/dev-sec/ansible-collection-hardening): This Ansible collection provides battle-tested hardening for Linux, SSH, nginx, MySQL.
- [ansible/ansible-lint](https://github.com/ansible/ansible-lint): ansible-lint checks playbooks for practices and behavior that could potentially be improved and can fix some of the most common ones for you.
- [fboender/ansible-cmdb](https://github.com/fboender/ansible-cmdb): Generate a host overview from ansible fact gathering output.
- [willthames/ansible-inventory-grapher](https://github.com/willthames/ansible-inventory-grapher): ansible-inventory-grapher creates a dot file suitable for use by graphviz.
- [ansible/ansible-lint](https://github.com/ansible/ansible-lint): ansible-lint checks playbooks for practices and behavior that could potentially be improved and can fix some of the most common ones for you.
- [groupon/ansible-silo](https://github.com/groupon/ansible-silo): Ansible in a self-contained environment via Docker.
- [pearofducks/ansible-vim](https://github.com/pearofducks/ansible-vim): A vim plugin for syntax highlighting Ansible's common filetypes.
- [nickjj/ansigenome](https://github.com/nickjj/ansigenome): A tool to help you gather information and manage your Ansible roles.
- [ansible-community/ara](https://github.com/ansible-community/ara): ARA Records Ansible and makes it easier to understand and troubleshoot.
- [mitogen-hq/mitogen](https://github.com/mitogen-hq/mitogen): Distributed self-replicating programs in Python ([Mitogen for Ansible](https://mitogen.networkgenomics.com/ansible_detailed.html) is a completely redesigned UNIX connection layer and module runtime for Ansible.)
- [Phansible](https://github.com/phansible/phansible): Phansible - generate Vagrant + Ansible dev environments for PHP.
- [cidrblock/td4a](https://github.com/cidrblock/td4a): Template designer for automation.
- [adammck/terraform-inventory](https://github.com/adammck/terraform-inventory): Terraform State → Ansible Dynamic Inventory.
- [ansible-community/ansible-bender](https://github.com/ansible-community/ansible-bender): This tool bends containers using Ansible playbooks and turns them into container images.
- [pixiu-io/kubez-ansible](https://github.com/pixiu-io/kubez-ansible): To provide quick deployment tools for Kubernetes clusters and cloud-native applications by Ansible.
- [apenella/go-ansible](https://github.com/apenella/go-ansible): Go-ansible is a Go package that enables the execution of ansible-playbook or ansible commands directly from Golang applications.
- [ansible/ansible-runner](https://github.com/ansible/ansible-runner): A tool and Python library that helps when interfacing with Ansible directly or as part of another system, whether that be through a container image interface, as a standalone tool, or as a Python module that can be imported.

### IDE Extensions

#### VSCode

- [Ansible extension by Red Hat](https://marketplace.visualstudio.com/items?itemName=redhat.ansible) - This extension provides comprehensive Ansible language support, including syntax highlighting, auto-completion, and integrated linting.
- [YAML Support](https://marketplace.visualstudio.com/items?itemName=redhat.vscode-yaml) - This extension offers enhanced YAML language support with features like schema validation, auto-completion, and hover documentation.
- [ansible-vault](https://marketplace.visualstudio.com/items?itemName=dhoeric.ansible-vault) - This extension facilitates the encryption and decryption of Ansible Vault files directly within VSCode, streamlining the process of managing sensitive data.

#### PyCharm

- [Ansible support](https://plugins.jetbrains.com/plugin/14893-ansible) - This plugin provides support for Ansible directly in PyCharm with features such as playbook run configurations, syntax highlighting, and completion for Ansible keywords.

#### Sublime

- [Ansible](https://packagecontrol.io/packages/Ansible) - This package enhances Sublime Text with Ansible syntax highlighting, code snippets, and completions for a better development experience.
- [GitGutter](https://packagecontrol.io/packages/GitGutter) - This package shows information about files in a git repository, including changes and line modifications directly in the editor.
- [SideBarEnhancements](https://packagecontrol.io/packages/SideBarEnhancements) - This package provides enhancements to the operations on the Sidebar of Files and Folders, improving file management in Sublime Text.
- [Sublime Linter](https://packagecontrol.io/packages/SublimeLinter) - This package is a code-linting framework for Sublime Text 3, helping to identify syntax errors and stylistic issues.
- [Pretty YAML](https://packagecontrol.io/packages/Pretty%20YAML) - This package prettifies YAML for Sublime Text 2 and 3, making YAML files easier to read and edit.
- [Yamllint](https://packagecontrol.io/packages/SublimeLinter-contrib-yamllint) - This package is a Sublime wrapper around yamllint, integrating YAML linting into Sublime Text.

#### Vim

- [Ansible-vim](https://github.com/pearofducks/ansible-vim) - This is a Vim plugin for syntax highlighting Ansible's common file types.

### Newsletters

- [Ansible The Bullhorn](https://forum.ansible.com/c/news/bullhorn/17)
- [DevOpsLinks](https://faun.dev/newsletter/devopslinks)
