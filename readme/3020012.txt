# puppet-git

## Overview

Install, enable and configure a GIT server.

* `git::daemon` : Class to create an xinetd-base GIT server.
* `git::gitolite` : Class to set up gitolite GIT server management.
* `git::gitosis` : Class to set up gitosis GIT server management.
* `git::gitweb` : Class to set up gitweb repository access.
* `git::user` : Class to create a dedicated system `git` user.

## Examples

Set up an xinetd-based GIT server for the git:// protocol :

    include git::user
    class { 'git::daemon':
      user => 'git',
    }

Set up an ssh-based GIT server to be managed using gitolite :

    include git::user
    class git::gitolite {
      admin_sshkey     => 'AAAAHsKhmP44J0....j2H6pC8dU=',
      admin_sshkeytype => 'rsa',
    }

