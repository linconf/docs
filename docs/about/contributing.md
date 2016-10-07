<h1>Contributing</h1>

All contributions to LinConf are welcome including bug reports, fixes, extensions,
documentation or ideas. GitHub is the best place to contribute in each individual
project.

If you are unfamiliar with GitHub there is an excellent guide on contributing
[here](https://guides.github.com/activities/contributing-to-open-source/#contributing).

If you add code or provide a fix, please keep the following in mind.

## Write Tests

Every role in LinConf includes integration tests which are run through vagrant
VMs or docker containers.

If you add a new feature, please also write a test to confirm the configuration 
is being correctly applied.

## Document

One goal of the LinConf project is maintaining simplicity and reusability of roles.
To achieve these ends, well documented and readable code is necessary.

- Please avoid using non-sensible names for variables
- Add messages that communicate failures or misconfiguration to users
- Feel free to add to the documentation at in the linconf/docs repository

