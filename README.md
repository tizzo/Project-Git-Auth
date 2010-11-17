# Project Git Authentication

This module integrates the project and sshkey modules with the daemons availble at https://github.com/tizzo/Drupal.org-Git-Daemons.

When a project module is created a job is created for one of the Daemons which, in turn, creates a repository at a configurable location using the projects shortname followed by '.git'.  It also provides a web service to the SSH Daemon that authenticates a user by their public keys stored in the sshkey module and allows them to access any repository that corresponds to a project for which to acting user is a maintainer over ssh, without having a user account on that system.

## Requirements:
-   [Project Module HEAD from CVS](http://drupal.org/project/project)
-   [SSH Keys Module](http://drupal.org/project/sshkey)
-   [Drupal Git Daemons](https://github.com/tizzo/Drupal.org-Git-Daemons)

## Installation instructions

1.   Install the module
2.   Clone the [Pheanstalk](https://github.com/pda/pheanstalk) into this module's directory: `git clone https://github.com/pda/pheanstalk``
3.   Configure the module (if necessary) at `admin/settings/project-git-auth`
4.   Start the [Drupal Git Daemons](https://github.com/tizzo/Drupal.org-Git-Daemons)
5.   Profit!
