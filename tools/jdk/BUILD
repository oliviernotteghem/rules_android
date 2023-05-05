load("@bazel_tools//tools/jdk:default_java_toolchain.bzl", "BASE_JDK9_JVM_OPTS", "default_java_toolchain")

# Setup default javacopts such as for errorprone without affecting external repos.
default_java_toolchain(
    name = "toolchain_android_only",
    bootclasspath = [
        "//tools/android:android_jar",
        # TODO(b/175805830): Add this only when desugaring is enabled.
        "@bazel_tools//tools/android:desugar_java8_extra_bootclasspath",
    ],
    #    javac = ["//tools/error-prone:javac"],
    java_runtime = "@lyft_jdk11//:jdk",
    jvm_opts = BASE_JDK9_JVM_OPTS + ["-XX:-MaxFDLimit"],
    package_configuration = ["@//:error_prone"],
    source_version = "1.8",
    target_version = "1.8",
    visibility = ["//visibility:public"],
)

alias(
    name = "toolchain",
    actual = "@bazel_tools//tools/jdk:toolchain",
    visibility = ["//visibility:public"],
)

alias(
    name = "current_java_runtime",
    actual = "@bazel_tools//tools/jdk:current_java_runtime",
    visibility = ["//visibility:public"],
)

alias(
    name = "current_java_toolchain",
    actual = "@bazel_tools//tools/jdk:current_java_toolchain",
    visibility = ["//visibility:public"],
)

alias(
    name = "jdk",
    actual = "@bazel_tools//tools/jdk:jdk",
    visibility = ["//visibility:public"],
)

alias(
    name = "current_host_java_runtime",
    actual = "@bazel_tools//tools/jdk:current_host_java_runtime",
    visibility = ["//visibility:public"],
)
