load("@npm//@bazel/rollup:index.bzl", "rollup_bundle")

rollup_bundle(
  name = "build/a/built",
  srcs = ['a/a.js'],
  entry_point = "a/index.js",
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


rollup_bundle(
  name = "build/b/built",
  srcs = ['b/b.js'],
  entry_point = "b/index.js",
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



# rollup_bundle(
#   name = "build",
#   srcs = [],
#   entry_points = {
#     "a/index.js": "a/built",
#     "b/index.js": "b/built",
#   },
#   output_dir = True,
#   config_file = "//config/rollup:rollup.config.js",
#   deps = [
#     "@npm//@babel/core",
#     "@npm//@babel/preset-typescript",
#     "@npm//rollup",
#     "@npm//@bazel/rollup",
#     "@npm//@rollup/plugin-babel",
#     "@npm//@rollup/plugin-commonjs"
#   ],
#   format = "system",
#   sourcemap = "false",
# )
