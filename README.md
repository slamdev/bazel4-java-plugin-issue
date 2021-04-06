# bazel4-java-plugin-issue

Showcase for the issue with [lombok](https://projectlombok.org/) used in [java_plugin](https://docs.bazel.build/versions/master/be/java.html#java_plugin)

Issue link: https://github.com/bazelbuild/bazel/issues/13305

To reproduce:

```shell script
git clone git@github.com:slamdev/bazel4-java-plugin-issue.git
cd bazel4-java-plugin-issue
./baseliskw build //lib_b:lib_b
```

Downgrade bazel version to get the build working:

```shell script
echo 3.7.2 > .bazelversion
./baseliskw build //lib_b:lib_b
```

Check [CI pipeline](https://github.com/slamdev/bazel4-java-plugin-issue/actions/workflows/build.yaml) that runs the code
with different OS, bazel and java versions.
