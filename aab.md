# AAB Research

## AAB: Android App Bundle
     includes all your app’s compiled code and resources
     defers APK generation and signing to Google Play.
Link [app-bundle](https://developer.android.com/guide/app-bundle)

## Bundletool: Underlying tool, that Android Studio, the Android Gradle plugin, and Google Play use to build an Android App Bundle
    convert an app bundle into the various APKs that are deployed to devices. 
    bundletool is also available to you as a command line tool, 
    so you can build app bundles yourself and recreate Google Play’s server-side build of your app’s APKs.

Bundletool [Bundletool](https://developer.android.com/studio/command-line/bundletool)
Download [Bundletool_repo](https://github.com/google/bundletool/releases)

## Bundletool Usage:  

* build-apks:  
java -jar bundletool.jar build-apks --ks=vivid_hmi.keystore --ks-pass=pass:android --ks-key-alias=android --key-pass=pass:android  --bundle=launcher_app2_fragmentBasedScoutDriveRelease-0.55.1-signed.aab --output=\local\my_app.apks

* install-apks:  
java -jar bundletool.jar install-apks --apks=G:\01localapp\aab\local1\my_app.apks

## Bundletool with Android studio
* steps:  
`run`->`edit configurations`->select Android App like `katas`->`Installation Options`->select `APK from app bundle`->`OK`->Than `run`  
* Build Output bundle relative tasks:  
    * Task :katas:bundleReleaseResources  
    * Task :katas:buildReleasePreBundle  
    * Task :katas:packageReleaseBundle  
    * Task :katas:makeApkFromBundleForRelease  
  
* Build output:  
    * aab path: ..\build\intermediates\intermediary_bundle\release\
    * apks path: ..\build\intermediates\apks_from_bundle\release\
    * apk path: ..\build\intermediates\extracted_apks\release\out\

## More
The Android Gradle Plugin [README.md](https://android.googlesource.com/platform/tools/base/+/studio-master-dev/build-system/README.md)

