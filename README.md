# Webarchitects Vim Ansible Role

[![pipeline status](https://git.coop/webarch/vim/badges/main/pipeline.svg)](https://git.coop/webarch/vim/-/commits/main)

This is an Ansible role for installing [Vim](https://www.vim.org/) on Debian or Ubuntu, it can be used with the [localhost playbook](https://git.coop/webarch/localhost).

There are six [default variables](defaults/main.yml):

| Variable name        | Default value        | Comment                                                                  |
|----------------------|----------------------|--------------------------------------------------------------------------|
| `vim`                | `true`               | When True the tasks in this role are run                                 |
| `vim_path`           | `/usr/bin/vim.basic` | The path to `vim`                                                        |
| `vim_alternatives`   | `true`               | When True the `editor` is set to `vim_path` using `update-alternatives`  |
| `vim_user`           | `root`               | The user account to configure                                            |
| `vim_group`          | `{{ vim_user }}`     | The group ownership for files and directories created for `vim_user`     |
| `vim_selected`       | `true`               | When True the ~/.selected-editor is set to `vim_path` for `vim_user`     |

The primary URL of this repo is [`https://git.coop/webarch/vim`](https://git.coop/webarch/vim) and this is where the [release notes](https://git.coop/webarch/vim/-/releases) are, it is also [mirrored to GitHub](https://github.com/webarch-coop/ansible-role-vim) and [available via Ansible Galaxy](https://galaxy.ansible.com/chriscroome/vim).

The [localhost](https://git.coop/webarch/localhost) repo can be used to run this role on the `localhost`.
