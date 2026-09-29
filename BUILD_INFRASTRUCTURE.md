# Build infrastructure

[ReMeizu/build-infra](https://github.com/ReMeizu/build-infra) contains manual,
resource-limited CI for kernel work. Its source/compiler pins, container recipe,
budget policy and tests are public. Android ROM jobs are not enabled there yet.

On 29 September 2026 the
[Blacksmith runner probe](https://github.com/ReMeizu/build-infra/actions/runs/36552629790)
and [M5s Yassy panel-object build](https://github.com/ReMeizu/build-infra/actions/runs/36553547835)
succeeded. The seven downloaded outputs were checked against their recorded
hashes. The AArch64 object and generated configuration matched the previous
successful build byte for byte.

This validates the small kernel-object workload on that runner. A complete
kernel, DTB, boot image and hardware behavior require their own tests. Job logs
and artifacts are available from the linked Actions runs; artifact retention is
seven days. Detailed historical validation records are retained privately.

For running a job and understanding its resource limits, see the
[build-infra usage guide](https://github.com/ReMeizu/build-infra#readme).
