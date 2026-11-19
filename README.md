# VRock Navigation SDK for Android

This repository distributes compiled VRock Navigation SDK artifacts for Android. The current release is **0.1.3**. It supports Android 8.0 (API 26) and later.

## Add the Maven repository

Add this repository under `dependencyResolutionManagement.repositories` in your app's `settings.gradle.kts`. Keep `google()` and `mavenCentral()` for Android and third-party dependencies.

```kotlin
maven {
    url = uri("https://bboyv-rock.github.io/vrock-navigation-sdk-distribution/maven/")
    content { includeGroup("com.vrock.navigation") }
}
```

The Maven endpoint supports anonymous downloads. No GitHub account or access token is required.

## Add the SDK

For a ready-made navigation Activity or Fragment with OSRM, add these dependencies to your app's `build.gradle.kts`:

```kotlin
dependencies {
    implementation("com.vrock.navigation:navigation-ui-view:0.1.3")
    implementation("com.vrock.navigation:navigation-routing:0.1.3")
}
```

| Add-on | Maven artifact |
| --- | --- |
| Jetpack Compose navigation UI | `com.vrock.navigation:navigation-ui:0.1.3` |
| Google Routes | `com.vrock.navigation:navigation-routing-google:0.1.3` |
| Google Maps renderer | `com.vrock.navigation:navigation-map-google:0.1.3` |
| Android GPS provider | `com.vrock.navigation:navigation-location:0.1.3` |

Google Maps and Google Routes require a Google API key. SDK activation for release apps is separate from Maven access.

See the [Android example](https://github.com/BboyV-Rock/vrock-navigation-example-android) for a runnable integration.
