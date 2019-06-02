Using bazel 0.26

```
[guillaume@paddle:~/bazel_non_repro_override_repo]$ bazel build //...
Starting local Bazel server and connecting to it...
DEBUG: /home/guillaume/.cache/bazel/_bazel_guillaume/5b3d64037925a138f9475c1e032758a5/external/foo/bar.bzl:2:5: I'm in a gist
INFO: Analyzed 0 targets (1 packages loaded, 0 targets configured).
INFO: Found 0 targets...
INFO: Elapsed time: 4.483s, Critical Path: 0.02s
INFO: 0 processes.
INFO: Build completed successfully, 1 total action

[guillaume@paddle:~/bazel_non_repro_override_repo]$ bazel build @foo//... --override_repository=foo=/home/guillaume/bazel_non_repro_override_repo/foo_alt
DEBUG: /home/guillaume/.cache/bazel/_bazel_guillaume/5b3d64037925a138f9475c1e032758a5/external/foo/bar.bzl:2:5: hello
INFO: Analyzed 0 targets (1 packages loaded, 0 targets configured).
INFO: Found 0 targets...
INFO: Elapsed time: 0.347s, Critical Path: 0.00s
INFO: 0 processes.
INFO: Build completed successfully, 1 total action

[guillaume@paddle:~/bazel_non_repro_override_repo]$ bazel build //...
DEBUG: /home/guillaume/.cache/bazel/_bazel_guillaume/5b3d64037925a138f9475c1e032758a5/external/foo/bar.bzl:2:5: hello
INFO: Analyzed 0 targets (1 packages loaded, 0 targets configured).
INFO: Found 0 targets...
INFO: Elapsed time: 0.138s, Critical Path: 0.00s
INFO: 0 processes.
INFO: Build completed successfully, 1 total action

[guillaume@paddle:~/bazel_non_repro_override_repo]$ bazel clean --expunge
INFO: Starting clean (this may take a while). Consider using --async if the clean takes more than several minutes.

[guillaume@paddle:~/bazel_non_repro_override_repo]$ bazel build //...
Starting local Bazel server and connecting to it...
DEBUG: /home/guillaume/.cache/bazel/_bazel_guillaume/5b3d64037925a138f9475c1e032758a5/external/foo/bar.bzl:2:5: I'm in a gist
INFO: Analyzed 0 targets (1 packages loaded, 0 targets configured).
INFO: Found 0 targets...
INFO: Elapsed time: 2.052s, Critical Path: 0.02s
INFO: 0 processes.
INFO: Build completed successfully, 1 total action
```
