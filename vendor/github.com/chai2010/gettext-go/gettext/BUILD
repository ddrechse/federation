load("@io_bazel_rules_go//go:def.bzl", "go_library", "go_test")

go_library(
    name = "go_default_library",
    srcs = [
        "caller.go",
        "doc.go",
        "domain.go",
        "domain_helper.go",
        "fs.go",
        "gettext.go",
        "local.go",
        "tr.go",
    ],
    importpath = "github.com/chai2010/gettext-go/gettext",
    visibility = ["//visibility:public"],
    deps = [
        "//vendor/github.com/chai2010/gettext-go/gettext/mo:go_default_library",
        "//vendor/github.com/chai2010/gettext-go/gettext/plural:go_default_library",
        "//vendor/github.com/chai2010/gettext-go/gettext/po:go_default_library",
    ],
)

go_test(
    name = "go_default_test",
    srcs = [
        "caller_test.go",
        "gettext_test.go",
        "testdata_test.go",
        "tr_test.go",
    ],
    importpath = "github.com/chai2010/gettext-go/gettext",
    library = ":go_default_library",
    deps = [
        "//vendor/github.com/chai2010/gettext-go/gettext/mo:go_default_library",
        "//vendor/github.com/chai2010/gettext-go/gettext/po:go_default_library",
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
    srcs = [
        ":package-srcs",
        "//vendor/github.com/chai2010/gettext-go/gettext/mo:all-srcs",
        "//vendor/github.com/chai2010/gettext-go/gettext/plural:all-srcs",
        "//vendor/github.com/chai2010/gettext-go/gettext/po:all-srcs",
    ],
    tags = ["automanaged"],
    visibility = ["//visibility:public"],
)
