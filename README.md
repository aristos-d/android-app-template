# A minimal Android app template

The goal is to create a minimal Android application template that can be built
with Gradle from the command line without Android Studio involved.


## Requirements

* Android SDK must be available. Create a *local.properties* file and set
  `sdk.path` to point to where the SDK is installed.

* Gradle must be available for the bootstrap process, i.e. to create Gradle
  Wrapper.


## Bootstrap

Android Studio projects typically include Gradle Wrapper in version control to
make life easier. However, this tactic requires committing a compiled JAR file
which is _not_ cool. Instead, create the wrapper yourself using an existing
Gradle installation [01] like so:

```
$ gradle wrapper --gradle-version=7.0.3
```

This command can also be used to change the used version of Gradle. Then, to
build:

```
$ ./gradlew build
```


## Customization

* In *app/build.gradle*, configure target SDK version, minimum SDK version, NDK
  version, the application's ID and the application version.

* In *app/src/main/values/strings.xml*, configure user-visible strings
  including the displayed application name.


## References

[01] <https://gradle.org/install/>
