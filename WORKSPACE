workspace(name = "rules_python_demo")

load("@bazel_tools//tools/build_defs/repo:git.bzl", "git_repository")
load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")
load("@bazel_tools//tools/build_defs/repo:git.bzl", "new_git_repository")

#rules_python_version = "0.2.0"  # broken
rules_python_version = "c361e789a246c81649dc8d9700d29b8a32a3d00f" # Fixes issue

http_archive(
    name = "rules_python",
#    url = "https://github.com/bazelbuild/rules_python/releases/download/{version}/rules_python-{version}.tar.gz".format(version = rules_python_version),
    url = "https://github.com/bazelbuild/rules_python/archive/{version}.tar.gz".format(version = rules_python_version),
    strip_prefix = "rules_python-{version}".format(version = rules_python_version),
    
    sha256 = "",
)

load("@rules_python//python:pip.bzl", "pip_install")

pip_install(
   name = "pypi",
   requirements = "//:requirements.txt",
)

