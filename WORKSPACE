load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

http_archive(
    name = "foo",
    sha256 = "ea7f90ceacf13c1b92e5d87feb6c95b343ae7355ff6ee632faaa3d0df024e04b",
    urls = ["https://gist.github.com/guibou/8e2946aab523125c634ee124f716753b/archive/f086326dced340e78fc549b92fb72b9142b82c46.zip"],
    strip_prefix = "8e2946aab523125c634ee124f716753b-f086326dced340e78fc549b92fb72b9142b82c46",
)

load("@foo//:bar.bzl", "biz")

biz()
