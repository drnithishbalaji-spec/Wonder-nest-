WonderNest
WonderNest is a small, no-login learning app for word meanings and number maths, with tools to search websites and open a web address directly. Website search uses Bing. Search results and websites open outside WonderNest and their content is not controlled or filtered by this app.

What it does
	•	Looks up one English word at a time and displays up to three definitions from the public Dictionary API at `dictionaryapi.dev`. Definitions containing blocked rude/explicit terms or link-like text are not shown.
	•	Solves arithmetic expressions and shows calculation steps. It supports `+`, `-`, `×`/`*`, `÷`/`/`, brackets, powers, percentages, square roots, and phrases such as “12 times 3” and “25% of 80”. Multiplication and division are handled before addition and subtraction.
	•	Searches the web through Bing. Search results open in the device/browser, where the listed website links are directly clickable.
	•	Opens one exact `http://` or `https://` address entered by the user. If the scheme is omitted, WonderNest adds `https://`.
	•	Rejects rude/explicit terms in the word, maths, website-search, and URL inputs. Dictionary definitions and word-type labels are filtered before display. This is a basic filter, not a guarantee that every inappropriate term will be caught.
	•	Runs calculations locally. Word lookups need an internet connection. Website searches and direct URLs open outside WonderNest; external search results and website pages cannot be filtered or controlled by this app.

Files
	•	`index.html` — the complete standalone website (HTML, CSS, and JavaScript).
	•	`android/` — the Android WebView wrapper project. Its Gradle build copies the current root `index.html` into the APK automatically.
	•	`README.md` — this guide.

Run the website locally
Open `index.html` in a modern browser. Maths works offline; word meanings need internet access. Website searches open Bing in a new browser tab, with clickable result links. Direct URLs also open in a new tab.

Build the Android APK
The Android project uses Java 17 or newer, Android SDK Platform 35, and Android Build Tools 35.0.0. Set `ANDROID_HOME` to your Android SDK location if it is not already configured.

From the project folder, run:


 cd android
./gradlew assembleDebug
 
The installable debug APK is created at:


 android/app/build/outputs/apk/debug/app-debug.apk
 
To install it on a connected Android device with USB debugging enabled:


 adb install -r app/build/outputs/apk/debug/app-debug.apk
 
The APK is debug-signed for testing and sideloading; it is not a Play Store release. The app loads the bundled learning page and sends website searches and entered URLs to the device’s external browser. Android needs internet access for dictionary lookups, website searches, and visited sites.

Keep the project local
No web hosting or publishing is required. The site can be opened from its local file, and the Android app can be built and installed directly from the project files.
