load("@rules_java//java:defs.bzl", "java_library")
load("//scala:scala.bzl", "scala_export_to_java", "scala_library")

scala_library(
    name = "a",
    srcs = ["A.scala"],
)

scala_export_to_java(
    name = "b",
    exports = [":a"],
    runtime_deps = [],
)

java_library(
    name = "c",
    srcs = ["C.java"],
    deps = [":b"],
)

java_library(
    name = "d",
    srcs = ["D.java"],
    tags = ["manual"],
    deps = [":c"],
)
