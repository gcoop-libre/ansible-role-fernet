# [_ANSIBLE-ROLE-FERNET CHANGELOG_](https://github.com/gcoop-libre/ansible-role-fernet)

 - this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html)

## [`Unreleased - 2025-10-02`](https://github.com/gcoop-libre/ansible-role-fernet/-/compare/v0.1.1...develop)


### `CHANGELOG`

- update Unreleased and add v0.1.0

### `README`

- add v0.1.0 in tags summary

## [`v0.1.1 - 2025-10-02`](https://github.com/gcoop-libre/ansible-role-fernet/-/compare/v0.1.0...v0.1.1) _don't build when encrypt/decrypt binaries already exists, allow force build and add symbolic link to the gcoop-libre.fernet role in tests/roles for easier test execution_


### `defaults/main`

- enable fernet_decrypt_dist_remote
- enable fernet_encrypt_dist_remote
- enable fernet_check_dist_remote
- disable fernet_build_remote_force

### `tasks/build`

- move all build tasks and dependencies from main.yml to build.yml

### `tasks/main`

- include bin info tasks when fernet_bin_info is enabled
- incude build tasks when fernet_build_remote_force is enabled or encrypt and decrypt binaries don't exists
- include verify in remote tasks when fernet_check_dist_remote is enabled
- disable fernet_encrypt_dist_remote_exists and fernet_decrypt_dist_remote_exists on start

### `tasks/verify-remote`

- enable fernet_decrypt_dist_remote_exists when decrypt binary exists and is executable
- verify in remote if exists decrypt binary when fernet_decrypt_dist_remote is enabled
- enable fernet_encrypt_dist_remote_exists when encrypt binary exists and is executable
- verify in remote if exists encrypt binary when fernet_encrypt_dist_remote is enabled

### `tests/gcoop-libre`

- add symbolic link to the role gcoop-libre.fernet in tests/roles

### `tests/requirements`

- set version as v0.1.1 for gcoop-libre.fernet

### `VERSION`

- Bump version to v0.1.1

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
