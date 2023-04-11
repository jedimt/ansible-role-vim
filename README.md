Ansible Role: Vim
=========

Installs Vim with a set of plugins.

Requirements
------------

None.

Role Variables
--------------

The defaults file specifies the list of Vim plugins and their various versions to install.

Addtionally, the following variables are defined in the defaults/main.yml file.

    # Location for vim configuration directory
    vim_dir: "{{ ansible_env.HOME }}/.vim"

    # Location for vim startup file
    vimrc: "{{ ansible_env.HOME }}/.vimrc"

    install_packages:
    - vim
    - git
    - fonts-powerline
    - fzf

Dependencies
------------

None

Example Playbook
----------------

    # ===========================================================================
    # Configure Vim
    # ===========================================================================
    - name: Install Vim plugins
      hosts: servers
      gather_facts: false
      tags: play_vim

      roles:
        - jedimt.vim

License
-------

MIT

Author Information
------------------

Aaron Patten
aaronpatten@gmail.com
