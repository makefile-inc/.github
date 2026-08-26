# makefile.inc

This organization contains repositories with utils makefile includes repositories for re-usable targets.

## Repositories list

- [common](https://github.com/makefile-inc/common) - contains base targets for another repos,
  like install binaries, create releases artifacts, git operations... 
- [git-crypt](https://github.com/makefile-inc/git-crypt) - targets for using [git-crypt](https://github.com/AGWA/git-crypt).
  
  Dependencies:
  - `common` as git submodule.
- [github-repos](https://github.com/makefile-inc/github-repos) - targets for manage Github repositories via opentofu (terraform).

  Dependencies:
  - `git-crypt` as git submodule (with `common` as submodule) for encrypt state files and secrets.
- [go](https://github.com/makefile-inc/go) - targets for `go lang` operations like lint, test, build.

  Also, includes github actions for test pull requests and create releases in Github.

  Dependencies:
  - `common` as git submodule.
- [openapi](https://github.com/makefile-inc/openapi) - targets for generate client and servers and conversions openapi specs.

  Dependencies:
  - `common` as git submodule.

## Test repositories

Organization also contains test repositories for testing another repositories.
All these repositories names started with `tests-` prefix:
- [tests-git-crypt](https://github.com/makefile-inc/tests-git-crypt) - [git-crypt](https://github.com/makefile-inc/git-crypt) test repo.
- [tests-go](https://github.com/makefile-inc/tests-go) - [go](https://github.com/makefile-inc/go) test repo.
