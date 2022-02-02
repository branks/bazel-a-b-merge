load("@npm//@bazel/rollup:index.bzl", "rollup_bundle")

configs = [{
  "name": "a",
  "srcs": ['a/a.js'],
  "entry_point": "a/a.js",
}, {
  "name": "b",
  "srcs": ['b/b.js'],
  "entry_point": "b/b.js",
}]

[
  rollup_bundle(
    name = "build/" + config.get("name") + "/built",
    srcs = config.get("srcs"),
    entry_point = config.get("entry_point"),
    config_file = "//config/rollup:rollup.config.js",
    deps = [
      "@npm//@babel/core",
      "@npm//@babel/preset-typescript",
      "@npm//rollup",
      "@npm//@bazel/rollup",
      "@npm//@rollup/plugin-babel",
      "@npm//@rollup/plugin-commonjs"
    ],
    format = "system",
    sourcemap = "false",
  )
   for config in configs
]
