load("//apple:ios.bzl", "ios_unit_test")

licenses(["notice"])

objc_library(
    name = "SquarerLib",
    srcs = ["Sources/Squarer.m"],
    hdrs = ["Sources/Squarer.h"],
)

objc_library(
    name = "SquarerTestsLib",
    srcs = ["Tests/SquarerTests.m"],
    deps = [":SquarerLib"],
)

ios_unit_test(
    name = "SquarerTests",
    env = {"TEST_ENV_VAR": "test_value"},
    minimum_os_version = "9.0",
    deps = [":SquarerTestsLib"],
)

ios_unit_test(
    name = "SquarerTestsOrdered",
    env = {"TEST_ENV_VAR": "test_value"},
    minimum_os_version = "9.0",
    runner = "@build_bazel_rules_apple//apple/testing/default_runner:ios_xctestrun_ordered_runner",
    deps = [":SquarerTestsLib"],
)

ios_unit_test(
    name = "SquarerTestsRandom",
    env = {"TEST_ENV_VAR": "test_value"},
    minimum_os_version = "9.0",
    runner = "@build_bazel_rules_apple//apple/testing/default_runner:ios_xctestrun_random_runner",
    deps = [":SquarerTestsLib"],
)
