package(default_visibility = ["//visibility:public"])

licenses(["notice"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_library",
    "go_test",
)

go_test(
    name = "go_default_test",
    srcs = [
        "mustrunas_test.go",
        "runasany_test.go",
    ],
    library = ":go_default_library",
    tags = ["automanaged"],
    deps = ["//pkg/api:go_default_library"],
)

go_library(
    name = "go_default_library",
    srcs = [
        "doc.go",
        "mustrunas.go",
        "runasany.go",
        "types.go",
    ],
    tags = ["automanaged"],
    deps = [
        "//pkg/api:go_default_library",
        "//vendor:k8s.io/apimachinery/pkg/util/validation/field",
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
)
