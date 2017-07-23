```
➜ bazel run //docker/postgresql:latest my-fucking-postgresql:my-fucking-label
.............
WARNING: /private/var/tmp/_bazel_oleg/ec1e6f6b694cce258dcc2baca5d4adee/external/bazel_tools/tools/build_defs/docker/docker.bzl:19:1: The docker_{build,bundle} rules bundled with Bazel are deprecated in favor of:
https://github.com/bazelbuild/rules_docker. Please change BUILD loads to reference: @io_bazel_rules_docker//docker:docker.bzl and add the following to your WORKSPACE:
git_repository(
    name = "io_bazel_rules_docker",
    remote = "https://github.com/bazelbuild/rules_docker.git",
    commit = "...",
)
load("@io_bazel_rules_docker//docker:docker.bzl", "docker_repositories")
docker_repositories().
INFO: Found 1 target...
Target //docker/postgresql:latest up-to-date:
  bazel-bin/docker/postgresql/latest-layer.tar
INFO: Elapsed time: 5.174s, Critical Path: 0.11s

INFO: Running command line: bazel-bin/docker/postgresql/latest my-fucking-postgresql:my-fucking-label
Skipping 59a19ad159735c0c37ad883ea57112d21bbadeb3fc806f3a6e0ac10d33cdf926, already loaded.
Tagging 59a19ad159735c0c37ad883ea57112d21bbadeb3fc806f3a6e0ac10d33cdf926 as plato/docker_postgresql:latest

➜ docker images | grep docker_
plato/docker_postgresql   latest              59a19ad15973        292 years ago       36.9MB
```

What's wrong: I can not specify local docker image repository
For instance, how I can get name "plato/postgresql:latest" without changing the directory structure?
