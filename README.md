# Ansible Role: NFS Client

This role sets up a Linux server to be a NFS client.

[![Ansible Role: NFS Client](https://img.shields.io/ansible/role/52314?style=flat-square)](https://galaxy.ansible.com/thorian93/ansible_role_nfs_client)
[![Ansible Role: NFS Client](https://img.shields.io/ansible/quality/52314?style=flat-square)](https://galaxy.ansible.com/thorian93/ansible_role_nfs_client)
[![Ansible Role: NFS Client](https://img.shields.io/ansible/role/d/52314?style=flat-square)](https://galaxy.ansible.com/thorian93/ansible_role_nfs_client)

## Requirements

No special requirements; note that this role requires root access, so either run it in a playbook with a global `become: yes`, or invoke the role in your playbook like:

    - hosts: foobar
      roles:
        - role: ansible-role-nfs-client
          become: yes

## Role Variables

None.

## Dependencies

None.

## OS Compatibility

This role ensures that it is not used against unsupported or untested operating systems by checking, if the right distribution name and major version number are present in a dedicated variable named like `<role-name>_stable_os`. You can find the variable in the role's default variable file at `defaults/main.yml`:

    role_stable_os:
      - Debian 10
      - Ubuntu 18
      - CentOS 7
      - Fedora 30

If the combination of distribution and major version number do not match the target system, the role will fail. To allow the role to work add the distribution name and major version name to that variable and you are good to go. But please test the new combination first!

Kudos to [HarryHarcourt](https://github.com/HarryHarcourt) for this idea!

## Example Playbook

    ---
    - name: "Run role."
      hosts: all
      become: yes
      roles:
        - ansible-role-nfs-client

## Contributing

Please feel free to open issues if you find any bugs, problems or if you see room for improvement. Also feel free to contact me anytime if you want to ask or discuss something.

## Disclaimer

This role is provided AS IS and I can and will not guarantee that the role works as intended, nor can I be accountable for any damage or misconfiguration done by this role. Study the role thoroughly before using it.

## License

MIT

## Author Information

This role was created in 2018 by [Thorian93](http://thorian93.de/).
