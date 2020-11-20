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
``` bash
npm start
```

### Use CLI for building Android apps
``` bash
npm start build:android
npm start build:android:production
```


### Use CLI for building iOS apps
Create the `ios/App/export-store-options.plist` and `ios/App/export-debug-options.plist` files.

#### Example debug plist:
``` xml
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
<plist version="1.0">
  <dict>
    <key>compileBitcode</key>
    <false/>
    <key>method</key>
    <string>development</string>
    <key>teamID</key>
    <string>XXXXXXXXXX</string>
    <key>provisioningProfiles</key>
    <dict>
      <key>io.ionic.starter</key>
      <string>XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX</string>
    </dict>
    <key>signingStyle</key>
    <string>manual</string>
    <key>signingCertificate</key>
    <string>iPhone Developer</string>
  </dict>
</plist>
```

#### Example store plist:
``` xml
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
<plist version="1.0">
  <dict>
    <key>compileBitcode</key>
    <false/>
    <key>method</key>
    <string>app-store</string>
    <key>teamID</key>
    <string>XXXXXXXXXX</string>
    <key>provisioningProfiles</key>
    <dict>
      <key>io.ionic.starter</key>
      <string>XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX</string>
    </dict>
    <key>signingStyle</key>
    <string>manual</string>
    <key>signingCertificate</key>
    <string>iPhone Distribution</string>
  </dict>
</plist>
```





``` bash
npm start build:ios
npm start build:ios:production
```


