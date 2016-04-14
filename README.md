release-android-library
=======================

Remote script to create a maven compatible release of an android library (aar). This release comes in a zip or exploded form and is only created locally inside your own build folder. You can these use these files to release to JCenter or Maven Central.


####adding to your library
```
apply plugin: 'com.android.library'

ext {
    PUBLISH_GROUP_ID = 'id-library'
    PUBLISH_ARTIFACT_ID = 'library-name'
    PUBLISH_VERSION = '1.0.0'
}

android {
    // configs, flavors etc
}

dependencies {
    // dependencies
}

// Copy the file locally and use
apply from: 'android-release-aar.gradle'
```


####useage

`./gradlew clean build generateRelease`

####example output


```
:rxconnectivitystatus:zipRelease
:rxconnectivitystatus:generateRelease
Release 1.0 can be found at /Users/abderrazak/AndroidStudioProjects/GitRepository/RxConnectivityState/rxconnectivitystatus/build/release/1.0/
Release 1.0 zipped can be found /Users/abderrazak/AndroidStudioProjects/GitRepository/RxConnectivityState/rxconnectivitystatus/build/release-1.0.zip

BUILD SUCCESSFUL

Total time: 2 mins 5.672 secs

```
