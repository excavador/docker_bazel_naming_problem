```
➜ bazel build //docker/postgresql/...
..............
WARNING: /private/var/tmp/_bazel_oleg/bb8329684d4f92473190c24d9fe97e93/external/bazel_tools/tools/build_defs/docker/docker.bzl:19:1: The docker_{build,bundle} rules bundled with Bazel are deprecated in favor of:
https://github.com/bazelbuild/rules_docker. Please change BUILD loads to reference: @io_bazel_rules_docker//docker:docker.bzl and add the following to your WORKSPACE:
git_repository(
    name = "io_bazel_rules_docker",
    remote = "https://github.com/bazelbuild/rules_docker.git",
    commit = "...",
)
load("@io_bazel_rules_docker//docker:docker.bzl", "docker_repositories")
docker_repositories().
ERROR: /Users/oleg/dev/docker_bazel_naming_problem/docker/postgresql/BUILD:6:1: no such target '@official_postgresql//image:image': target 'image' not declared in package 'image' defined by /private/var/tmp/_bazel_oleg/bb8329684d4f92473190c24d9fe97e93/external/official_postgresql/image/BUILD and referenced by '//docker/postgresql:latest'.
ERROR: Analysis of target '//docker/postgresql:latest' failed; build aborted.
INFO: Elapsed time: 21.241s
```
