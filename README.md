# Niagara-4-FRPC-Module 🌐

[![Niagara 4.14+](https://img.shields.io/badge/Niagara-4.14%2B-blue)](https://www.tridium.com)
[![License: Trial](https://img.shields.io/badge/License-Trial%20%7C%20Commercial-orange)](LICENSE)
[![Contact](https://img.shields.io/badge/Contact-WhatsApp-brightgreen)](https://wa.me/8613801909968)

> **Remote access for Niagara stations behind NAT/firewall — no VPN required.**

---

## What Is It?

Deploy an FRPC (Fast Reverse Proxy Client) tunnel directly inside your Niagara Station. Expose JACE intranet ports (HTTP, Fox, oBIX, etc.) to the cloud so you can access them remotely without VPN configuration.

### Why FRPC?

JACE controllers are typically deployed behind customer firewalls with no public IP. Traditionally you need:

- VPN server ❌ (complex setup)
- Static public IP ❌ (expensive)
- Port forwarding ❌ (security risk)

**FRPC solves this** with a single lightweight tunnel.

---

## Quick Start

```bash
# 1. Set up an FRPS server on your cloud VM (frps.zip included)

# 2. Install gline.pem certificate into your station trust store

# 3. Add glineFrpc-rt.jar to your modules/ directory

# 4. Restart station

# 5. Create a GlineFrpc component in Workbench:
#    - Set FRPS server IP / port
#    - Configure which local ports to map
#    - Set cloud-side mapping ports

# 6. Enable the tunnel — test connectivity from the cloud
```

---

## Features

| Feature | Support |
|---------|:-------:|
| Cloud port mapping | ✅ |
| Auto-reconnect on network interruption | ✅ |
| Auto-reconnect after station reboot | ❌ (requires health check program) |
| JACE-8000 compatible | ✅ Tested |
| Edge / N4.14+ | ✅ Tested |
| Windows Supervisor | ✅ Tested |

### Included Health Check

The repo includes `CurlCommand_check_FRPC_Port.bog` — a program that verifies cloud port availability and can trigger a reconnection attempt. Open it in Workbench to configure.

---

## Pricing

| Tier | License | Price |
|:----:|---------|:-----:|
| 🆓 | **Trial** | **Free for 30 days** (per station start) |
| 🥇 | **Single Station** | **$149** |
| 🏢 | **Site Pack (5 stations)** | **$599** |

> Trial: 30 days of full functionality after each station restart.  
> Commercial licenses include 12 months of updates and email support.

---

## Requirements

| Component | Requirement |
|-----------|-------------|
| **Niagara** | 4.14 or later |
| **JAR signing** | Requires gline.pem certificate |
| **Cloud server** | FRPS server (Linux/Windows) — frps.zip included |
| **Network** | Outbound from JACE → cloud FRPS server (port configurable) |

---

## Documentation

| Manual | Description |
|--------|-------------|
| [FRPC User Manual](docs/FRPC%20User%20Manual.pdf) | Complete deployment and configuration guide |

---

## Support & Contact

- **Email**: [jason.zhang@gline-net.com](mailto:jason.zhang@gline-net.com)
- **WhatsApp**: [+86 138 0199 0968](https://wa.me/8613801909968)

**Shanghai Gline Net Co., Ltd.** — Your Partner in Smarter Automation

---

© 2026 Shanghai Gline Net Co., Ltd. All rights reserved.
