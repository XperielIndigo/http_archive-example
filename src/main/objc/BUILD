objc_library(
        name = "objc",
        srcs = glob(["*.m"]),
        hdrs = glob(["*.h"]),
        includes = ["."],
        visibility = ["//visibility:public"],
        deps = [
             "//external:example",
# Uncommenting the following line shows that the example lib does work when stored locally.
#              "//example_lib:example",
        ],
)