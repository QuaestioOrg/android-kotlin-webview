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
Edit the URL indirectly from **strings.xml** from:

`   <string name="website_domain">quaestio.org</string>`

`    <string name="website_url">https://quaestio.org</string>`
* to:

`   <string name="website_domain">your.url</string>`

`   <string name="website_url">http://your.url</string>`

Or edit the `loadURL`directly in **MainActivity.kt** from:

`21        mWebView.loadUrl(getString(R.string.website_url))`

`30        if (Uri.parse(url).host == getString(R.string.website_domain)) {`
* to:

`21        mWebView.loadUrl("http://your.url")`

`30        if (Uri.parse(url).host == "your.url") {`

# Credits
A live demo can be seen from this [web app](https://play.google.com/store/apps/details?id=org.quaestio.quaestio.org) which simply loads the homepage of [Quaestio.org](https://quaestio.org/).
* Boilerplate code from [Vamsi Tallapudi](https://github.com/vamsitallapudi/create-android-app-for-website)'s [repository](https://github.com/vamsitallapudi/create-android-app-for-website).
