```
➜ bazel build //docker/postgresql/...
ERROR: /Users/oleg/dev/docker_bazel_naming_problem/docker/postgresql/BUILD:6:1: no such target '@official_postgresql//image:image': target 'image' not declared in package 'image' defined by /private/var/tmp/_bazel_oleg/bb8329684d4f92473190c24d9fe97e93/external/official_postgresql/image/BUILD and referenced by '//docker/postgresql:latest'.
ERROR: Analysis of target '//docker/postgresql:latest' failed; build aborted.
INFO: Elapsed time: 0.076s
```
