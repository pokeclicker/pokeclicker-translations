# Translator Instructions
This file contains details for people who want to help translate the game.

## Prerequisites
1. You will need a github account for providing edits to the files here, if you do not already have on you can [sign up here](https://github.com/signup)
1. Log into your account and create a fork of this repo [click here](https://github.com/pokeclicker/pokeclicker-translations/fork)

## Making Changes
1. Find the file with the content you want to translate. Translation files are inside the `/locales/{lang}/` folders
2. Click the edit button at the top right of the file
3. Make your changes in the web editor
4. Check what you have changed on the preview tab
5. Below the editor, add a short description of what you have changed, select the "Create a new branch" option, and then click the "Propose Changes" button
6. Confirm that the changes are being compared to repo `pokeclicker/pokeclicker-translations` branch `develop`, and then click "Create Pull Request"
7. Add any additional comments you want, and then click "Create Pull Request"
8. Someone will review your changes and either accept them or request you make some changes

## Updating a pull request with new changes
1. On your repo, switch to the branch you made for your pull request
2. Make any additional changes you want, but this time commit them directly to that branch instead of making a new one
3. After commiting, your Pull Request should automatically pick up your new changes

## Other Notes
Any content which is an empty string ("") will fallback to the english translation string. If you need your language to actually return nothing for this key, you can use the unqouted value `null`
