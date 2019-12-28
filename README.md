# go-lint

## Description

To run GolangCI-Lint tool by docker for static check

## Inputs

- `FLOWCI_GIT_REPO` (required): git repo name
- `GOLINT_VERSION`: GolangCI-Lint version, default is `v1.21.0`

## How to use it

```yml
#  Example that togeher with git clone plugin

envs:
  FLOWCI_GIT_URL: "https://github.com/gin-gonic/gin.git"
  FLOWCI_GIT_REPO: "golang-gin"
  FLOWCI_GIT_BRANCH: "master"

steps:
  - name: clone
    plugin: 'gitclone'
    allow_failure: false

  - name: lint
    plugin: go-lint
```