load("//empty:empty.bzl", "empty")

# Run 'bazel build :nothing'. The target will be successfully analyzed,
# but it does nothing.
empty(name = "nothing")

load("//attributes:printer.bzl", "printer")

# Run 'bazel build :some_target' to print its information.
printer(
    name = "some_target",
    deps = [
        "BUILD",
        ":other",
    ],
)

# This target is a dependency of 'some_target', so it is automatically analyzed
# when you build 'some_target'.
printer(name = "other")

