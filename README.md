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
