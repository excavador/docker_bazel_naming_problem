```
➜ bazel run //docker/postgresql:latest
INFO: Found 1 target...
Target //docker/postgresql:latest up-to-date:
  bazel-bin/docker/postgresql/latest-layer.tar
INFO: Elapsed time: 32.635s, Critical Path: 6.79s

INFO: Running command line: bazel-bin/docker/postgresql/latest
Skipping 998347a1078e8c82bdb48503e172f5e27f203ca3532e6d2ecb0120064b2ebf8d, already loaded.
Loading 59a19ad159735c0c37ad883ea57112d21bbadeb3fc806f3a6e0ac10d33cdf926...
Loaded image: plato/docker/postgresql:latest
Tagging 59a19ad159735c0c37ad883ea57112d21bbadeb3fc806f3a6e0ac10d33cdf926 as plato/docker/postgresql:latest

➜ docker images | grep postgresql | grep docker
plato/docker/postgresql   latest              59a19ad15973        292 years ago       36.9MB
```

What's wrong: I can not specify local docker image repository
For instance, how I can get name "plato/postgresql:latest" without changing the directory structure?

