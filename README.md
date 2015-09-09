This is just the sample of Android [Auto Backup](https://developer.android.com/preview/backup/index.html) bug.

## Process

```sh
$ ./gradlew installDebug
# Launch app, TextView shows sample.autobackup.SampleApplication
$ adb shell bmgr run
$ adb shell bmgr fullbackup sample.autobackup
# Uninstall app
$ ./gradlew installDebug
# Launch app, TextView shows android.app.Application during the first process
# From the second process, TextView shows sample.autobackup.SampleApplication
```