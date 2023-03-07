load(
    "@com_github_buildbuddy_io_rules_xcodeproj//xcodeproj:defs.bzl",
    "top_level_target",
    "xcodeproj",
)
load("@build_bazel_rules_swift//swift:swift.bzl",
    "swift_binary"
)

swift_binary(
    name = "binary",
    srcs = [
        "main.swift",
    ],
    deps = [
        "//srcs/module_a:module_a"
    ]
)

xcodeproj(
    name = "xcodeproj",
    project_name = "App",
    tags = ["manual"],
    top_level_targets = [
        ":binary"
    ],
)