load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

http_archive(
    name = "io_bazel_rules_go",
    sha256 = "08c3cd71857d58af3cda759112437d9e63339ac9c6e0042add43f4d94caf632d",
    urls = [
        "https://mirror.bazel.build/github.com/bazelbuild/rules_go/releases/download/v0.24.2/rules_go-v0.24.2.tar.gz",
        "https://github.com/bazelbuild/rules_go/releases/download/v0.24.2/rules_go-v0.24.2.tar.gz",
    ],
)

http_archive(
    name = "bazel_gazelle",
    sha256 = "d4113967ab451dd4d2d767c3ca5f927fec4b30f3b2c6f8135a2033b9c05a5687",
    urls = [
        "https://mirror.bazel.build/github.com/bazelbuild/bazel-gazelle/releases/download/v0.22.0/bazel-gazelle-v0.22.0.tar.gz",
        "https://github.com/bazelbuild/bazel-gazelle/releases/download/v0.22.0/bazel-gazelle-v0.22.0.tar.gz",
    ],
)

load("@io_bazel_rules_go//go:deps.bzl", "go_register_toolchains", "go_rules_dependencies")
load("@bazel_gazelle//:deps.bzl", "gazelle_dependencies", "go_repository")

go_rules_dependencies()

go_register_toolchains()

gazelle_dependencies()

go_repository(
    name = "com_github_mitchellh_go_homedir",
    commit = "af06845cf3004701891bf4fdb884bfe4920b3727",
    importpath = "github.com/mitchellh/go-homedir",
)

go_repository(
    name = "com_github_spf13_cobra",
    commit = "7f8e83d9366ab8e96959f9c3fbdf3507d4b39c3b",
    importpath = "github.com/spf13/cobra",
)

go_repository(
    name = "com_github_spf13_viper",
    commit = "d9d7dcdc6399b74695d0be0c5051bc4443c263c6",
    importpath = "github.com/spf13/viper",
)

go_repository(
    name = "com_github_hashicorp_hcl",
    commit = "d58017782ffeccb02d0f461c8710753e5da49834",
    importpath = "github.com/hashicorp/hcl",
)