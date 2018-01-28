# Git Hooked

This repository is meant to be a companion to a blog post (that is yet to be published).

There is a branch for each option presented in the post for managing Git hooks:

* Using [Husky](https://github.com/typicode/husky/tree/master)
* Using a local `.hooks` directory and symlinks
* Using a local `.hooks` directory and Git configurations

## Branch: husky
Hooks are automatically created and use commands from the `scripts` section of `package.json`.

## Branch: githook-dir-symlinked:
Hooks are managed by having a tracked `.hooks` directory then symlinks them to the `.git/hooks`
directory. Symlinks are created when `npm install` is run, or by invoking `bin/install-hooks.sh`.

## Branch: githook-dir-config:
Hooks are managed by having a tracked `.hooks` directory then you must update your configuration to
point to the `.hooks` directory using:
`git config core.hooksPath .hooks`
