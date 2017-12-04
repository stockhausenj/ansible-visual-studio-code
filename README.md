# Ansible Role: ansible-visual-studio-code

Installs Visual Studio Code on Windows.

## Requirements

Requires the following to be executed in Powershell on the target machine(s):
```
> Set-ExecutionPolicy RemoteSigned
```
Download and execute this Powershell script: [ConfigureRemotingForAnsible.ps1](https://github.com/ansible/ansible/blob/devel/examples/scripts/ConfigureRemotingForAnsible.ps1)

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):
```
```

## Dependencies

None.

## Example Playbook
```
$ ansible-galaxy install stockhausenj.visual-studio-code
$ ansible-playbook -i inventory.yaml setup-vs-code.yaml -u admin --ask-pass
```
```
- hosts: all
  vars:
    ansible_port: 5986
    ansible_connection: winrm
    ansible_winrm_server_cert_validation: ignore
  tasks:
  roles:
    - include_role:
        name: stockhausenj.ansible-visual-studio-code
```
## License

MIT
