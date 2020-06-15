RapidMiner Language Pack Template
=============================

A template project for creating a RapidMiner Studio language pack. 

### Prerequisite
* Requires Gradle 4.10.3+ (get it [here](http://gradle.org/installation) or use the Gradle wrapper shipped with this template)

### Getting started
1. Clone the language pack template

2. Change the **language** pack settings in _build.gradle_ (e.g. replace 'EN' by the desired language descriptor)

3. Change how much you want to translate by changing the **i18n_pack** settings in _build.gradle_ (currently available: core, supported)

4. Initialize the language pack project by executing the _initializeExtensionProject_ Gradle task (e.g. via 'gradlew --no-daemon initializeExtensionProject')

5. Provide your translations in the i18n files (by default) located at _/src/main/resources/com/rapidminer/extension/resources/i18n_. Look for the files that end with _"\_<language>"_. Original texts are provided above each key and are preset as well.

6. Add an extension icon by placing an image named "icon.png" (48x48 pixels) in  _src/main/resources/META-INF/_. 

7. Build and install your extension by executing the _installExtension_ Gradle task 

8. Start RapidMiner Studio and check whether your extension has been loaded
