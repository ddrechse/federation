load("@io_bazel_rules_go//go:def.bzl", "go_library")

go_library(
    name = "go_default_library",
    srcs = [
        "fixtures.go",
        "storage.go",
    ],
    importpath = "github.com/docker/docker/integration-cli/cli/build/fakestorage",
    visibility = ["//visibility:public"],
    deps = [
        "//vendor/github.com/docker/docker/integration-cli/cli:go_default_library",
        "//vendor/github.com/docker/docker/integration-cli/cli/build:go_default_library",
        "//vendor/github.com/docker/docker/integration-cli/cli/build/fakecontext:go_default_library",
        "//vendor/github.com/docker/docker/integration-cli/environment:go_default_library",
        "//vendor/github.com/docker/docker/integration-cli/request:go_default_library",
        "//vendor/github.com/docker/docker/pkg/stringutils:go_default_library",
    ],
)

filegroup(
    name = "package-srcs",
    srcs = glob(["**"]),
    tags = ["automanaged"],
    visibility = ["//visibility:private"],
)

filegroup(
    name = "all-srcs",
    srcs = [":package-srcs"],
    tags = ["automanaged"],
    visibility = ["//visibility:public"],
)
