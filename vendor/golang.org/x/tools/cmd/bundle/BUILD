load("@io_bazel_rules_go//go:def.bzl", "go_binary", "go_library", "go_test")

go_library(
    name = "go_default_library",
    srcs = ["main.go"],
    importpath = "golang.org/x/tools/cmd/bundle",
    visibility = ["//visibility:private"],
    deps = ["//vendor/golang.org/x/tools/go/loader:go_default_library"],
)

go_binary(
    name = "bundle",
    importpath = "golang.org/x/tools/cmd/bundle",
    library = ":go_default_library",
    visibility = ["//visibility:public"],
)

go_test(
    name = "go_default_test",
    srcs = ["main_test.go"],
    importpath = "golang.org/x/tools/cmd/bundle",
    library = ":go_default_library",
    deps = ["//vendor/golang.org/x/tools/go/buildutil:go_default_library"],
)

filegroup(
    name = "package-srcs",
    srcs = glob(["**"]),
    tags = ["automanaged"],
    visibility = ["//visibility:private"],
)

filegroup(
    name = "all-srcs",
    srcs = [
        ":package-srcs",
        "//vendor/golang.org/x/tools/cmd/bundle/testdata/src/domain.name/importdecl:all-srcs",
        "//vendor/golang.org/x/tools/cmd/bundle/testdata/src/initial:all-srcs",
    ],
    tags = ["automanaged"],
    visibility = ["//visibility:public"],
)
