RapidMiner Language Pack Template
=============================

A template project for creating a RapidMiner Studio language pack. 

### Prerequisite
* Requires Gradle 4.10.3+ (use the Gradle wrapper shipped with this template or get it [here](http://gradle.org/installation))

### Getting started
1. Clone the language pack template

2. Change the **language** pack settings in _build.gradle_ (e.g. replace 'EN' by the desired language descriptor; you can find supported language locales [here](https://www.oracle.com/java/technologies/javase/jdk8-jre8-suported-locales.html). Simple locales like 'EN', 'IT' or 'DE' are allowed as well)

3. Change how much you want to translate by changing the **i18n_pack** settings in _build.gradle_ (currently available: core, supported).
 Check the comment in _build.gradle_ for an explanation of the available i18n packs.

4. Change the RapidMiner Studio dependency to a version of your liking (must be at least 9.1.0)

5. Initialize the language pack project by executing the _initializeExtensionProject_ Gradle task (e.g. via 'gradlew initializeExtensionProject')

6. Provide your translations in the i18n files (by default) located at _/src/main/resources/com/rapidminer/extension/resources/i18n_. Look for the files that end with _"\_\<language>"_. Original texts are provided above each key and are preset as well.

7. Optionally, add an extension icon by placing an image named "icon.png" (48x48 pixels) in  _src/main/resources/META-INF/_. 

8. Build and install your extension by executing the _installExtension_ Gradle task 

9. Start RapidMiner Studio and check whether your extension has been loaded and change the language setting to check your translation after a restart

### Sharing your translations
To share your language pack with the RapidMiner community, you can register your extension on the [RapidMiner Marketplace](https://marketplace.rapidminer.com/UpdateServer/faces/restricted/file_product_request.xhtml).
The information that you will need are the following
* Product Name: The name of your language pack.
* Product ID: You will need to provide the ID as follows *rmx_language_pack_<lang>*, where the *lang* placeholder
is your language with all separators (like dash "-" and underscore "_") removed and all lower case.
* A short description of the language pack

You can also set the development stage of your translation and provide a website link if you like. 

### Resetting extension
You can use the _reset_ Gradle task to reset the extension to its pre-initialized state and start from scratch.
 
 **NOTE:** This will delete all classes and resources etc-. Be mindful before using this task.

### Notes and limitations
* Not all extensions have proper i18n; e.g. Auto Model/Turbo Prep have a lot of hard coded text
* New HTML views might not allow translations
* Operator help xmls cannot be translated at the current state (9.7)
* Tutorials and Templates cannot be translated at the current state (9.7)
* _Open Sans_ is the hard coded font in several places. Since this font does not include all UTF8 characters, users would need a modified font installed
