# [_GCOOP-LIBRE.FERNET CHANGELOG_](https://github.com/gcoop-libre/ansible-role-fernet)

 - this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html)

## [`Unreleased - 2025-09-30`](https://github.com/gcoop-libre/ansible-role-fernet/-/compare/v0.1.0...develop)


## [`v0.1.0 - 2025-09-30`](https://github.com/gcoop-libre/ansible-role-fernet/-/compare/6a33d07...v0.1.0) _first public release_


### `ansible`

- add ansile config file

### `defaults/main`

- set all defaults variables

### `general`

- add GPLv3 LICENSE
- add project description as 'Build Fernet (symmetric encryption) pipe commands'

### `.gitignore`

- add *.retry, tests/inventory and tests/roles/* in .gitignore

### `handlers/main`

- set empty handlers

### `Makefile`

- add inventory, inventory_env, lint, playbook, playbook_only, requirements, syntax, tools, vault rules

### `meta/main`

- set galaxy_info (author, company, license, platforms, galaxy_tags, etc)

### `pre-commit`

- sort hooks and update revisions ansible-lint/v25.9.0, pre-commit-hooks/v6.0.0, pre-commit-shell/v1.0.6, pylint/v3.3.8 in pre-commit-config
- add hooks (end-of-file-fixer, trailing-whitespace, shell-lint, ansible-lint, pylint) in pre-commit config

### `README`

- add flag .NO_TAG_LINK to use with git-tag-readme
- add .readme-footer to use ewith git-tag-readme
- add .readme-header to use ewith git-tag-readme
- add README.md generated with git-tag-readme

### `tasks/apt`

- add APT tasks (delte old settings, configure, update and install packages)

### `tasks/bin-info`

- add bin info tasks (execute readelf and ldd, show debug)

### `tasks/main`

- add main tasks (apt, dirs, encryption key, encrypt and decrypt build and test)

### `tasks/pip-package`

- add pip packages install task

### `tasks/pip-venv`

- add initilize virtualenv

### `templates/pd`

- set python decrypt source template code

### `templates/pe`

- set python encrypt source template code

### `tests/requirements`

- add gcoop-libre.fernet/v0.1.0 in requirements

### `tests/test`

- add test Playbook for Fernet (symmetric encryption)

### `vars/main`

- set empty vars

### `VERSION`

- Bump version to v0.1.0
- set version as v0.0.0
