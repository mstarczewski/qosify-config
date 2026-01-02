# OpenWrt Qosify: diffserv8 (8-tin mode) Mapping Reference

This document provides a verified mapping for the `diffserv8` (8-tin) mode in Qosify/CAKE. 

## Mapping Table

| Tin | Class Name | Priority | Purpose / Traffic Type | Traffic Type (Standard Definition) | DSCP Mapping |
|:---:|:---|:---:|:---|:---|:---|
| **0** | `background` | 1 (Low) | Pure Background / Scavenger | Lower Effort (RFC 8622) | `LE` (1) |
| **1** | `bulk` | 2 | High Throughput / Bulk Data | Class Selector 1 (Priority) | `CS1` (8) |
| **1** | *(NOT USED)* | 2 | *(NOT USED)* | Assured Forwarding 11 (Low Drop) | `AF11` (10) |
| **1** | *(NOT USED)* | 2 | *(NOT USED)* | Assured Forwarding 12 (Medium Drop) | `AF12` (12) |
| **1** | *(NOT USED)* | 2 | *(NOT USED)* | Assured Forwarding 13 (High Drop) | `AF13` (14) |
| **2** | `besteffort` | 3 | Standard Internet Traffic (DF) | Default Forwarding / Best Effort | `CS0` (0) |
| **3** | *(NOT USED)* | 4 | *(NOT USED)* | Class Selector 3 (Broadcast Video) | `CS3` (24) |
| **3** | *(NOT USED)* | 4 | *(NOT USED)* | Assured Forwarding 31 (Low Drop) | `AF31` (26) |
| **3** | *(NOT USED)* | 4 | *(NOT USED)* | Assured Forwarding 32 (Medium Drop) | `AF32` (28) |
| **3** | *(NOT USED)* | 4 | *(NOT USED)* | Assured Forwarding 33 (High Drop) | `AF33` (30) |
| **3** | `video` | 4 | Video Streaming | Assured Forwarding 41 (Low Drop) | `AF41` (34) |
| **3** | *(NOT USED)* | 4 | *(NOT USED)* | Assured Forwarding 42 (Medium Drop) | `AF42` (36) |
| **3** | *(NOT USED)* | 4 | *(NOT USED)* | Assured Forwarding 43 (High Drop) | `AF43` (38) |
| **4** | `voice` | 5 | Interactive Video/Audio (Teams) | Assured Forwarding 21 (Low Drop) | `AF21` (18) |
| **4** | *(NOT USED)* | 5 | *(NOT USED)* | Assured Forwarding 22 (Medium Drop) | `AF22` (20) |
| **4** | *(NOT USED)* | 5 | *(NOT USED)* | Assured Forwarding 23 (High Drop) | `AF23` (22) |
| **5** | `network_services` | 6 | DNS, ICMP (Ping), NTP, Routing | Class Selector 2 (OAM) | `CS2` (16) |
| **6** | `gaming` | 7 | High Priority Data, Games | Class Selector 4 (Real-Time Interactive) | `CS4` (32) |
| **6** | *(NOT USED)* | 7 | *(NOT USED)* | Class Selector 5 (Signaling) | `CS5` (40) |
| **6** | *(NOT USED)* | 7 | *(NOT USED)* | Voice Admit (Call Admission Control) | `VA` (44) |
| **6** | *(NOT USED)* | 7 | *(NOT USED)* | Expedited Forwarding (Premium VoIP) | `EF` (46) |
| **7** | *(NOT USED)* | 8 (High) | *(NOT USED)* | Class Selector 6 (Network Control) | `CS6` (48) |
| **7** | `telephony` | 8 (High) | Critical Control, Voice Sign. | Class Selector 7 (Reserved) | `CS7` (56) |
