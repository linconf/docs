[LinConf](https://github.com/linconf) is a collection of Ansible roles on GitHub
targeted at Debian/Ubuntu and CentOS/RHEL systems.

Each role is written with ease-of-use and ease-of-interpretation in mind. Released
under the MIT license, roles also make good building blocks for more specialized
roles.


## Design

Roles are written with precidence given to the following (in order):

1. Simplicity
2. Dependency-Free
3. Functionality
4. Idempotance


** Simplicity ** - Roles should be easy to read and easy to follow whenever possible.

** Dependency-Free ** - Wherever practical, different functions are broken into different
roles. If required dependency resolution and configuration isn't managed by a distributions
package manager, it will likely require more than one role.

** Functionality ** - Where possible and without sacraficing simplicity, roles are
written to be as useful as possible (notibly at the occasional expense of idempotance)

** Idempotance ** - A very useful and important feature of Ansible, roles that fail
to maintain idempotance will, where possible, present tags allowing idempotant 
execution (by disabling some actions).


## Testing

Roles are tested locally using Vagrant or Docker as well as on each commit using
Travis-CI. See the Testing page for more detailed information about testing methods.

## Author

Chad Sheets - [GitHub](https://github.com/cjsheets) | [Blog](http://chadsheets.com/) | [Email](mailto:chad@linconf.com)

## License

All LinConf authored roles are released under the [MIT License](https://tldrlegal.com/license/mit-license)
unless otherwise stated. Some roles posted in LinConf are forked from other repositories
in which case their original license is retained. 

[![Analytics](https://cjs-beacon.appspot.com/UA-10006093-3/github/linconf/ansible-users?pixel)](https://github.com/linconf/ansible-users)



