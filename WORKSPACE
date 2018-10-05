load("@bazel_tools//tools/build_defs/repo:git.bzl", "new_git_repository")
git_repository(
  name = "com_github_nelhage_rules_boost",
  commit = "8a8853fd755496288995a603ce9aa2685709cd39",
  remote = "https://github.com/nelhage/rules_boost",
)

load("@com_github_nelhage_rules_boost//:boost/boost.bzl", "boost_deps")
boost_deps()

RAPIDJSON_BUILD = """
cc_library(
  name = "rapidjson",
  hdrs = glob(["include/rapidjson/**/*.h"]),
  includes = ["include"],
  visibility = ["//visibility:public"],
)
"""
new_git_repository(
  name = "rapidjson",
  build_file_content = RAPIDJSON_BUILD,
  remote = "https://github.com/Tencent/rapidjson.git",
  tag = "v1.1.0",
)

SOCKETIO_BUILD = """
cc_library(
  name = "websocketpp",
  hdrs = glob(["websocketpp/**/*.hpp"]),
  visibility = ["//visibility:public"],
  includes = ["."],
  copts = ["-Iexternal/websocketcpp"]
)
"""
new_git_repository(
  name = "websocketpp",
  build_file_content = SOCKETIO_BUILD,
  remote = "https://github.com/zaphoyd/websocketpp.git",
  tag = "0.8.1",
)