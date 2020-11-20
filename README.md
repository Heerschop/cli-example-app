# Example App for using ionic and capacitor from the CLI

Leverages the [ionic hooks](https://ionicframework.com/docs/cli/configuration#hooks) and [script-launcher](https://www.npmjs.com/package/script-launcher) for enabling building apps form the cli. 

### Tools

- [ionic-cli](https://beta.ionicframework.com/docs/installation/cli) - The Ionic command line interface (CLI) is your go-to tool for developing Ionic apps.
- [capacitor](https://capacitorjs.com/) - A cross-platform native runtime for web apps.
- [script-launcher](https://www.npmjs.com/package/script-launcher) - Enhance your package.json scripts with features like: menus, functions, arrays, concurrency and many more.

### Basic setup
``` bash
git clone git@github.com:Heerschop/cli-example-app.git
cd cli-example-app
npm install
npx ionic build
```

### Use the [launcher menu](https://www.npmjs.com/package/script-launcher#interactive-menu) for building 
``` bash
npm start
```

### Use CLI for building
``` bash
npm start 
```


