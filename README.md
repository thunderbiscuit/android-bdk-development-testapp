# Readme
The purpose of this repository is to dry-run your local development setup for Android and the [bitcoindevkit](https://github.com/bitcoindevkit). It consists of 2 potential tasks: 
1. Building the app on the `master` branch of this repository
2. Building the app on the `bdk-library` branch of this repository

## Requirements
To accomplish the two tasks above you will need:
1. Android Studio
2. A phone with Android 6 or above (Android Marshmallow, API level 23) with USB debugging activated _OR_ an emulator on your development machine
3. The bitcoindevkit library (for task 2)

### Android Studio
The easiest way to install/uninstall Android Studio is through JetBrains' [Toolbox app](https://www.jetbrains.com/toolbox-app/), but any way you get a working Android Studio on your computer is fine. You can find the download link to install Android Studio `4.2.2` (latest stable release) [here](https://developer.android.com/studio).

### Phone with USB debugging activated
Running your apps on a phone is more fun than using the emulators. Installing apps from Android Studio directly on your phone requires that you (a) have you phone connected to your computer via USB cable, and (b) that you have _USB debugging_ activated. The specifics of how to do this is phone and vendor dependent, so you'll have to figure out how to turn that on for your own phone. It usually consists of turning on _Developer Options_ via something like `Settings -> System -> About Phone -> Software Info -> Build Number` and pressing the `Build number` 7 times. From there you'll find a new section at `Settings -> System -> Developer options`, and there you'll be able to toggle on `USB debugging`. [See this link for more info](https://developer.android.com/studio/run/device). Because all setups are different, expect having to do a bit of googling for this to work.

### Emulators
You can install emulators for a range of devices (that's the beauty of emulators) on any computer directly from Android Studio. Click on the dropdown menu (pictured below) and select `AVD Manager`. From there, follow the instructions and install an emulator of your choosing with a recent API level (Pixel 3 with API 30 is a good choice). Note that there is a known issue with emulators on Ubuntu OS which makes them very slow. In general if your local development machine runs on a Linux distro, consider using a phone for testing/debugging.

### Bitcoindevkit library
Simply add the bitcoindevkit android library as one of your dependencies using:
```kotlin
// Kotlin DSL
dependencies {
    implementation("org.bitcoindevkit:bdk-android:0.5.1")
}
```

The source code for the library is here: [bdk-kotlin](https://github.com/bitcoindevkit/bdk-kotlin). 

## Run the app
Once you have all of the above, you should be able to open this repository in Android Studio, choose a device in the dropdown menu (emulator or USB connected hardware) and simply press 'run' (the green triangle). Both branches of this repository should build an app that will fire up on your phone, fully installed (in other words you can disconnect your phone and the app will keep working).
 
<center>
    <img src="./images/run-app.png" width="700px" />
</center>

## Expected output
<center>
    <img src="./images/part-1.gif" width="300px"/>
</center>
