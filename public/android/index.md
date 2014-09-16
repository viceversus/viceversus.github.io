title: UI Testing for Android
author:
  name: Ken Shimizu
  twitter: vice_versus_
output: index.html

--
# UI Testing On Android
--
## Two main options

Robotium (Google/Contributors)

Espresso (Google)

--
## Robotium
### Pros
* Easy to write and read
* Docs are good
* A good community around it

### Cons
* Slooooooow
* Timing issues
--

## Espresso

### Pros
* Super fast
* Reliable

### Cons
* Painful to write
* Docs are terrible
* Imports, imports, imports
--

# Getting Started

--

## Including the libraries!

## Two ways to do it

--

## .jar files

1. Download the [Robotium](https://code.google.com/p/robotium/downloads/list) or [Espresso](https://code.google.com/p/android-test-kit/source/browse/#git%2Fbin%2Fespresso-standalone%253Fstate%253Dclosed) .jar files.
1. Create a `libs` directory in:
  1a. Eclipse: At the same level as your `src` directory.
  1b. Android Studio: Inside your `app` directory.
1. (For Android Studio only) Right click the .jar file and select 'Add as Library'

--

## Gradle Sync

Add this to your gradle.build file under `dependencies`

Robotium:

    compile 'com.jayway.android.robotium:robotium-solo:5.0.1'

    androidTestCompile 'com.jayway.android.robotium:robotium-solo:5.0.1'

Espresso:

    androidTestCompile 'com.jakewharton.espresso:espresso:1.1-r3'

Then gradle sync

--

## Configuration for Espresso

For Eclipse:

    <instrumentation
      android:name="com.google.android.apps.common.testing.testrunner.GoogleInstrumentationTestRunner"
      android:targetPackage="$YOUR_TARGET_APP_PACKAGE"/>

For Android Studio:

    android {
      defaultConfig {
        testInstrumentationRunner "com.google.android.apps.common.testing.testrunner.GoogleInstrumentationTestRunner"
      }
    }

--

Then set your run configuration to use that test runner

* Eclipse: Run -> Run Configurations

* Android Studio: Run -> Edit Configurations

--

Now you're ready to write your first test!

--

# Let's write our first test

Logging in and logging in and logging out a user

--

## Robotium



--

## Espresso



--

## Getting it up on Travis



--
