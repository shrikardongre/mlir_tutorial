# The "tools" directory contains binary targets that expose the public API of
# the passes in the project.

# We name the tool `tutorial-opt` following the pattern of `mlir-opt`.
package(
    default_visibility = ["//visibility:public"],
)
cc_binary(
    name = "tutorial-opt",
    srcs = ["tutorial-opt.cpp"],
    includes = ["include"],
    deps = [
        "//lib/Transform/Affine:AffineFullUnroll",
        "//lib/Dialect/Poly",
        "//lib/Transform/Arith:MulToAdd",
        "@llvm-project//mlir:AllPassesAndDialects",
        "@llvm-project//mlir:MlirOptLib",
        "@llvm-project//mlir:Pass",
    ],
)