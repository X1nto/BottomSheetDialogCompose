# BottomSheetDialogCompose
A bottom sheet dialog for Jetpack Compose that provides the same syntax as AlertDialog.

Installation
-------
### Groovy
Add JitPack repository to root build.gradle
```groovy
allprojects {
    repositories {
        ...
        maven { url 'https://jitpack.io' }
    }
}
```
Add OverlappingPanelsCompose dependency to app build.gradle
```groovy
dependencies {
    implementation 'com.github.X1nto:BottomSheetDialogCompose:1.0.0'
}
```
### Kotlin DSL
Add JitPack repository to root build.gradle
```kotlin
allprojects {
    repositories {
        ...
        maven(url = "https://jitpack.io")
    }
}
```
Add OverlappingPanelsCompose dependency to app build.gradle
```kotlin
dependencies {
    implementation("com.github.X1nto:BottomSheetDialogCompose:1.0.0")
}
```

Basic usage
-------
```kotlin
var showDialog by remember { mutableStateOf(false) }
Button(onClick = {
    showDialog = true
}) {
    Text("Show Dialog")
}
if (showDialog) {
    BottomSheetDialog(onDismissRequest = {
        showDialog = false
    }) {
        //Your content
    }
}
```
Check out the [sample app](/app) for a better example on how to use the library.