# vue native setup guide for windows

Some crucial info, that is not told here: https://vue-native.io/docs/installation.html#Setup-with-Vue-Native-CLI
This is the documentation for the latest version vue-native 0.2.0 (2021-02-26)

## Step Python
(vue-native 0.2.0 is based on react-native 0.59.x, which still requires python)
- Download and install Python2 (e.g. `choco install -y python2`)
- Set env variable `PYTHON_HOME` to install directory
- Add to Path:  `%PYTHON_HOME%;%PYTHON_HOME%\Scripts`

## Step JDK
- Download and install Oracle JDK 8 (e.g. `choco install -y jdk8`)
- Set env variable `JAVA_HOME` to install directory
- Add to Path:  `%JAVA_HOME%\bin`

## Step ADK
- Install Android SDK e.g. using IntelliJ
- Set env variable `ANDROID_SDK_ROOT` to install directory
- Add to Path:  `%ANDROID_SDK_ROOT%\platform-tools`

## Step Node
- Download and install NodeJs 10
- Set env variable `NODE_HOME` to install directory
- Add to Path:  `%NODE_HOME%`
- run `npm install react-native-cli -g`
- run `npm install vue-native-cli -g`
