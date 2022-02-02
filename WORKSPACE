load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

#########
# Node js
#########
http_archive(
    name = "build_bazel_rules_nodejs",
    sha256 = "f690430f4d4cc403b5c90d0f0b21842183b56b732fff96cfe6555fe73189906a",
    urls = ["https://github.com/bazelbuild/rules_nodejs/releases/download/5.0.1/rules_nodejs-5.0.1.tar.gz"],
)

load("@build_bazel_rules_nodejs//:repositories.bzl", "build_bazel_rules_nodejs_dependencies")
build_bazel_rules_nodejs_dependencies()

load("@build_bazel_rules_nodejs//:index.bzl", "yarn_install", "node_repositories")
node_repositories(
  yarn_version = "1.5.1",
  node_version = "16.13.2",
)
yarn_install(
  name = "npm",
  exports_directories_only = True,
  package_json = "//:package.json",
  yarn_lock = "//:yarn.lock",
)
