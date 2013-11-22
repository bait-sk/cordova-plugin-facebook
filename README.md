Facebook plugin
=======================


This plugin is mainly a fork of @phonegap/phonegap-facebook-plugin and it is accomodated for Phonegap >=3.0, and cleaned up a little bit, and accomodated for our needs. So it is not official, and we cannot guarantee it will work properly for your needs. It does not include Facebook SDK. Supports Android and iOS.

INSTALLATION GUIDE
------------------

**ANDROID**

First you will need [Facebook SDK](https://developers.facebook.com/docs/getting-started/facebook-sdk-for-android/3.0/)
Then you need to include the SDK into your Ant build: edit your `local.properties` file and add `android.library.reference.1=../relative/path/to/facebook-android-sdk-3.5.2/facebook/`

Then add the plugin to your phonegap project:
`phonegap local plugin add https://github.com/bait-sk/cordova-plugin-facebook.git`

**iOS**

tbc


EXAMPLE OF USAGE
----------------

Initialize plugin upon `deviceready` event, replace `1234567890123456789` with your facebook app id.

```javascript
document.addEventListener('deviceready', function() {
    try {
        alert('Device is ready! Make sure you set your app_id below this alert.');
        FB.init({ appId: "1234567890123456789", nativeInterface: CDV.FB, useCachedDialogs: false });
        document.getElementById('data').innerHTML = "";
    } catch (e) {
        alert(e);
    }
}, false);
```