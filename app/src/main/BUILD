android_binary(
    name = "app",
    manifest = "AndroidManifest.xml",
    custom_package = "com.afollestad.aidlexample",
    srcs = [
        "java/com/afollestad/aidlexample/MainActivity.java",
    ],
    resource_files = glob(["res/**"]),
    deps = [
        ":lib",
        "@androidsdk//com.android.support:appcompat-v7-23.0.1",
    ],
)

android_library(
    name = "lib",
    srcs = [
        "java/com/afollestad/aidlexample/MainObject.java",
    ],
    idl_srcs = [
        "aidl/com/afollestad/aidlexample/IMainService.aidl",
    ],
    idl_parcelables = [
        "aidl/com/afollestad/aidlexample/MainObject.aidl",
    ],
    idl_import_root = "aidl",
)
