package(default_visibility = ["//visibility:public"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_library",
    "go_test",
)

go_library(
    name = "go_default_library",
    srcs = [
        "mustmatchpatterns.go",
        "types.go",
    ],
    importpath = "k8s.io/kubernetes/pkg/security/podsecuritypolicy/sysctl",
    deps = [
        "//pkg/api:go_default_library",
        "//pkg/api/helper:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/util/validation/field:go_default_library",
    ],
)

go_test(
    name = "go_default_test",
    srcs = ["mustmatchpatterns_test.go"],
    importpath = "k8s.io/kubernetes/pkg/security/podsecuritypolicy/sysctl",
    library = ":go_default_library",
    deps = [
        "//pkg/api:go_default_library",
        "//pkg/api/helper:go_default_library",
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
