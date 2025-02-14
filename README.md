# AIDL Example

This is a basic example of the Android Interface Definition Language, a component of the Android framework
that allows to separate apps (processes) to communicate with each other using a "contract" (interface).

![Screenshot](https://raw.githubusercontent.com/afollestad/aidl-example/master/art/screenshot1.png)

### Using this example

To observe this example project work, you must first install the `receiver` module on your device
(it doesn't show any UI, it's just a `Service`). Once it's installed, install and run the `app` module
on your device. The `app` module will display UI that starts the service, binds with the service,
and uses methods declared in the service.

Note it also tells you how long it took to receive the entire response from the Service, AIDL is *very* fast
compared to other forms of IPC.

### Building with Bazel

Download bazel 0.4.5 or later from https://github.com/bazelbuild/bazel/releases.
You can then build the two APKs like this:

```
$ bazel build //app/src/main:app //receiver/src/main:service
INFO: Found 2 targets...
INFO: Elapsed time: 10.656s, Critical Path: 9.00s

$ adb install bazel-bin/receiver/src/main/service.apk
bazel-bin/receiver/src/main/service.apk: 1 file pushed. 0.7 MB/s (25933 bytes in 0.033s)
        pkg: /data/local/tmp/service.apk
Success

$ adb install bazel-bin/app/src/main/app.apk
bazel-bin/app/src/main/app.apk: 1 file pushed. 1.7 MB/s (1083460 bytes in 0.603s)
        pkg: /data/local/tmp/app.apk
Success
```
