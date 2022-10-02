# Developer Instructions
This file contains instructions for developers adding new translatable content into the game

After adding or removing any new keys, you will need to run a command, so the first step is to clone the repo locally and make sure Node is installed.

If your content is in a feature or area of the game we haven't started translating yet, create a new file for it at `locales/en/{feature}.json`

Add the keys and english text for the content you are translating. There some things you can do besides a flat file with hardcoded strings, see [i18next documentation](https://www.i18next.com/translation-function/interpolation) for more details.

After adding your english text, run these commands to update the other language files with empty strings (empty strings will fallback to english)
```cmd
npm ci
npm run i18n-sync
```
