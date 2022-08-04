# Sample bazel project showing lack of coverage support for android_local_test

To run this locally update the `path` for `android_sdk_repository` in WORKSPACE to your android sdk path and then run

```
bazel coverage //src/test:main_activity_test
```

This will throw an error saying: `android_local_test does not yet support coverage`

```
ERROR: /src/rules_jvm_external/examples/android_local_test/src/test/BUILD:1:19: in android_local_test rule //src/test:main_activity_test: android_local_test does not yet support coverage
ERROR: /src/rules_jvm_external/examples/android_local_test/src/test/BUILD:1:19: Analysis of target '//src/test:main_activity_test' failed
ERROR: Analysis of target '//src/test:main_activity_test' failed; build aborted:
FAILED: Build did NOT complete successfully

```

This project was copied from https://github.com/bazelbuild/rules_jvm_external/tree/master/examples/android_local_test