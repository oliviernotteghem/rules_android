load("@rules_android//android:rules.bzl", "android_binary", "android_library")

android_library(
    name = "other_lib",
    srcs = ["BasicLib.java"],
    manifest = "AndroidManifest.xml",
    custom_package = "com.basicapp",
    resource_files = glob(["res/**"]),
    visibility = ["//visibility:public"],
)
