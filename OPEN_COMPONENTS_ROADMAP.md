# Open-component roadmap

ReMeizu aims to replace closed host drivers and Android HALs with maintainable,
open implementations where practical. Upstream Linux and existing open projects
are the starting point. This is planned work; a complete open stack is not yet
available for these devices.

| Area | First milestone | Later work |
|---|---|---|
| Lights, vibration, sensors and touch | Small drivers/HALs with correct hardware behavior | Wakeup, batching and power management |
| Audio | PCM playback, recording and routing | Call audio, effects and low-power operation |
| Graphics | Suitable DRM/Mesa support and display output | Android buffer/fence integration, performance and power |
| Wi-Fi, Bluetooth, FM and GNSS | Working host transport and services | Coexistence, suspend and additional hardware features |
| Telephony | Host-side IPC/RIL, SIM and data | Voice, dual-SIM and IMS |
| Camera | Sensor control and repeatable RAW/YUV capture | ISP processing, exposure/focus, tuning and Android HAL integration |
| Video | Source-built playback and encode baseline | Hardware acceleration and power optimization |
| Power and charging | Verified board resources and battery limits | Thermal management, suspend and battery-life testing |
| Firmware and boot software | Identify interfaces and available source | Feasibility assessment per component |

An open host driver may still need closed firmware. Sensor control alone does
not provide a complete camera stack: processing, tuning and the application
interface must also work. Calibration data and secure-world dependencies need
separate treatment.

Shared code follows compatible hardware interfaces; board descriptions retain
actual pins, regulators, sensors and memory layouts. MT6750 and MT6755 are related
but are not interchangeable. MT6797 and Qualcomm devices keep separate ports.

Each implementation needs a clear license, reproducible build, functional tests
and validation on its target hardware. Small driver fixes and board descriptions
can reach upstream independently of larger camera or graphics work. Completely
replacing embedded firmware is a longer-term investigation, not a prerequisite
for useful Android releases.

[Device status](PROJECT_STATUS.md) · [Source repositories](SOURCE_INDEX.md)
