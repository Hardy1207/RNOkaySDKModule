### Installation

##### 1) Create folder "custom_modules" in your project root folder: 
---
* Project_Name/custom_modules
##### 2) Added folder with library to your "custom_modules" folder:
---
* Project_Name/custom_modules/OkaySDK
##### 3) Added to package.json "dependencies":
---
*  "react-native-okay-sdk": "file:custom_modules/OkaySDK"
##### 4) Install node_modules:
---
```sh
$ npm install
```
##### 5) Link library with react-native:
---
```sh
$ react-native link react-native-okay-sdk
```
##### 6) Link library with react-native:
---
* Open Project_Name/android/build.gradle
* Set minSdkVersion in build.gradle
```sh
buildscript {
    ext {
        buildToolsVersion = "28.0.3"
        minSdkVersion = 21 // Change this to 21
        compileSdkVersion = 28
        targetSdkVersion = 28
        supportLibVersion = "28.0.0"
    }
    .....
}
```
* Added maven repository to build.gradle
```sh
allprojects {
    repositories {
        mavenLocal()
        google()
        jcenter()
        maven {
            // All of React Native (JS, Obj-C sources, Android binaries) is installed from npm
            url "$rootDir/../node_modules/react-native/android"

        }
        // Begin: Added This
        maven {
            url 'https://dl.bintray.com/itrtestorg/maven'
        }
        // End:
    }
}
```
##### 7) Added permissions to AndroidManifest.xml:
---
* Open Project_Name/android/src/main/AndroidManifest.xml
* Added user-permissions to AndroidManifest.xml
````sh
    <uses-permission android:name="android.permission.INTERNET" />
    <uses-permission android:name="android.permission.READ_PHONE_STATE"/>
    <uses-permission android:name="android.permission.ACCESS_WIFI_STATE"/>
    <uses-permission android:name="android.permission.ACCESS_NETWORK_STATE"/>
    <uses-permission android:name="android.permission.WRITE_EXTERNAL_STORAGE"/>
    <uses-permission android:name="android.permission.READ_EXTERNAL_STORAGE"/>
````

##### 8) Install react-native Firebase:
* https://rnfirebase.io/docs/v5.x.x/installation/initial-setup
* https://rnfirebase.io/docs/v5.x.x/installation/android
* https://rnfirebase.io/docs/v5.x.x/messaging/android
