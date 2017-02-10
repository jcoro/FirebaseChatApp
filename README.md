# FriendlyChat

This repository contains code for the FriendlyChat project in the [Firebase in a Weekend: Android by Google](https://www.udacity.com/course/firebase-in-a-weekend-by-google-android--ud0352) Udacity course.

## Overview

FriendlyChat is an app that allows users to send and receive text and photos in realtime across platforms.

## Setup

Setup requires creating a Firebase project. See https://firebase.google.com/ for more information.

## License
See [LICENSE](LICENSE)

Notes:
There appears to be a problem with FirebaseAuth / FirebaseAuth UI where the display name for a newly-created user can't be retrieved. Using older versions seemed to fix it:
```
compile 'com.google.firebase:firebase-auth:9.6.1'
// FirebaseUI Auth only
compile 'com.firebaseui:firebase-ui-auth:0.6.1'
```
More on the issue:
(https://github.com/firebase/FirebaseUI-Android/issues/409).
```
GRADLE ERROR: Failed to resolve: com.twitter.sdk.android:twitter:2.0.0
```
Soved by adding the following to app-level build.gradle repositories:
```
maven { url 'https://maven.fabric.io/public' }
```
i.e.,
```
repositories {
    mavenLocal()
    flatDir {
        dirs 'libs'
    }
    maven { url 'https://maven.fabric.io/public' }
}
```
More on the issue:
(https://github.com/firebase/FirebaseUI-Android/issues/392)
(https://github.com/firebase/FirebaseUI-Android/blob/master/auth/README.md)

If you have any questions I'd be happy to try and help. Please contact me at: john@coronite.net.


