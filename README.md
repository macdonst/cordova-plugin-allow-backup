# cordova-plugin-allow-backup
To allow you to set the allowBackup property of a cordova-android application

## Config.xml

So I totally biffed on the fact that `edit-config` is now supported in `config.xml` as well as `plugin.xml` so you don't need the above plugin. All you need to do is add an edit-config section to your `config.xml` file like this:

```
<platform name="android">
    <edit-config file="AndroidManifest.xml"
                 target="/manifest/application"
                 mode="merge">
        <application android:allowBackup="false"/>
    </edit-config>
</platform>
```

## Installation

By default adding this plugin to your cordova-android project will set the `android:allowBackup` property in the `<application/>` tag to `false`.

```
cordova plugin add cordova-plugin-allow-backup
```

If you want to set the property to `true` use the `BACKUP` environment value.

```
cordova plugin add cordova-plugin-allow-backup --variable BACKUP=true
```
