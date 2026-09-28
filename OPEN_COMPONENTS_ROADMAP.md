# Open-component roadmap

This is a development plan, not a report of completed replacements. It covers
the same 17-board registry as the ReMeizu project: M2 Mini, M5c, M2 Note, M5s,
M1 Note, M3, M3s, M5, M5 Note, M6, M6T, U10, U20, M3 Note M681/L681, MX6 and
M6 Note M1721. New boards enter the plan after hardware identity is established.

## Work in useful increments

| Area | First useful result | Later work |
|---|---|---|
| Dependency inventory | Hashed, classified components with consumers, ABI and known source alternatives | Coverage of all selected images and board revisions |
| Lights, vibration and power | Small source-built HALs with observable hardware behavior | Power/thermal and suspend regression tests |
| Sensors and touch | Open host drivers, accurate events and a thin HAL | Batching, wakeup, fusion and controller-specific behavior |
| Audio | Open PCM playback/capture and documented routing | Call audio, effects, offload and quality validation |
| Graphics | Reuse DRM/Mesa support where hardware and API requirements match | Display integration, buffer/fence ownership, performance and power |
| Wi-Fi, Bluetooth, FM and GNSS | Open host transport/services with concrete connectivity tests | Coexistence, power management and advanced features |
| Telephony | Open host-side IPC/RIL with SIM/data tests | Voice, dual-SIM and IMS, tested as separate milestones |
| Camera | Sensor control and the first repeatable RAW/YUV capture | ISP processing, exposure/white balance/focus, tuning and Android HAL integration |
| Video codecs | Correct source-built playback/encode baseline | Hardware acceleration and associated power/latency validation |
| Other services and security interfaces | Documented interfaces and narrow open implementations | Board-specific capabilities and secure-world dependencies |
| Embedded firmware and boot software | A separate feasibility assessment per processor/boot path | Source-built implementations where technically achievable |
| Configuration and calibration | Documented formats and validated parsers/generators | Per-device data provenance and reproducible configuration |

A host driver, Android HAL and embedded firmware are separate components.
An open host implementation can still depend on closed firmware; that dependency
remains visible in the progress record. A wrapper around an existing binary is
useful compatibility work but does not count as replacing that binary.

The camera path has separate milestones: identify the exact sensor and rails;
obtain a real captured frame; implement processing and controls; expose the
Android/Linux interface; then assess image quality and sustained operation.
A source-built sensor driver alone does not establish a complete camera stack.

## Shared code with board-specific evidence

Common code follows verified hardware interfaces and ABI generations. Board
configuration retains exact regulators, pins, sensors, firmware requirements
and memory layout. MT6750 and MT6755 are related but not interchangeable.
Existing common/thin device work is the starting point; Qualcomm and MT6797
owners retain their separate device tracks.

The implementation path is: reuse suitable upstream code; document the required
interface; write a scoped openly licensed implementation; build it with pinned
tools; test behavior and failure cases; then validate on the intended hardware.
Larger components advance through independently useful milestones rather than
holding up every practical Android release.

## Acceptance

Each replacement records its source/license, target boards, ABI, remaining
firmware/data dependencies, build recipe, artifact identity and functional tests.
Progress states distinguish inventory, implementation, compilation and verified
hardware behavior. Acceptance requires the tested function to work without the
replaced original component, with regression coverage and known limitations.

CI can automate source checks, builds, evidence collection and failure triage.
Hardware acceptance also needs exact device/image identity, partition readback
where applicable, recovery and meaningful functional tests. Completing that
loop is part of the roadmap, not a capability claimed for the whole fleet today.

Upstream contributions should be small and reviewable: board descriptions,
driver fixes, tests and then postmarketOS device support. Completely replacing
all embedded firmware is an exploratory long-term objective, not a prerequisite
for the first useful releases.

Return to [project progress](PROJECT_STATUS.md) or the [source index](SOURCE_INDEX.md).
