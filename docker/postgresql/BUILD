load(
  "@bazel_tools//tools/build_defs/docker:docker.bzl",
  "docker_build",
)

docker_build(
    name = "latest",
    repository = "plato",
    base = "@official_postgresql//image:image.tar",
    legacy_repository_naming = True,
)
