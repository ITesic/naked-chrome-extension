# Naked Chrome extension

Simple and clean Chrome Extension skeleton. It is base point for building new Chrome Extension.
There is no JS framework integrated, no test suite, so you can easily setup your favorite tools and start building.

Manifest file contains basic settings and best practices.
Modular file structure enables building different part of extension separately.
Automated build system for development and production is configured and ready for use.

# Getting started

NCE uses few tools to speed up development process. Styles are written in SASS. 
Build system is written in Gulp, which automatically converts SASS to CSS during development.

## Installation

1. Clone this repository in you project directory
2. Type command `npm install` or `yarn install` to install all dependencies
3. Type command `gulp` to start build process and watching for changes

To install extension open Extensions panel in Chrome (More Tools > Extensions) and check 'Developer Mode' option.
Click 'Load unpacked extension' button and navigate to `<your project path>/src/`. It will install development version of NCE to your browser.

Details about Chrome extension development can be found in the [official documentation](https://developer.chrome.com/extensions).

## File structure

NCE uses modular file structure which enables development and building separate parts of extension.

```javascript
|_ _locales             // Localization files
|_ icons                // Icons of the extension, visible in browser and in Chrome Web Store
|_ assets               // Common assets which will be used in different parts of extension
|_ src                  // Source files. Every section can have it's inner structure with assets and styles
  |_ popup              // Popup section of extension. All files related to popup should go here.
    |_ assets           // Assets related only with popup
    |_ styles           // Styles used only in popup
  |_ background         // Code for background section
  |_ content            // Injectable code
  |_ options            // Scripts for options section which is visible in settings
|_ manifest.json        // Chrome Extension manifest file. Contains config of extension and paths to all scripts
|_ gulpfile.js          // Gulp configuration file
|_ package.json

```

## Deployment

Extensions are distributed through [Chrome Web Store](https://chrome.google.com/webstore/category/extensions).
You need developer account to upload extension to Chrome Web Store. 

To package extension and prepare it for distribution run command `grunt build` and after it finishes run `grunt package`.
Built extension will be in folder `<your project path>/dist/`.
Packed extension will be in folder `<your project path>/package/`.

# Contributing

This is my hobby project, but it would great to see it in the wild, used by other people.
I will gladly accept any ideas and contribution.
I use SemVer for versioning. For the versions available, see the tags on this repository.

# Licence

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

# Credits

Icons used for NCE are made by [Smashicons](https://www.flaticon.com/authors/smashicons) from [www.flaticon.com](https://www.flaticon.com/)
