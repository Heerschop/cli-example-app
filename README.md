# App for using ionic and capacitor from the CLI

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
When using serve (--livereload) for Android make sure WIFI is enabled on the phone and for iOS make sure the iOS device can access the IP address of the Mac being used.
``` bash
npm start
```

### Use CLI for building or running Android apps
``` bash
# Build Android debug apk
npx ionic capacitor build android --no-open

# Run Android debug apk
npx ionic capacitor run android --no-open

# Run Android debug IPA with livereload
adb reverse tcp:8100 tcp:8100
npx ionic capacitor run android --no-open --livereload --port=8100
```

### Use CLI for building iOS apps
Update the `export-store-options.plist` and `export-debug-options.plist` files. For livereload to work, make sure the iOS device can access the IP address of the Mac being used.
``` bash
# Create to ios project files
npx ionic capacitor update ios

# Open xcode to configure **Signing & Capabilities**
npx ionic capacitor open ios

# Build iOS debug IPA
npx ionic capacitor build ios --no-open

# Run iOS debug IPA
npx ionic capacitor run ios --no-open

# Run iOS debug IPA with livereload
npx ionic capacitor run ios --no-open --livereload --external --port=8100
```
