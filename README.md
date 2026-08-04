# Zephyr Project (zephyr)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

The Zephyr Project is a Linux Foundation project that delivers a small, scalable, secure, and open-source real-time operating system (RTOS) for resource-constrained embedded devices. Zephyr supports 1000+ boards across ARM Cortex, RISC-V, ARC, x86, Xtensa, and other architectures, ships with a C kernel, device drivers, networking stacks (BLE, Wi-Fi, Thread, Matter), security subsystems, and is supported by a meta-tool (west), an SDK (sdk-ng), and a broad ecosystem of training partners and commercial silicon and module vendors.

**URL:** [Visit APIs.json URL](https://raw.githubusercontent.com/api-evangelist/zephyr/refs/heads/main/apis.yml)

## Scope

- **Type:** Index
- **Position:** Consumer
- **Access:** 3rd-Party

## Tags

- Embedded, IoT, Linux Foundation, RTOS, Open Source, Edge

## Timestamps

- **Created:** 2026-03-16
- **Modified:** 2026-05-03

## APIs

### Zephyr RTOS Kernel API

The Zephyr kernel C API exposes scheduling, threading, synchronization, memory management, and timer services for real-time embedded applications.

**Human URL:** [https://docs.zephyrproject.org/latest/kernel/index.html](https://docs.zephyrproject.org/latest/kernel/index.html)

#### Properties

- [Documentation](https://docs.zephyrproject.org/latest/kernel/index.html)
- [APIReference](https://docs.zephyrproject.org/apidoc/latest/index.html)
- [GettingStarted](https://docs.zephyrproject.org/latest/develop/getting_started/index.html)
- [GitHubRepository](https://github.com/zephyrproject-rtos/zephyr)

### Zephyr Device Driver API

The Zephyr device driver subsystem exposes a uniform device model across GPIO, I2C, SPI, UART, ADC, sensors, displays, networking, USB, Bluetooth, and many other peripheral classes, configured through Devicetree and Kconfig.

**Human URL:** [https://docs.zephyrproject.org/latest/build/dts/index.html](https://docs.zephyrproject.org/latest/build/dts/index.html)

#### Properties

- [Documentation](https://docs.zephyrproject.org/latest/hardware/index.html)
- [APIReference](https://docs.zephyrproject.org/apidoc/latest/group__io__interfaces.html)

### Zephyr Networking API

The Zephyr networking stack exposes BSD-like sockets, TLS/DTLS, MQTT, CoAP, LWM2M, HTTP, WebSocket, gRPC, and connectivity layers including IPv4/IPv6, Wi-Fi, Thread, OpenThread, Matter, and BLE.

**Human URL:** [https://docs.zephyrproject.org/latest/connectivity/networking/index.html](https://docs.zephyrproject.org/latest/connectivity/networking/index.html)

#### Properties

- [Documentation](https://docs.zephyrproject.org/latest/connectivity/networking/index.html)

## Common Properties

- [Portal](https://www.zephyrproject.org/)
- [Documentation](https://docs.zephyrproject.org/latest/)
- [APIReference](https://docs.zephyrproject.org/apidoc/latest/index.html)
- [GettingStarted](https://docs.zephyrproject.org/latest/develop/getting_started/index.html)
- [GitHubOrganization](https://github.com/zephyrproject-rtos)
- [GitHubRepository](https://github.com/zephyrproject-rtos/zephyr)
- [SDK (sdk-ng)](https://github.com/zephyrproject-rtos/sdk-ng)
- [CLI (west)](https://github.com/zephyrproject-rtos/west)
- [Blog](https://www.zephyrproject.org/blog/)
- [ReleaseNotes](https://docs.zephyrproject.org/latest/releases/index.html)
- [Training](https://www.zephyrproject.org/training-partner-program/)
- [Events](https://www.zephyrproject.org/events/)
- [Compliance / Security](https://docs.zephyrproject.org/latest/security/index.html)
- [TermsOfService](https://www.linuxfoundation.org/terms)
- [PrivacyPolicy](https://www.linuxfoundation.org/privacy-policy/)
- [JSON-LD Context](json-ld/zephyr-context.jsonld)
- [Vocabulary](vocabulary/zephyr-vocabulary.yml)
- [Capability: Build and Flash](capabilities/zephyr-build.yaml)

## Maintainers

**FN:** Kin Lane

**Email:** info@apievangelist.com
