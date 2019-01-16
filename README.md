# Webpack4 Front-end Boilerplate for single-page application

<a target="_blank" href="https://opensource.org/licenses/MIT" title="License: MIT">
  <img src="https://img.shields.io/badge/License-MIT-blue.svg">
</a>
<a href="#badge">
  <img alt="code style: prettier" src="https://img.shields.io/badge/code_style-prettier-ff69b4.svg">
</a>
<a target="_blank" href="http://makeapullrequest.com" title="PRs Welcome"><img src="https://img.shields.io/badge/PRs-welcome-brightgreen.svg"></a>

## Prepare

### Required

1. Install or update [Node.js](https://nodejs.org/en/);

### Optional

2. Install editorconfig plugin for your editor ([PhpStorm](https://plugins.jetbrains.com/plugin/7294-editorconfig), [Sublime Text](https://packagecontrol.io/packages/EditorConfig), [Atom](https://atom.io/packages/linter-eslint), [VS Code](https://marketplace.visualstudio.com/items?itemName=EditorConfig.EditorConfig)) - consistent coding style between different editors and IDEs. You can find configuration in .editorconfig file.
3. Install eslint plugin for your editor ([PhpStorm](https://www.jetbrains.com/help/phpstorm/eslint.html), [Sublime Text](https://packagecontrol.io/packages/ESLint), [Atom](https://atom.io/packages/editorconfig), [VS Code](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)) - the pluggable linting utility for JavaScript. You can find configuration in .eslintrc file.

## Start

1. Clone or [download](https://github.com/VitFL/webpack4-frontend-spa-boilerplate/archive/master.zip) project:
   ```
   git clone https://github.com/VitFL/webpack4-frontend-spa-boilerplate.git your-project-name
   ```
1. Enter in project folder and remove .git folder:
   ```
   cd your-project-name && rm -rf .git
   ```
1. Install dependencies with npm:
   ```
   npm install
   ```
1. Use build commands:

| Command            | Description                                                                                                                                                        |
| ------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `npm run build`    | Build project for production (compiles/minifies/copies assets to /dist ready for production);                                                                      |
| `npm run dev`      | Run your project on a local dev server with auto compile and browser reload each time you press save on a file (webpack-dev-server + browser-sync-webpack-plugin); |
| `npm run lint`     | Lint js code in scr folder using Eslint, you can edit rules in .eslintrc config file;                                                                              |
| `npm run lint:fix` | Lint js code in src folder using Eslint and automatically fix errors.                                                                                              |
| `npm run deploy`   | Deploys site to Github Pages.                                                                                                                                      |

### Include plugins/libraries

#### CSS

Install dependency (for example, [animate.css](https://daneden.github.io/animate.css/)):

```
npm i animate.css
```

Import dependency in src/scss/\_libs.scss once:

```
@import '~animate.css';
```

- Prefix your imports with `~` to grab from node_modules/
- for more information, see https://github.com/webpack-contrib/sass-loader#imports

#### JS

##### JavaScript plugins

Install dependency (for example, [tippy.js](https://github.com/atomiks/tippyjs)):

```
npm i tippy.js
```

Import dependency in src/js/main.js once:

```js
import 'tippy.js';
```

### Alias @ in styles and js

@ in path points to src folder, with it you can create an absolute path.
CSS:

```
  background: #000 url(~@/img/webpack.png) no-repeat;
```

JS:

```
import module from '@/js/module';
```

## Features

- [Webpack 4](https://webpack.js.org/)
- [FontAwesome 5](https://www.npmjs.com/package/@fortawesome/fontawesome-free)
- [jQuery](https://jquery.com/) \*
- [BrowserSync](https://www.npmjs.com/package/browser-sync-webpack-plugin)
- ES6+ Support via [babel-loader](https://github.com/babel/babel-loader)
- SASS Support via [sass-loader](https://github.com/webpack-contrib/sass-loader)
- JS linting and formatting via [ESLint](https://eslint.org/) and [Prettier](https://github.com/prettier/prettier)
- Css [Autoprefixer](https://github.com/postcss/autoprefixer)
- Image optimization using [image-webpack-loader](https://www.npmjs.com/package/image-webpack-loader)
- Deployment to Github Pages with [gh-pages](https://www.npmjs.com/package/gh-pages)

\* Webpack will add jQuery code to final bundled js file only if it is used somewhere in your code or if it is needed by some of imported plugins.
