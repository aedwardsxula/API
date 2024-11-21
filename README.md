# README

[Luis Vespa's Medium](https://www.mobileinsights.dev/making-get-requests-to-a-rest-api-with-kotlin-and-gson-in-android-9005ef75546e)

1. Create a new Android Studio project.
2. Tell Gradle to build with GSON, a JSON parser.  He says add to build.gradle (module)'s dependency section.
   `implementation 'com.google.code.gson:gson:2.8.8'`
   This doesn't seem correct.

   https://github.com/google/gson is the source so let's look at the README
   `implementation 'com.google.code.gson:gson:2.11.0'`
   This doesn't seem correct but they give a Maven Central download link

   `https://maven-badges.herokuapp.com/maven-central/com.google.code.gson/gson`
   `https://mvnrepository.com/artifact/com.google.code.gson/gson/2.11.0`
   Let's try their Gradle dependency
   `implementation("com.google.code.gson:gson:2.11.0")`

3. Sync Gradle so it downloads GSON.  Sometimes need to clean stuff by using
   File | Invalidate Caches
4. Now let's see what some Nintendo API response looks like (no API key needed)
   `https://www.amiiboapi.com`
   `https://www.amiiboapi.com/docs/`
   `https://www.amiiboapi.com/api/amiibo/`
5. Look in the AmiiboItem class to see how this relates to the API response.
6. We need to give our app permission to access the Internet.  In AndroidManifest.xml
     `<uses-permission android:name="android.permission.INTERNET" />`
