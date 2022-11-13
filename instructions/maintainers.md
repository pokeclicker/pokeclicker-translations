# Maintainer Instructions

This file contains instructions for the maintainer of this repo, for updating the published files etc

## Updating Github Pages
No build process currently required, just trigger the [release workflow](https://github.com/pokeclicker/pokeclicker-translations/actions/workflows/release.yml)

## Adding a New Language
Add the language code into the [i18n-locales-sync config](/config/localesSync.config.js) `secondaryLanguages` array, then run
```cmd
npm run i18n-sync
```
A folder will be created for the language, and a copy of the english language files will be created with empty strings on all keys

## Pull Requests
There is a [test.yml](.github/workflows/test.yml) workflow run on PRs just to check the json is valid and no new keys were added/removed without updating all language files


## TODO
Add a CODEOWNERS file to automatically request reviews from certain people if a file was changed for a language they manage

Look into using [translation check](https://github.com/locize/translation-check) for a better view of what needs translating

Add a workflow to auto-label PRs with the languages changed
