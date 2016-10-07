
`linconf.users` allows you to configure users and groups in an organized manner.
For simple or one-off cases see the [Ansible user module](http://docs.ansible.com/ansible/user_module.html).


## Installation

Run the following command to install from Ansible Galaxy.

```
ansible-galaxy install linconf.users
```


## Dependencies

- None

The latest stable release of Ansible is assumed, however most LinConf roles will run
on earlier versions as well.


## Example Use

**Add a User**

```
- hosts: localhost
  roles:
      - linconf.users
  vars:
    users_accounts:
        - name: 'NewUser'
        group: 'NewUser'
        # Additional Groups
        groups: ['wheel', 'users']
        password: '$6$c6pQJ3kzW80oZwTi$...'
        update_password: 'always'
```

Password hash created using: `mkpasswd --method=SHA-512`

**Remove a User**

```
users_accounts:
    - name: 'NewUser'
    state: absent
```

**Add a Group**

```
users_groups:
    - name: 'NewGroup'
```

Whenever you add a user to a group that doesn't yet exist on the system (using
the `groups:` option of `users_accounts`) you must also use `users_groups` to
add the group to the system.


## Role Variables

All variables are optional.

- `users_system_uid: False` - All users without specified uids will recieve uids less than 1000 per convention.
- `users_accounts: []` - Expects a list of users to add, only **name:** is required.
    - `option:` - see [Ansible user module](http://docs.ansible.com/ansible/user_module.html) for options
- `users_groups: []` - Expects a list of groups to add
    - `option:` - see [Ansible group module](http://docs.ansible.com/ansible/group_module.html) for options

**Additional Options**

This role has 3 lists for users, and 3 lists for groups. This can be useful in 
situations where groups of hosts share the same users.

- `users_accounts: []`
- `users_host_accounts: []`
- `users_group_accounts: []`
- `users_groups: []`
- `users_host_groups: []`
- `users_group_groups: []`

## Role Tags

Including the `--tags` or `--skip-tags` parameters allows the execution
of only parts of certain roles.

**Available Tags:**

- `users` - Primary role tag, executes all role tasks

## Additional


** Testing **

The master branch is continuously validated by Travis-CI.

Minor versions indicate the role passed local testing as described by the
`.kitchen` declaration. Instructions for performing test-kitchen runs locally
are detailed in the [LinConf Documentation](http://linconf.com/about/methodology/).

** Author and License **

Chad Sheets - [GitHub](https://github.com/cjsheets) | [Blog](http://chadsheets.com/) | [Email](mailto:chad@linconf.com)

Released under the [MIT License](https://tldrlegal.com/license/mit-license)