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

For testing the translations in pokeclicker, you can set the `TRANSLATIONS_URL` variable in your pokeclicker config.js file to `https://raw.githubusercontent.com/pokeclicker/pokeclicker-translations/develop` if they have been merged here, or the equivalent for your own repo and branch otherwise.

## Hashed translation keys

For some translatable features, such as Pokemon names, translations are unlikely to change. For other features, such as questlines, the English text could change at any time. We use hashed translation keys for such content: the key changes whenever the original text does. This invalidates outdated translations rather than risk them growing inaccurate.

Pokeclicker's translation code handles the difficult parts of this process. All you need to do to is use `App.translation.getHashed()` instead of `App.translation.get()`.

If you are translating a new section of the game that warrants hashed keys, also create a helper function in pokeclicker's `TranslationHelper` class to export all of the keys and English text. This makes it much easier to keep the translation file updated as the game changes.

### Current hashed translations

For all export helper functions, open the browser console in a development build of the game and execute the function there.

- `questlines.json`: call `TranslationHelper.exportQuestlineTranslationDefaults()`