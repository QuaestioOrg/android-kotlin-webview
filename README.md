# Kotlin Converted WebView

# Description
A [WebView](https://developer.android.com/guide/webapps/webview.html) simply converted from Java to Kotlin using the basic [Android Studio tool](https://developer.android.com/kotlin/get-started.html#convert-to-kotlin-code).

# Installation
* Clone the project;
* unzip the folder;
* run Android Studio;
* open a new project;
* and pick the package.

# Usage
Edit the URL indirectly from **strings.xml**.
* From:
`        <string name="url_website">https://quaestio.org/</string>`
* To:
`        <string name="url_website">https://quaestio.org/</string>`

Or edit the `loadURL`directly in **MainActivity.kt**.
* From:
`        mWebView.loadUrl(getString(R.string.url_website))`
* To:
`        mWebView.loadUrl("http://your.url/")`


# Credits
A live demo can be seen from this [web app](https://play.google.com/store/apps/details?id=org.quaestio.quaestio.org) which simply loads the homepage of [Quaestio.org](https://quaestio.org/).
* Boilerplate code from [Vamsi Tallapudi](https://github.com/vamsitallapudi/create-android-app-for-website)'s [repository](https://github.com/vamsitallapudi/create-android-app-for-website).
