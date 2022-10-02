# Maintainer Instructions

This file contains instructions for the maintainer of this repo, for updating the published files etc

## Updating Github Pages
No build process currently required, just merge `develop` into `main` and pokeclicker will start getting the latest translations

## Pull Requests
There is a [test.yml](.github/workflows/test.yml) workflow run on PRs just to check the json is valid and no new keys were added/removed without updating all language files

Possibly want to add a CODEOWNERS file to automatically request reviews from certain people if a file was changed for a language they manage
