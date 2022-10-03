# Maintainer Instructions

This file contains instructions for the maintainer of this repo, for updating the published files etc

## Updating Github Pages
No build process currently required, just merge `develop` into `main` and pokeclicker will start getting the latest translations

## Pull Requests
There is a [test.yml](.github/workflows/test.yml) workflow run on PRs just to check the json is valid and no new keys were added/removed without updating all language files


## TODO
Add a CODEOWNERS file to automatically request reviews from certain people if a file was changed for a language they manage

Look into using [translation check](https://github.com/locize/translation-check) for a better view of what needs translating

Add a workflow to auto-label PRs with the languages changed
