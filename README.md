# go-lint

## Description

To run GolangCI-Lint tool by docker for static check

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