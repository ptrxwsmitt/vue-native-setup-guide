# vue native setup guide for windows

Some crucial info, that is not told here: https://vue-native.io/docs/installation.html#Setup-with-Vue-Native-CLI \
This is the documentation for the latest version vue-native 0.2.0 (2021-02-26)


## Step JDK
- Download and install Open JDK 8 (e.g. https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u282-b08/OpenJDK8U-jdk_x86-32_windows_hotspot_8u282b08.zip)
- Set env variable `JAVA_HOME` to install directory
- Add to Path:  `%JAVA_HOME%\bin`

## Step ADK
- Install Android SDK e.g. using IntelliJ
- Set env variable `ANDROID_SDK_ROOT` to install directory
- Add to Path:  `%ANDROID_SDK_ROOT%\platform-tools`

## Step Node
- Download and install NodeJs 12 LTS
- Set env variable `NODE_HOME` to install directory
- Add to Path:  `%NODE_HOME%`
- run `npm install react-native-cli -g`
- run `npm install vue-native-cli -g`

## Update package.json
Generating an app using `vue-native init VN1Test --no-expo` will result in an application not runnable on NodeJs 12 LTS due to version conflicts.
Update Versions as follows:

`
{
  "name": "VN1Test",
  "version": "0.0.1",
  "private": true,
  "scripts": {
    "start": "node node_modules/react-native/local-cli/cli.js start",
    "test": "jest"
  },
  "dependencies": {
    "react": "16.13.1",
    "react-native": "0.63.4",
    "vue-native-core": "^0.2.0",
    "vue-native-helper": "^0.2.0"
  },
  "devDependencies": {
    "@babel/core": "^7.0.0",
    "@babel/runtime": "7.13.8",
    "babel-jest": "26.6.3",
    "jest": "26.6.3",
    "metro-react-native-babel-preset": "0.65.1",
    "react-test-renderer": "16.13.1",
    "vue-native-scripts": "^0.2.0"
  },
  "jest": {
    "preset": "react-native"
  }
}
`
