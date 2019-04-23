
# react-native-okay-sdk

## Getting started

`$ npm install react-native-okay-sdk --save`

### Mostly automatic installation

`$ react-native link react-native-okay-sdk`

### Manual installation


#### iOS

1. In XCode, in the project navigator, right click `Libraries` ➜ `Add Files to [your project's name]`
2. Go to `node_modules` ➜ `react-native-okay-sdk` and add `RNOkaySdk.xcodeproj`
3. In XCode, in the project navigator, select your project. Add `libRNOkaySdk.a` to your project's `Build Phases` ➜ `Link Binary With Libraries`
4. Run your project (`Cmd+R`)<

#### Android

1. Open up `android/app/src/main/java/[...]/MainActivity.java`
  - Add `import com.reactlibrary.RNOkaySdkPackage;` to the imports at the top of the file
  - Add `new RNOkaySdkPackage()` to the list returned by the `getPackages()` method
2. Append the following lines to `android/settings.gradle`:
  	```
  	include ':react-native-okay-sdk'
  	project(':react-native-okay-sdk').projectDir = new File(rootProject.projectDir, 	'../node_modules/react-native-okay-sdk/android')
  	```
3. Insert the following lines inside the dependencies block in `android/app/build.gradle`:
  	```
      compile project(':react-native-okay-sdk')
  	```

#### Windows
[Read it! :D](https://github.com/ReactWindows/react-native)

1. In Visual Studio add the `RNOkaySdk.sln` in `node_modules/react-native-okay-sdk/windows/RNOkaySdk.sln` folder to their solution, reference from their app.
2. Open up your `MainPage.cs` app
  - Add `using Okay.Sdk.RNOkaySdk;` to the usings at the top of the file
  - Add `new RNOkaySdkPackage()` to the `List<IReactPackage>` returned by the `Packages` method


## Usage
```javascript
import RNOkaySdk from 'react-native-okay-sdk';

// TODO: What to do with the module?
RNOkaySdk;
```
  