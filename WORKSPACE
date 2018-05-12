git_repository(
    name = "io_bazel_rules_go",
    remote = "https://github.com/bazelbuild/rules_go.git",
    commit = "a390e7f7eac912f6e67dc54acf67aa974d05f9c3",
)
load("@io_bazel_rules_go//go:def.bzl", "go_rules_dependencies", "go_register_toolchains")

go_rules_dependencies()
go_register_toolchains()

load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

http_archive(
    name = "io_bazel_rules_docker",
    sha256 = "6dede2c65ce86289969b907f343a1382d33c14fbce5e30dd17bb59bb55bb6593",
    strip_prefix = "rules_docker-0.4.0",
    urls = ["https://github.com/bazelbuild/rules_docker/archive/v0.4.0.tar.gz"],
)

load(
    "@io_bazel_rules_docker//go:image.bzl",
    _go_image_repos = "repositories",
)

_go_image_repos()
