# Copyright 2023 Uber Technologies, Inc.
# Licensed under the MIT License

load("@bazel_gazelle//:def.bzl", "gazelle")

# gazelle:build_file_name BUILD
# gazelle:prefix github.com/uber/hermetic_cc_toolchain
# gazelle:exclude tools.go

gazelle(name = "gazelle")

gazelle(
    name = "gazelle-update-repos",
    args = [
        "-from_file=go.mod",
        "-to_macro=repositories.bzl%go_repositories",
        "-prune",
    ],
    command = "update-repos",
)
