java_library(
    name = "lib_a",
    srcs = ["A.java"],
    plugins = [":lombok"],
    visibility = ["//visibility:public"],
    deps = ["@lombok//jar"],
)

java_plugin(
    name = "lombok",
    generates_api = True,
    processor_class = "lombok.launch.AnnotationProcessorHider$AnnotationProcessor",
    deps = ["@lombok//jar"],
)
