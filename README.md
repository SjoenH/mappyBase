# mappyBase

Goal: Using Firebase and Google Maps plugin in an ionic project.

Here is the steps to reproduce the problem, with a terminal dump.

Started the project 

    ionic start mappyBase -v2

Added Android platform:
    
    ionic platform add android

Installed the ionic native core:

    npm install @ionic-native/core --save

Installed the Firebase plugin [link](http://ionicframework.com/docs/native/firebase/)

    ionic plugin add cordova-plugin-firebase
    npm install --save @ionic-native/firebase

Projects still builds.

Installed the Google Maps Plugin [link](http://ionicframework.com/docs/native/google-maps/)

    ionic plugin add cordova-plugin-googlemaps --variable API_KEY_FOR_ANDROID="AIzaSyDZGI8ZsY8RGXnfPBJToVyPezJMhJeI0pI" --variable API_KEY_FOR_IOS="AIzaSyDZGI8ZsY8RGXnfPBJToVyPezJMhJeI0pI"
    npm install --save @ionic-native/google-maps

Project will not build...

Here is the terminal dump.


```{r, engine='bash', count_lines}
[henry@Archie mappyBase]$ npm install --save @ionic-native/google-maps
ionic-hello-world@ /home/henry/Projects/mappyBase
└── @ionic-native/google-maps@3.4.4 

npm WARN optional SKIPPING OPTIONAL DEPENDENCY: fsevents@^1.0.0 (node_modules/chokidar/node_modules/fsevents):
npm WARN notsup SKIPPING OPTIONAL DEPENDENCY: Unsupported platform for fsevents@1.1.1: wanted {"os":"darwin","arch":"any"} (current: {"os":"linux","arch":"x64"})
[henry@Archie mappyBase]$ ionic run android --device
> ionic-hello-world@ ionic:build /home/henry/Projects/mappyBase
> ionic-app-scripts build "--device"

[18:29:21]  ionic-app-scripts 1.1.4 
[18:29:21]  build dev started ... 
[18:29:21]  clean started ... 
[18:29:21]  clean finished in 2 ms 
[18:29:21]  copy started ... 
[18:29:21]  transpile started ... 
[18:29:23]  transpile finished in 2.15 s 
[18:29:23]  preprocess started ... 
[18:29:23]  preprocess finished in less than 1 ms 
[18:29:23]  webpack started ... 
[18:29:23]  copy finished in 2.35 s 
[18:29:29]  webpack finished in 5.59 s 
[18:29:29]  sass started ... 
[18:29:30]  sass finished in 980 ms 
[18:29:30]  postprocess started ... 
[18:29:30]  postprocess finished in 1 ms 
[18:29:30]  lint started ... 
[18:29:30]  build dev finished in 8.77 s 
[18:29:31]  lint finished in 1.29 s 
ANDROID_HOME=/home/henry/Android/Sdk

JAVA_HOME=/usr/lib/jvm/java-8-jdk

Subproject Path: CordovaLib

Incremental java compilation is an incubating feature.


:preBuild UP-TO-DATE
:preDebugBuild UP-TO-DATE
:checkDebugManifest
:CordovaLib:preBuild UP-TO-DATE
:CordovaLib:preDebugBuild UP-TO-DATE
:CordovaLib:checkDebugManifest
:CordovaLib:prepareDebugDependencies
:CordovaLib:compileDebugAidl


:CordovaLib:compileDebugNdk
 UP-TO-DATE
:CordovaLib:compileLint


:CordovaLib:copyDebugLint
 UP-TO-DATE
:CordovaLib:mergeDebugShaders


:CordovaLib:compileDebugShaders

:CordovaLib:generateDebugAssets
:CordovaLib:mergeDebugAssets
:CordovaLib:mergeDebugProguardFiles UP-TO-DATE
:CordovaLib:packageDebugRenderscript UP-TO-DATE
:CordovaLib:compileDebugRenderscript

:CordovaLib:generateDebugResValues
:CordovaLib:generateDebugResources
:CordovaLib:packageDebugResources


:CordovaLib:processDebugManifest


:CordovaLib:generateDebugBuildConfig


:CordovaLib:processDebugResources

:CordovaLib:generateDebugSources

:CordovaLib:incrementalDebugJavaCompilationSafeguard


:CordovaLib:compileDebugJavaWithJavac

:CordovaLib:compileDebugJavaWithJavac - is not incremental (e.g. outputs have changed, no previous execution, etc.).

Note: Some input files use or override a deprecated API.
Note: Recompile with -Xlint:deprecation for details.

:CordovaLib:processDebugJavaRes
 UP-TO-DATE

:CordovaLib:transformResourcesWithMergeJavaResForDebug

:CordovaLib:transformClassesAndResourcesWithSyncLibJarsForDebug


:CordovaLib:mergeDebugJniLibFolders


:CordovaLib:transformNative_libsWithMergeJniLibsForDebug


:CordovaLib:transformNative_libsWithSyncJniLibsForDebug


:CordovaLib:bundleDebug


:prepareAndroidCordovaLibUnspecifiedDebugLibrary

:preReleaseBuild UP-TO-DATE
:CordovaLib:preReleaseBuild UP-TO-DATE
:CordovaLib:checkReleaseManifest

:CordovaLib:prepareReleaseDependencies
:CordovaLib:compileReleaseAidl

:CordovaLib:compileReleaseNdk UP-TO-DATE
:CordovaLib:copyReleaseLint UP-TO-DATE
:CordovaLib:mergeReleaseShaders

:CordovaLib:compileReleaseShaders
:CordovaLib:generateReleaseAssets

:CordovaLib:mergeReleaseAssets

:CordovaLib:mergeReleaseProguardFiles UP-TO-DATE
:CordovaLib:packageReleaseRenderscript UP-TO-DATE
:CordovaLib:compileReleaseRenderscript

:CordovaLib:generateReleaseResValues

:CordovaLib:generateReleaseResources
:CordovaLib:packageReleaseResources

:CordovaLib:processReleaseManifest


:CordovaLib:generateReleaseBuildConfig


:CordovaLib:processReleaseResources


:CordovaLib:generateReleaseSources

:CordovaLib:incrementalReleaseJavaCompilationSafeguard

:CordovaLib:compileReleaseJavaWithJavac

:CordovaLib:compileReleaseJavaWithJavac - is not incremental (e.g. outputs have changed, no previous execution, etc.).

Note: Some input files use or override a deprecated API.

Note: Recompile with -Xlint:deprecation for details.

:CordovaLib:processReleaseJavaRes UP-TO-DATE
:CordovaLib:transformResourcesWithMergeJavaResForRelease


:CordovaLib:transformClassesAndResourcesWithSyncLibJarsForRelease

:CordovaLib:mergeReleaseJniLibFolders

:CordovaLib:transformNative_libsWithMergeJniLibsForRelease


:CordovaLib:transformNative_libsWithSyncJniLibsForRelease

:CordovaLib:bundleRelease

:prepareComAndroidSupportSupportV42400Library


:prepareComGoogleAndroidGmsPlayServicesBase1021Library


:prepareComGoogleAndroidGmsPlayServicesBasement1021Library


:prepareComGoogleAndroidGmsPlayServicesLocation980Library


:prepareComGoogleAndroidGmsPlayServicesMaps980Library

:prepareComGoogleAndroidGmsPlayServicesTasks1021Library

:prepareComGoogleFirebaseFirebaseAnalytics1021Library

:prepareComGoogleFirebaseFirebaseAnalyticsImpl1021Library

:prepareComGoogleFirebaseFirebaseCommon1021Library

:prepareComGoogleFirebaseFirebaseConfig1021Library

:prepareComGoogleFirebaseFirebaseCore1021Library

:prepareComGoogleFirebaseFirebaseCrash1021Library

:prepareComGoogleFirebaseFirebaseIid1021Library


:prepareComGoogleFirebaseFirebaseMessaging1021Library

:prepareMeLeolinShortcutBadger114Library

:prepareDebugDependencies
:compileDebugAidl

:compileDebugRenderscript


:generateDebugBuildConfig


:generateDebugResValues

:generateDebugResources
:mergeDebugResources

:processDebugManifest


:processDebugResources


:generateDebugSources


:incrementalDebugJavaCompilationSafeguard

:compileDebugJavaWithJavac

:compileDebugJavaWithJavac - is not incremental (e.g. outputs have changed, no previous execution, etc.).

/home/henry/Projects/mappyBase/platforms/android/src/plugin/google/maps/PluginPolyline.java:37: error: cannot access AbstractSafeParcelable

        polylineOptions.add(path.get(i));
                       ^
  class file for com.google.android.gms.common.internal.safeparcel.AbstractSafeParcelable not found

Note: Some input files use or override a deprecated API.
Note: Recompile with -Xlint:deprecation for details.

1 error

:compileDebugJavaWithJavac FAILED



FAILURE: Build failed with an exception.


* What went wrong:
Execution failed for task ':compileDebugJavaWithJavac'.
> Compilation failed; see the compiler error output for details.

* Try:
Run with 
--stacktrace option to get the stack trace. Run with --info or --debug option to get more log output.


BUILD FAILED

Total time: 18.065 secs

Error: /home/henry/Projects/mappyBase/platforms/android/gradlew: Command failed with exit code 1 Error output:
Note: Some input files use or override a deprecated API.
Note: Recompile with -Xlint:deprecation for details.
Note: Some input files use or override a deprecated API.
Note: Recompile with -Xlint:deprecation for details.
/home/henry/Projects/mappyBase/platforms/android/src/plugin/google/maps/PluginPolyline.java:37: error: cannot access AbstractSafeParcelable
        polylineOptions.add(path.get(i));
                       ^
  class file for com.google.android.gms.common.internal.safeparcel.AbstractSafeParcelable not found
Note: Some input files use or override a deprecated API.
Note: Recompile with -Xlint:deprecation for details.
1 error

FAILURE: Build failed with an exception.

* What went wrong:
Execution failed for task ':compileDebugJavaWithJavac'.
> Compilation failed; see the compiler error output for details.

* Try:
Run with --stacktrace option to get the stack trace. Run with --info or --debug option to get more log output.

```

It looks like the gradle config is off...
Hypotesis: the plugins use different versions of gms and it looks for a package that is not in that version or something...
If I manually edit the `build.gradle` in the android platorm folder, I can specify the same version for both plugins.

I change the versions for gms play services to the latest with `+`.
It now looks like this:

```{r, engine='gradle', count_lines}
    dependencies {
    compile fileTree(dir: 'libs', include: '*.jar')
    // SUB-PROJECT DEPENDENCIES START
    debugCompile(project(path: "CordovaLib", configuration: "debug"))
    releaseCompile(project(path: "CordovaLib", configuration: "release"))
    compile "com.google.firebase:firebase-core:+"
    compile "com.google.firebase:firebase-messaging:+"
    compile "com.google.firebase:firebase-crash:+"
    compile "com.google.firebase:firebase-config:+"
    compile "com.google.android.gms:play-services-maps:+"
    compile "com.google.android.gms:play-services-location:+"
    // SUB-PROJECT DEPENDENCIES END
}
```
Because running `ionic run android --device` rebuilds the gradle file, we have to run gradle on itself. I use Android studio and just press run. 
Going through Android studio I can now build the app with both plugins!

We have to find a better solution. Editing some ionic config.