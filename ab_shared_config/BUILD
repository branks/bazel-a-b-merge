load("@npm//@bazel/rollup:index.bzl", "rollup_bundle")

rollup_bundle(
  name = "build",
  srcs = glob(['a/**/*.js', 'b/**/*.js']),
  entry_points = {
    "a/index.js": "a/built",
    "b/index.js": "b/built",
  },
  output_dir = True,
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
