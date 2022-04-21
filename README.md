# Fork from Sceneform v1.16.0 (Open source version)

![status: active](https://img.shields.io/badge/status-active-green.svg)

## Getting started

Use the following steps to include and build the Sceneform 1.16.0 SDK with your
app:

1. Download `sceneform-android-sdk-1.16.0.zip` from the Sceneform SDK
   [releases](https://github.com/google-ar/sceneform-android-sdk/releases/tag/v1.16.0)
   page.
2. Extract the `sceneformsrc` and `sceneformux` directories into your project's
   top-level directory. The resulting directory structure should be similar to
   the following:
```
project
+-- app
|   +-- build.gradle
|   +-- ...
+-- sceneformsrc
+-- sceneformux
+-- build.gradle
+-- settings.gradle
+-- ...
```

3. Modify your project's `settings.gradle` to include the Sceneform projects:
```
include ':app'

// Add these lines:
include ':sceneform'
project(':sceneform').projectDir=new File('sceneformsrc/sceneform')

include ':sceneformux'
project(':sceneformux').projectDir=new File('sceneformux/ux')
```

4. Finally, add a reference to the Sceneform SDK to your app's `build.gradle`:
```
dependencies {
    api project(":sceneformux")
}
```

To get started with the Sceneform SDK, check out the
[Sceneform sample](https://github.com/google-ar/sceneform-android-sdk/tree/master/samples/gltf/app).
