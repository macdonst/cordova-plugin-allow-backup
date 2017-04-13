# cordova-plugin-allow-backup
To allow you to set the allowBackup property of a cordova-android application

## Installation

By default adding this plugin to your cordova-android project will set the `android:allowBackup` property in the `<application/>` tag to `false`.

```
cordova plugin add cordova-plugin-allow-backup
```

If you want to set the property to `true` use the `BACKUP` environment value.

```
cordova plugin add cordova-plugin-allow-backup --variable BACKUP=true
```
