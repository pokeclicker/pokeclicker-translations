# Translator Instructions
This file contains details for people who want to help translate the game.

## Prerequisites
1. You will need a github account for editing the files here, if you do not already have one you can [sign up here](https://github.com/signup)
1. Log into your account and create a fork of this repo [click here](https://github.com/pokeclicker/pokeclicker-translations/fork)

## Creating a new branch for changes
First, make sure you are on your develop branch (use branch selector in top left), and it is up date by using the "sync fork" button

![Sync Fork](https://user-images.githubusercontent.com/4183969/194877677-f2e1a83b-558e-4f5a-873b-3a9d32576ad7.png)

Click the Update Fork button, and if it asks about conflicting changes, you should discard your conflicting changes

Next click the branch selector and type in a name for your new branch. An option will appear to create a branch with this name and switch you onto it

<img src=https://user-images.githubusercontent.com/4183969/194878383-f223a997-48a3-42e9-89c2-87ef2cb795be.png height="300px" alt="Create new branch"/>


## Making Changes
1. [Create a new branch](#creating-a-new-branch-for-changes)
3. Find the file with the content you want to translate. Translation files are inside the `/locales/{lang}/` folders
4. Click the edit button at the top right of the file
5. Make your changes in the web editor
6. Check what you have changed on the preview tab
7. Below the editor, add a short description of what you have changed, make sure the option "Commit directly to the `your-branch-name` branch" option is selected, and click "Commit changes"
8. Confirm that the changes are being compared to repo `pokeclicker/pokeclicker-translations` branch `develop`, and then click "Create Pull Request"
9. Add any additional comments you want, and then click "Create Pull Request"
10. Someone will review your changes and either accept them or request you make some changes

## Updating a pull request with new changes
1. On your repo, switch to the branch you made for your pull request
2. Make any additional changes you want, but this time commit them directly to that branch instead of making a new one
3. After commiting, your Pull Request should automatically pick up your new changes

## Other Notes
Any content which is an empty string ("") will fallback to the english translation string. If you need your language to actually return nothing for this key, you can use the unqouted value `null`

You can reference another translation key within your content like this `[[other_key]]`
There are other features of the translation system you can read about [here](https://www.i18next.com/translation-function/interpolation)

This referencing of other keys is used extensively in the pokemon.json file, many languages will be able to get translations for all of some variant types (eg, Megas) by only translating the `alt.mega` key. 
This is achieved by having the english translation for mega pokemon set up like this:
```json
{
  "alt": {
    "mega": "Mega"
  },
  "Venusaur": "Venusaur",
  "Mega Venusaur": "[[alt.mega]] [[Venusaur]]",
  "Blastoise": "Blastoise",
  "Mega Blastoise": "[[alt.mega]] [[Blastoise]]"
}
```
Note that these are also referencing the translation for the base pokemon name as well as the mega key, so the french file can simply be this:
```json
{
  "alt": {
    "mega": "Méga",
  },
  "Venusaur": "Florizarre",
  "Mega Venusaur": "",
  "Blastoise": "Tortank",
  "Mega Blastoise": ""
}
```
and the Mega Venusaur and Mega Blastoise keys are still properly translated as "Méga Florizarre" and "Méga Tortank"


If you think a translation key is missing (eg, a new pokemon has been added to the game but you can't find it in pokemon.json), please [create an issue](https://github.com/pokeclicker/pokeclicker-translations/issues/new/choose) listing anything missing and someone will make sure it gets added to all language files.
