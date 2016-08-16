sib-clone-git-repo
==================

This role clones a remote git repo.

It also creates facts, primarily for use in other roles that follow:

* git_path
* git_url
* git_commit
* git_last_tag
* git_commit_list

It's easy for anyone to modify the role as needed since it's MIT licensed.

Requirements
------------

Tested to run on Linux, FreeBSD, and OS X. Windows is not supported.

Role Variables
--------------

Pass in these values in the playbook:

* git_dest (path to local git clone)
* project_git_url

Dependencies
------------

* git_branch - from role aikchar.sib-synthesize-vars (when run before) or vars/main.yml

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: aikchar.sib-clone-git-repo,
             project_git_url: "git@example.com/project.git",
             git_dest: "/path/to/git/repo/clone" }

License
-------

MIT

Author Information
------------------

Hamza Sheikh
