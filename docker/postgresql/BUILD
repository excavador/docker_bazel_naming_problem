load(
  "@io_bazel_rules_docker//docker:docker.bzl",
  "docker_build",
)

docker_build(
    name = "latest",
    repository = "plato",
    base = "@official_postgresql//image",
    legacy_repository_naming = True,
)
