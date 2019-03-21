# eslint-config-hbg

ESlint configuration for Helsingborg Stad JS projects. This package was inspired by [wesbos/eslint-config-wesbos](https://github.com/wesbos/eslint-config-wesbos).

## Installation

1. npm install -D eslint-config-hbg
2. Create a .eslintrc.js file in the project root and extend the configuration:

```
module.exports = {
    extends: ["hbg"]
};
```

## Setup with VSCODE

You should read this entire thing. Serious!

Once you have done one, or both, of the above installs. You probably want your editor to lint and fix for you. Here are the instructions for VS Code:

1. Install the [ESLint package](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)
2. Now we need to setup some VS Code settings via `Code/File` → `Preferences` → `Settings`. It's easier to enter these settings while editing the `settings.json` file, so click the `{}` icon in the top right corner:

```js
  // These are all my auto-save configs
"editor.formatOnSave": true,
// turn it off for JS and JSX, we will do this via eslint
"[javascript]": {
  "editor.formatOnSave": false
},
"[javascriptreact]": {
  "editor.formatOnSave": false
},
// tell the ESLint plugin to run on save
"eslint.autoFixOnSave": true,
// Optional BUT IMPORTANT: If you have the prettier extension enabled for other languages like CSS and HTML, turn it off for JS since we are doing it through Eslint already
"prettier.disableLanguages": ["javascript", "javascriptreact"],
```
