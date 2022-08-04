load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

android_sdk_repository(
    name = "androidsdk",
    path = "/private/var/tmp/_bazel_dilpreets/fd1872a369e190eb61f80e8199447f5a/external/downloaded_android_sdk/android_sdk",
)

http_archive(
    name = "robolectric",
    sha256 = "95d61d6b94bd19b0d528e47a5c1e482f2b2c914438028e9465b7ebd026013672",
    strip_prefix = "robolectric-bazel-4.8.1",
    urls = ["https://github.com/robolectric/robolectric-bazel/archive/4.8.1.tar.gz"],
)

load("@robolectric//bazel:robolectric.bzl", "robolectric_repositories")

robolectric_repositories()

http_archive(
    name = "rules_jvm_external",
    strip_prefix = "rules_jvm_external-4.2",
    sha256 = "cd1a77b7b02e8e008439ca76fd34f5b07aecb8c752961f9640dea15e9e5ba1ca",
    url = "https://github.com/bazelbuild/rules_jvm_external/archive/4.2.zip",
)

load("@rules_jvm_external//:defs.bzl", "maven_install")

maven_install(
    artifacts = [
        "androidx.appcompat:appcompat:1.0.2",
        "androidx.annotation:annotation:1.1.0",
        "androidx.test.ext:junit:1.1.0",
        "org.robolectric:robolectric:4.8.1",
        "org.assertj:assertj-core:3.12.1",
    ],
    maven_install_json = "//:maven_install.json",
    repositories = [
        "https://maven.google.com",
        "https://repo1.maven.org/maven2",
    ],
)

load("@maven//:defs.bzl", "pinned_maven_install")

pinned_maven_install()
