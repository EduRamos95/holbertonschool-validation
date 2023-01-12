# Awesome Inc. website Docs

Welcome to our site, please follow the next information in order to have a
working website. test/tag

## Prerequisites

- A Valid Go-Hugo website is provided
- There are no Git Submodules
- The theme ananke is installed
- No directory dist/ committed
- Makefile present
- Use the theme "ananke" for the website by following:
`Note for non-git users` at the
[Step 3](https://docs.edg.io/guides/sites_frameworks/getting_started/hugo).
- The website is expected to be generated into ./dist folder but this folder
should be **absent** from the repo.

## Lifecycle

- post
- build
- clean
- package
- lint
- unit-tests
- integration-tests
- validate
- help

## Workflow

- Continuous Integration with GitHub Actions
- The workflow is executed into Ubuntu 18.04 environment
- Required tools are installed prior to any `make` target,
  by executing the script `setup.sh`
