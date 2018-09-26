# Android Kotlin WebView

## Description
An [Android WebView](https://developer.android.com/guide/webapps/webview.html) simply converted from Java to Kotlin using the basic [Android Studio tool](https://developer.android.com/studio/projects/add-kotlin#convert-to-kotlin-code).

## Table of Contents
* [Installation](https://github.com/QuaestioOrg/kotlin-converted-webview#installation)
* [Usage](https://github.com/QuaestioOrg/kotlin-converted-webview#usage)
* [Contributing](https://github.com/QuaestioOrg/kotlin-converted-webview#contributing)
* [Credits](https://github.com/QuaestioOrg/kotlin-converted-webview#credits)
* [License](https://github.com/QuaestioOrg/kotlin-converted-webview#license)

## Installation
1. Clone the project;
2. unzip the folder;
3. run [Android Studio](https://developer.android.com/studio/index.html);
4. open a new project;
5. and pick the package.

## Usage
Change the URL indirectly from [strings.xml](https://github.com/QuaestioOrg/kotlin-converted-webview/blob/master/app/src/main/res/values/strings.xml) from:

`   <string name="website_domain">quaestio.org</string>`

`    <string name="website_url">https://quaestio.org</string>`

to:


`   <string name="website_domain">your.url</string>`

`   <string name="website_url">http://your.url</string>`

Or change the `loadURL`directly in [MainActivity.kt](https://github.com/QuaestioOrg/kotlin-converted-webview/blob/master/app/src/main/java/org/quaestio/kotlinconvertedwebview/MainActivity.kt) from:

`21        mWebView.loadUrl(getString(R.string.website_url))`

`30        if (Uri.parse(url).host == getString(R.string.website_domain)) {`

to:

`21        mWebView.loadUrl("http://your.url")`

`30        if (Uri.parse(url).host == "your.url") {`

And don't forget to edit the following lines in the [AndroidManifest.xml](https://github.com/QuaestioOrg/kotlin-converted-webview/blob/master/app/src/main/AndroidManifest.xml) file:

`                <data`

`                    android:host="quaestio.org"`

`                    android:scheme="https" />`

## Contributing
This sample is open to contributions; please, read [Contributing guidelines](https://github.com/QuaestioOrg/kotlin-converted-webview/blob/master/CONTRIBUTING.md) before opening new [issues](https://github.com/QuaestioOrg/kotlin-converted-webview/issues) or submitting [pull requests](https://github.com/QuaestioOrg/kotlin-converted-webview/pulls) to this repository.

## Credits
A live demo can be seen from [Quaestio's web app](https://e5kmd.app.goo.gl/zvpW) which loads similar **Android Kotlin WebView** pieces of code.

A special thanks to [Vamsi Tallapudi](https://github.com/vamsitallapudi/create-android-app-for-website)'s [Android Java WebView sample](https://github.com/vamsitallapudi/create-android-app-for-website) and [CodeRefer's tutorials](https://www.coderefer.com/create-android-app-for-website/) for the introductory lessons they provided in the past.

## Screenshots

![](/screenshots/1_hires.png) ![](/screenshots/2_hires.png)

## License
Licensed under the [Apache License, Version 2.0 (the "License")](http://www.apache.org/licenses/LICENSE-2.0); you may not use files of this sample except in compliance with its [License](https://github.com/QuaestioOrg/kotlin-converted-webview/blob/master/LICENSE).

Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an "as is" basis, without warranties or conditions of any kind, either express or implied.

See the License for the specific language governing permissions and limitations under the License.
