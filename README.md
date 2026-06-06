# Hi, I'm Gabriel 👋

Systems programmer focused on **C++ and Go** — performance engineering, scalable systems, data serialization, and high-throughput services. I like finding the bug nobody else can reproduce and the allocation nobody knew was there.

📍 Montreal

## Open Source Contributions

- **[Apache Avro](https://github.com/apache/avro/pull/3646)** (C++) — Fixed `BinaryDecoder::arrayNext()` mishandling negative block counts per the Avro spec, which corrupted stream position when decoding multi-block arrays (~20% decode failures on production messages). Root-caused, fixed, added regression tests, and resolved an undefined-behavior edge case when negating `INT64_MIN`. Merged into `apache/avro` main.
- **[haproxy-spoe-go](https://github.com/negasus/haproxy-spoe-go/pull/28)** (Go) — Profiled a high-throughput SPOE agent and found `Frame.Read` responsible for ~75% of total allocations, with GC consuming ~16% of CPU. Reusing the read buffer across pooled frames cut frame-buffer allocations by **99%** and GC overhead to **~3%**, freeing significant CPU headroom for scaling under load.
- **[microsoft/vcpkg](https://github.com/microsoft/vcpkg/pull/42991)** (C++/CMake) — Updated the `behaviortree-cpp` port from 4.3.7 to 4.6.2, including version database and SHA512 updates per the maintainer guide.

## Projects

- **[KafkaDesktopClient](https://github.com/gfeyer/KafkaDesktopClient)** (C++) — Desktop client for consuming and filtering JSON data streams from Kafka.
- **[fleet_commander](https://github.com/gfeyer/fleet_commander)** (C++) — 2D colonization simulator built on an Entity Component System architecture, optimized to handle large numbers of entities. [Playable on itch.io](https://gfeyer.itch.io/fleet-commander).
- **[DocumentSearcher](https://github.com/gfeyer/DocumentSearcher)** (C++) — Fast indexing and full-text search over large archives (.doc/.docx/.pdf), built on Lucene++. Tested on 20GB+/20,000-document archives with sub-second queries. Also shipped a separate Java/Scala implementation as a [commercial desktop product](https://documentsearcher.weebly.com/).
- **[ecs_sim](https://github.com/gfeyer/ecs_sim)** (Go) — Entity Component System simulation built from scratch.

## Interests

Scalable system design · memory and allocation behavior · serialization formats and binary protocols · GC and latency tuning · game/simulation architecture (ECS at scale)
