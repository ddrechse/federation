load("@io_bazel_rules_go//go:def.bzl", "go_library")

go_library(
    name = "go_default_library",
    srcs = ["interface.go"],
    importpath = "github.com/aws/aws-sdk-go/service/elbv2/elbv2iface",
    visibility = ["//visibility:public"],
    deps = [
        "//vendor/github.com/aws/aws-sdk-go/aws/request:go_default_library",
        "//vendor/github.com/aws/aws-sdk-go/service/elbv2:go_default_library",
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
