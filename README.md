# Android Edge Agent

This is a template for any project that want to use OpenDSU inside an Android application.

This project is a heavily modified version of Android's native-gradle-node-folder project
from [nodejs-mobile-samples/](https://github.com/janeasystems/nodejs-mobile-samples/).

It uses Node 12.19 as Node platform.

## How to make it run

This will basically install Node inside the Android application and
make it run on port 3000 for the application to connect to.

### Step 1 - Install Android Studio 4.1

Download version 4.1 from [Download Android Studio](https://developer.android.com/studio) page

### Step 2 - Install proper dependencies

#### Install NDK
    SDK Manager > SDK Tools > Show Package Details > NDK (Side by side) > 21.3.6528147

### Step 3 - Create/open project


### Step 4 - Add the Nodejs project

#### a. Copy project's files

Copy project inside app/src/main/assets/**nodejs-project**/ folder


#### b. Bring in all project dependencies
```sh
cd  app/src/main/assets/nodejs-project/

npm install
```

### Step 5 - Create proper Android emulator

Note: Android 28

### Step 6 - Run the project

Note: Set proper permissions for application: #App Info > Permissions > (3 dots) > All permissions

## Build it from console


### Make sure you can run gradle

__Windows__
Run gradle.bat in Command Prompt

__Linux__
Run gradlew in console.

Tip: If gradlew is not running make it executable with

```sh
chmod +x gradlew
```

### See gradle available task
```sh
grade(w) tasks
```

### Build a debug APK
```sh
gradlew assembleDebug
```

This will create an .apk inside `app/build/output/apk/debug` folder.

If beside building you want to run it
```shell
gradlew installDebug
```
This will install the application on the default (running) emulator but IT
WILL NOT LAUNCH IT FOR YOU.


### Build a release APK
See this [link](https://developer.android.com/studio/build/building-cmdline#ReleaseMode)


## Troubleshooting

You can debug the inner browser (WebView) by typing

```
chrome://inspect
```

inside your Chrome browser.

You will get something like

![alt text](./webview-debugging.png "Webview Debugging")


### Open

More information here: [Remote Debugging WebViews](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/webviews)