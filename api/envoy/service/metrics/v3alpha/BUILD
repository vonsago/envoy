load("@envoy_api//bazel:api_build_system.bzl", "api_proto_library_internal", "api_proto_package")

licenses(["notice"])  # Apache 2

api_proto_package(
    has_services = True,
    deps = [
        "//envoy/api/v3alpha/core",
        "@prometheus_metrics_model//:client_model",
    ],
)

api_proto_library_internal(
    name = "metrics_service",
    srcs = ["metrics_service.proto"],
    has_services = 1,
    require_py = 0,
    deps = [
        "//envoy/api/v3alpha/core:base",
        "//envoy/api/v3alpha/core:grpc_service",
        "@prometheus_metrics_model//:client_model",
    ],
)
