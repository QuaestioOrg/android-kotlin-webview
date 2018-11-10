# Android Kotlin WebView

[![API](https://img.shields.io/badge/API-19%2B-brightgreen.svg?style=flat)](https://android-arsenal.com/api?level=19)

## Description
An [Android WebView](https://d.android.com/guide/webapps/webview) simply converted from [Java](https://www.java.com/) to [Kotlin](https://kotlinlang.org/) using the basic [Android Studio tool](https://developer.android.com/studio/projects/add-kotlin#convert-to-kotlin-code).

## Table of Contents
* [Installation](#installation)
* [Usage](#usage)
* [Contributing](#contributing)
* [Credits](#credits)
* [Screenshots](#screenshots)
* [License](#license)

## Installation
1. Clone the project;
2. unzip the folder;
3. run [Android Studio](https://d.android.com/studio/);
4. open a new project;
5. and pick the package.

## Usage
Change the URL indirectly from [strings.xml](/app/src/main/res/values/strings.xml) from:

`   <string name="website_domain">quaestio.org</string>`

`    <string name="website_url">https://quaestio.org</string>`

to:


`   <string name="website_domain">your.url</string>`

`   <string name="website_url">http://your.url</string>`

Or change the `loadURL`directly in [MainActivity.kt](/app/src/main/java/org/quaestio/kotlinconvertedwebview/MainActivity.kt) from:

`21        mWebView.loadUrl(getString(R.string.website_url))`

`30        if (Uri.parse(url).host == getString(R.string.website_domain)) {`

to:

`21        mWebView.loadUrl("http://your.url")`

`30        if (Uri.parse(url).host == "your.url") {`

And don't forget to edit the following lines in the [AndroidManifest.xml](/app/src/main/AndroidManifest.xml) file:

`                <data`

`                    android:host="quaestio.org"`

`                    android:scheme="https" />`

## Contributing
This sample is open to contributions; please, read [Contributing guidelines](/CONTRIBUTING.md) before opening new [issues](https://github.com/QuaestioOrg/kotlin-converted-webview/issues) or submitting [pull requests](https://github.com/QuaestioOrg/kotlin-converted-webview/pulls) to this repository.

## Credits
A live demo can be seen from [Quaestio's web app](https://e5kmd.app.goo.gl/zvpW) which loads similar **Android Kotlin WebView** pieces of code.

A special thanks to [Vamsi Tallapudi](https://github.com/vamsitallapudi)'s [Android Java WebView sample](https://github.com/vamsitallapudi/create-android-app-for-website) and [CodeRefer's tutorials](https://www.coderefer.com/create-android-app-for-website/) for the introductory lessons they provided in the past.



## Screenshots
![](/screenshots/1_hires.png) ![](/screenshots/2_hires.png)

## License
Licensed under the [Apache License, Version 2.0 (the "License")](http://www.apache.org/licenses/LICENSE-2.0); you may not use files of this sample except in compliance with its [License](/LICENSE).

Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an "as is" basis, without warranties or conditions of any kind, either express or implied.

See the License for the specific language governing permissions and limitations under the License.
