android_binary(
    name = "service",
    manifest = "AndroidManifest.xml",
    srcs = [
        "java/com/afollestad/aidlexamplereceiver/MainService.java",
    ],
    resource_files = glob(["res/**"]),
    deps = [
        ":lib",
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
