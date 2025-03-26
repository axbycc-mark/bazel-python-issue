load("@rules_python//python:pip.bzl", "compile_pip_requirements")
load("@rules_python//python:py_binary.bzl", "py_binary")

# This rule adds a convenient way to update the requirements file.
compile_pip_requirements(
    name = "requirements",
    src = "requirements.in",
    requirements_txt = "requirements.txt",
    requirements_windows = "requirements_windows.txt",
)

py_binary(
    name = "main",
    srcs = ["main.py"],
    deps = [
        "@pypi//ibis_framework:pkg",
    ],
)

