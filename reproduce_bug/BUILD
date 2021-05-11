load("@rules_python//python:defs.bzl", "py_binary", "py_test")
load("@pypi//:requirements.bzl", "requirement")

py_binary(
    name = "main",
    srcs = ["main.py"],
    deps = [
        requirement("ciso8601"),
    ],
)
