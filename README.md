# Bugsee for Jetpack Compose

## Protecting views

In addition we support a way to mark your custom sensitive views so they will be hidden from the recorded video. We provide ***BugseeProtect*** composable function for this ([BugseeProtect.kt](https://github.com/bugsee/bugsee-compose)).

```kotlin
setContent {
    ...
    val secureContent = @Composable {
        Text(text = "Confidential.")
    }

    BugseeProtect(
        contentToHide = { secureContent() }
    )
    ...
}