<img src="banner.png" alt="drawing" width="700"/>

[marketplace.visualstudio/ark-ng-extensions-pack](https://marketplace.visualstudio.com/items?itemName=AlvaroAlmendros.ark-ng-extensions-pack)

> All common extension between the different packs has been moved to [Ark's Common Extensions Pack](https://github.com/arkdelkaos/ark-common-extensions-pack)

# Ark's Angular Extensions Pack

- [Ark's Angular Extensions Pack](#arks-angular-extensions-pack)
  - [FAQ](#faq)
    - [Why do I need all those extensions](#why-do-i-need-all-those-extensions)
    - [What about the extensions I've already installed](#what-about-the-extensions-ive-already-installed)
  - [Included Extensions](#included-extensions)
    - [Core](#core)
    - [Linting and Syntax highlighting](#linting-and-syntax-highlighting)
    - [Tricks](#tricks)
    - [UI](#ui)
  - [Configuration](#configuration)
  - [How to contribute](#how-to-contribute)

This is a pack with the extensions I use and recommend to my coworkers, so we can activate/deactivate between workspaces easier.
For example, when working with angular and react projects the process of whitelisting workspace only extensions is kind of tedious.

## FAQ

### Why do I need all those extensions

Maybe. You can just disable any extension you don't want to use.
But I recommend you to try them.

- The ones with the icon 🔥 are my favorites!
- Those with the icon 🔒 are a must!

Having less extensions running at the same time will always return a better performance.
But remember that not all extensions are running in the background!: those "on demand" (command palette) extensions weight almost nothing performance wise.

- The extensions with the icon ⚙️ can be kind of heavy on performance

I'll try to explain why I use every extension and how to configure it, **but feel free to add a new PR with any change proposal**.

### What about the extensions I've already installed

Those that aren't included will not be affected.
The ones that are included but were already installed will work as the were, but will be managed with the pack:

- If you enable the pack for a workspace all its extensions (actual and future ones) will be enabled for that workspace
- The same if you disable the pack.
- If you set a unique status for a extension included in the pack, for example you disable the pack as a whole but enable a pair of extensions, the individual settings will prevail over the pack ones.

## Included Extensions

### Core

- 🔒 **Angular Language Service**: El todo en uno imprescible para Angular.
- 🔒 **TSLint**: Deprecated in favor of ESLint, but still in use at our ng9.

### Linting and Syntax highlighting

- 🔒 🔥 **Angular HTML Highlighter**: Will highlight all those angular-esque decorators we use!
- 🔒 **Prettier**: As we don't enable prettier from eslint _(tslint is deprecated, but...)_, we must install it individually.
- 🔒 **SCSS IntelliSense**: The official SCSS intellisense for VSCode.
- 🔒 **Stylelint**: The stylelint client for VSCode.
- 🔥 **LintLens**: When editing `.eslintrc` rules, will tell what every rule do and if it's configured correctly.
- **Headwind**: CSS Class sorter.
- **SCSS Everywhere**: BEM helper that will recommend the current BEM prefix when needed.

### Tricks

- **Sort Package.json**: Automatically sort package.json
- **Typescript Explicit Types**: Automatically generates explicit types
- ⚙️ **Javascript Booster**: refactoring tools like convert from/to function to arrow function, and a lot more

### UI

- 🔒 🔥 **Angular Switcher**: Review the keybindings, as they let you quick change between styles, code, and templates.
- 🔥 **Angular Follow Selector**: `cmd+click` para abrir el codigo del componente al que señala el selector que elijas en las templates.

## Configuration

First of all you should install a good all-in-one font, and use it.

I'll recommend you the two I use, from the [NerdFonts](https://github.com/ryanoasis/nerd-fonts) project: JetBrainsMono Nerd Font & DroidSansMono Nerd Font.

This fonts supports font ligatures and have been patched with all kind of icons to be used with advanced ZSH themes like [powerlevel10k](https://github.com/romkatv/powerlevel10k) _(this princess will be talk about in another castle)_

- Do you have brew? If not, lets start by installing it!

  ```bash
  /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
  ```

- Then...

  ```bash
  brew tap homebrew/cask-fonts
  brew cask install font-jetbrainsmono-nerd-font
  brew cask install font-droidsansmono-nerd-font-mono
  ```

Now that we have brew installed for sure, let me talk you about how to install node correctly, just to be sure.

I hate the official installer and its documentation, and tend to avoid it at all costs. What I do like is [n](https://github.com/tj/n), a Node.js version manager, installed with brew. It will install the node versions you want to use at `/usr/local`, avoiding all kind of shenanigans.

- If you have alread installed node...in your place I probably uninstall it. **If you don't want to just skip this step**.
- Install n and the lts version of node

  ```bash
  brew install n
  n lts
  ```

> _Can anybody find me somebody to love?..._
> **I use brew to install _almost_ everything**. Brew is love! 😍

Now, lets create a custom workspace settings file!
Let's do it the easy way:

- Open VSCode at your react project :)
- Open the command palette: cmd+shift+p
- Type `workspace json`, and you will be able to open the current workspace

Now open the [settings.json](/settings.json) included, and copy it at your workspace settings!
As you can see I have added comments explaining what does every setting :)

When you have this options fulfilled, we can configure how to quick change between workspaces.

- First lest go to the extensions list and disable this addon
- Then enable it **only for the workspace**

Now go to the projects manager and select another project!
In that project you will see that the react extensions included in this pack are disabled!
If you open the react project again you will se that the react extensions and settings are automatically switched on again! _isn't that cool?_ 😉

> Do you want to be able to easily know what workspace are you editing? Take a look at the peacock extension, or just try at de command palette `Peacock: Change to a favorite color` 🌈

## How to contribute

Do you have a extension you really like?

Just wants to provide some configuration or having any doubt?

**Add a issue**! 😉 👍🏻
