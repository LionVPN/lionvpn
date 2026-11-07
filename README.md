<p align="center">
  <img src="assets/lionvpn-logo.png" width="112" alt="LionVPN logo">
</p>

<h1 align="center">LionVPN: Fast, No-Logs VPN Access</h1>

<p align="center">
  A no-logs VPN focused on security and privacy, with regional servers and automatic route selection<br>
  to choose faster, more reliable connections.
</p>

<p align="center">
  <a href="https://lionvpn.com/en/download"><img alt="Download" src="https://img.shields.io/badge/Download-lionvpn.com-F5A623?style=flat-square"></a>
  <a href="https://lionvpn.com/en/download"><img alt="macOS 6.4" src="https://img.shields.io/badge/macOS-6.4-000000?style=flat-square&logo=apple&logoColor=white"></a>
  <a href="https://lionvpn.com/en/download"><img alt="Windows 3.0.1" src="https://img.shields.io/badge/Windows-3.0.1-0078D4?style=flat-square"></a>
  <a href="https://apps.apple.com/app/id1445424991"><img alt="App Store" src="https://img.shields.io/badge/iOS-App%20Store-0D96F6?style=flat-square&logo=appstore&logoColor=white"></a>
  <a href="https://play.google.com/store/apps/details?id=com.vpn.peervpn"><img alt="Google Play" src="https://img.shields.io/badge/Android-Google%20Play-34A853?style=flat-square&logo=googleplay&logoColor=white"></a>
  <a href="https://lionvpn.com/en/download"><img alt="Linux 0.1.3-rc.1" src="https://img.shields.io/badge/Linux%20%2F%20OpenWrt-0.1.3--rc.1-FCC624?style=flat-square&logo=linux&logoColor=black"></a>
</p>

<p align="center">
  <a href="https://lionvpn.com/en">Website</a> ·
  <a href="https://lionvpn.com/en/pricing">Pricing</a> ·
  <a href="https://lionvpn.com/en/servers">Servers</a> ·
  <a href="https://lionvpn.com/en/faq">FAQ</a> ·
  <a href="https://lionvpn.com/en/support">Support</a>
</p>

<p align="center">
  <b>English</b> ·
  <a href="README.zh-CN.md">简体中文</a> ·
  <a href="README.zh-TW.md">繁體中文</a> ·
  <a href="README.ja.md">日本語</a> ·
  <a href="README.ko.md">한국어</a> ·
  <a href="README.vi.md">Tiếng Việt</a>
</p>

---

## Why choose LionVPN

No-logs comes first, followed by security, privacy, regional servers, and route selection for faster, more reliable connections.

| | |
| --- | --- |
| 🔒 **No-logs privacy** | LionVPN puts no-logs first so your activity stays yours, with privacy kept at the center of the product experience. |
| ⚡ **Automatic route selection** | Automatic route selection matches you to faster, more stable server paths with less manual choosing. |
| 🌍 **Regional server coverage** | Keep access to regional server locations so you can connect closer to where you need speed, stability, and availability. |
| 🛡️ **Security and privacy** | Secure, encrypted connections and a privacy-first design help protect everyday browsing, work, and travel. |
| 🔁 **Reliable connections** | Speed, stability, security, and privacy work together in one connection experience. |
| 🧭 **Protocol roadmap** | The product is VPN-first. SOCKS5 is supported where enabled, and H2 is being added progressively. |

## About LionVPN

LionVPN emphasizes no-logs, strong security and privacy, regional server coverage, and automatic route selection to help users reach faster, more reliable connections.

The goal is straightforward: protect privacy, keep connections secure, and make it easier to reach a fast, stable server without extra complexity. Regional servers remain available today. SOCKS5 is supported where enabled, while H2 is being added progressively alongside the current VPN experience.

## Download

All installers are published on the official site and the app stores.

| Platform | Latest | Get it |
| --- | --- | --- |
| macOS 12.4 or later | **6.4** — Universal (Apple silicon + Intel), notarized by Apple | [lionvpn.com/en/download](https://lionvpn.com/en/download) |
| Windows 7 – 11 | **3.0.1** — 32-bit and 64-bit, code-signed | [lionvpn.com/en/download](https://lionvpn.com/en/download) · [LionVPN-3.0.1.exe](LionVPN-3.0.1.exe) in this repository |
| iOS / iPadOS | App Store · Enterprise install | [App Store](https://apps.apple.com/app/id1445424991) · [Enterprise install](https://lionvpn.com/en/install) |
| Android / Android TV | Google Play | [Google Play](https://play.google.com/store/apps/details?id=com.vpn.peervpn) |
| Linux | **0.1.3-rc.1** — `.deb` (amd64, arm64), `.rpm` (x86_64, aarch64), portable `.tar.gz` | [lionvpn.com/en/download](https://lionvpn.com/en/download) |
| OpenWrt 24.10 / 25.12 | **0.1.3-rc.1** — `.ipk` and `.apk` for x86_64 and aarch64_cortex-a53 | [lionvpn.com/en/download](https://lionvpn.com/en/download) |

The Windows installer in this repository is byte-identical to the one served from lionvpn.com.
SHA-256: `b8b504c92d0ef5703b0f1334d832b523af46fa681e2c261e5a6b76148206cc69`.

## Protocols and transports

| Transport | Description | Platforms |
| --- | --- | --- |
| **LionVPN UDP** | Native UDP tunnel with a KCP reliability layer, AES-256 encryption and ECC key exchange | macOS, Windows, iOS, Android, Linux |
| **LionVPN TCP** | The same protocol over TCP for networks that block UDP | macOS, iOS, Android, Linux |
| **CDN mode** | VLESS + XHTTP over TLS on standard HTTPS, for heavily filtered networks | macOS 6.4, iOS |
| **Hysteria 2** | QUIC-based transport for lossy or throttled links | macOS 6.4, iOS (next release) |
| **SOCKS5** | Supported where enabled | Depends on client build and deployment |
| **H2** | Being added progressively | Roadmap |

Availability depends on the client build and the deployed environment. Not every access mode is exposed in every release.

## What's new

- **macOS 6.4** — CDN mode and Hysteria 2 support, relay line selection in Settings, hardened classic UDP/TCP channel. Notarized Universal build.
- **iOS** — CDN mode is the default transport on every server. Hysteria 2 with real DNS over the tunnel ships in the next release.
- **Linux and OpenWrt 0.1.3-rc.1** — first public packages for Debian/Ubuntu, RHEL/Fedora, portable archives and OpenWrt.
- **Login integrity** — server login replies are signed and verified on UDP, TCP and CDN paths.
- **Fewer drops on mobile networks** — login retries back off on cellular links, redundant re-logins are gone, and local devices (AirPlay, printers) keep working while connected.

## Common questions

**What does LionVPN protect?**
LionVPN encrypts your traffic, masks your IP address, and helps reduce exposure when you use public or shared networks.

**How quickly can I get started?**
Pick a plan, download the app for your device, sign in, and connect to a recommended location in just a few minutes.

**Can I use LionVPN for work, travel, and streaming?**
LionVPN is suited to everyday browsing, work, travel, and account access. Compatibility with specific third-party services should not be treated as guaranteed.

More answers: [FAQ](https://lionvpn.com/en/faq) · [Support center](https://lionvpn.com/en/support) · [support@lionvpn.com](mailto:support@lionvpn.com)

## Privacy and terms

[Privacy policy](https://lionvpn.com/en/privacy) · [Terms of service](https://lionvpn.com/en/terms)

## License

LionVPN is proprietary software of Master Proxy Co. See [license.txt](license.txt). The source code is not published in this repository.
