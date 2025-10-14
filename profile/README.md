<div align="center">

<img src="logo.png" alt="Parallax Systems Logo" width="120"/>

# Parallax Systems SDK

**Request-Based Anti-Bot Bypass Solution**

[![Discord](https://img.shields.io/badge/Discord-Join%20Us-5865F2?style=for-the-badge&logo=discord&logoColor=white)](https://discord.com/invite/2QWbHcmWnf)
[![Website](https://img.shields.io/badge/Website-Visit-00D4FF?style=for-the-badge&logo=google-chrome&logoColor=white)](https://www.parallaxsystems.io)
[![License](https://img.shields.io/badge/License-Commercial-yellow?style=for-the-badge)](https://www.parallaxsystems.io)

**DataDome Bypass • PerimeterX Bypass • CAPTCHA Solver • Sub-400ms Response**

<p align="center">
  <strong>HTTP API for anti-bot cookie generation</strong> | No browser automation required
</p>

[Features](#-features) • [Installation](#-installation) • [Quick Start](#-quick-start) • [Documentation](#-documentation) • [Discord](https://discord.com/invite/2QWbHcmWnf)

</div>

---

## 🎯 What is Parallax Systems SDK?

A **multi-language SDK** for bypassing anti-bot protection systems including **DataDome** and **PerimeterX**. Generate valid authentication cookies through a simple request-based API without the overhead of browser automation or headless browsers.

Perfect for **web scraping**, **automation**, **testing**, and **bot development** that requires bypassing bot detection systems.

### 📚 SDK Documentation

[**Go**](docs/go.md) • [**TypeScript**](docs/typescript.md) • [**Python**](docs/python.md) • [**Playwright**](docs/playwright.md)

### 🌟 Why Choose Parallax?

<table>
<tr>
<td width="50%" valign="top">

<div align="center">

**⚡ Lightning Fast**

</div>

- DataDome cookies in ~200ms
- PerimeterX cookies in ~350-400ms
- Request-based, no browser overhead

</td>
<td width="50%" valign="top">

<div align="center">

**🚀 Developer Friendly**

</div>

- Simple REST API
- 4+ language SDKs
- Comprehensive documentation

</td>
</tr>
<tr>
<td width="50%" valign="top">

<div align="center">

**🔒 Enterprise Security**

</div>

- End-to-end encryption
- SOC 2 compliant infrastructure
- Zero data retention policy

</td>
<td width="50%" valign="top">

<div align="center">

**📦 Production Ready**

</div>

- 99.9% uptime SLA
- Scalable infrastructure
- 24/7 support available

</td>
</tr>
</table>

### 🛠️ Supported Languages

| Language | Status | Install |
|----------|:------:|---------|
| ![Go](https://img.shields.io/badge/Go-00ADD8?style=flat&logo=go&logoColor=white) | ✅ | `go get parallax-sdk` |
| ![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat&logo=typescript&logoColor=white) | ✅ | `npm install @parallax/sdk` |
| ![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white) | ✅ | `pip install parallax-sdk` |
| ![Playwright](https://img.shields.io/badge/Playwright-2EAD33?style=flat&logo=playwright&logoColor=white) | ✅ | `npm install @parallax/playwright-sdk` |

---

## ✨ Features

<table>
<tr>
<th width="30%">Feature</th>
<th width="35%">DataDome</th>
<th width="35%">PerimeterX</th>
</tr>
<tr>
<td><strong>Cookie Generation</strong></td>
<td align="center">✅ ~200ms</td>
<td align="center">✅ ~350-400ms</td>
</tr>
<tr>
<td><strong>User Agent Generation</strong></td>
<td align="center">✅ Included</td>
<td align="center">❌ Not needed</td>
</tr>
<tr>
<td><strong>Challenge Solver</strong></td>
<td align="center">✅ Captcha & Interstitial</td>
<td align="center">✅ Hold Captcha</td>
</tr>
<tr>
<td><strong>Proxy Support</strong></td>
<td align="center">✅ HTTP/HTTPS/SOCKS5</td>
<td align="center">✅ HTTP/HTTPS/SOCKS5</td>
</tr>
<tr>
<td><strong>Geo-Targeting</strong></td>
<td align="center">✅ All regions</td>
<td align="center">✅ All regions</td>
</tr>
</table>

### 🎯 Use Cases

- 🤖 **Web Scraping** - Bypass bot detection for data collection
- 🧪 **Automation Testing** - Test websites protected by anti-bot systems
- 📊 **Price Monitoring** - Monitor competitor prices without detection
- 🔍 **SEO Tools** - Build SEO tools that work with protected sites
- 🛒 **E-commerce Bots** - Automate purchase flows on protected platforms

---

## 📦 Installation

<details open>
<summary><strong>Go</strong></summary>

```bash
go get github.com/yourusername/parallax-sdk
```

</details>

<details>
<summary><strong>TypeScript/JavaScript</strong></summary>

```bash
npm install @parallax/sdk
# or
yarn add @parallax/sdk
# or
pnpm add @parallax/sdk
```

</details>

<details>
<summary><strong>Python</strong></summary>

```bash
pip install parallax-sdk
# or
poetry add parallax-sdk
```

</details>

<details>
<summary><strong>Playwright</strong></summary>

```bash
npm install @parallax/playwright-sdk
```

</details>

---

## 🚀 Quick Start

### DataDome Cookie Generation

<details open>
<summary><strong>Go Example</strong></summary>

```go
package main

import (
    "fmt"
    parallax "github.com/yourusername/parallax-sdk"
)

func main() {
    sdk := parallax.NewSDK("YOUR_API_KEY", "")

    response, _ := sdk.GenerateDatadomeCookie(parallax.TaskDatadomeCookie{
        Site:        "example",
        Region:      "us",
        Proxyregion: "us",
        Proxy:       "http://user:pass@proxy:port",
        Pd:          parallax.PD_Init,
    })

    fmt.Printf("Cookie: %s\n", response.Message)
}
```

</details>

<details>
<summary><strong>TypeScript Example</strong></summary>

```typescript
import DatadomeSDK from "@parallax/sdk/datadome";

const sdk = new DatadomeSDK({ apiKey: "YOUR_API_KEY" });

const cookie = await sdk.generateCookie({
    site: "example",
    region: "us",
    proxy: "http://user:pass@proxy:port",
    proxyregion: "us",
    pd: "init",
    data: {}
});

console.log(cookie.message);
```

</details>

<details>
<summary><strong>Python Example</strong></summary>

```python
from parallax_sdk import DatadomeSDK

sdk = DatadomeSDK(api_key="YOUR_API_KEY")

response = sdk.generate_cookie(
    site="example",
    region="us",
    proxy="http://user:pass@proxy:port",
    proxyregion="us",
    pd="init"
)

print(response.message)
```

</details>

### PerimeterX Cookie Generation

<details open>
<summary><strong>Go Example</strong></summary>

```go
pxSDK := parallax.NewPerimeterxSDK("YOUR_API_KEY", "")

response, _ := pxSDK.GenerateCookies(parallax.TaskGeneratePXCookies{
    Site:        "example",
    Region:      "com",
    Proxyregion: "us",
    Proxy:       "http://user:pass@proxy:port",
})

fmt.Printf("_px3: %s\n_pxvid: %s\npxcts: %s\n",
    response.Cookie, response.Vid, response.Cts)
```

</details>

<details>
<summary><strong>TypeScript Example</strong></summary>

```typescript
import PerimeterxSDK from "@parallax/sdk/perimeterx";

const sdk = new PerimeterxSDK({ apiKey: "YOUR_API_KEY" });

const result = await sdk.generateCookies({
    site: "example",
    region: "com",
    proxy: "http://user:pass@proxy:port",
    proxyregion: "us"
});

console.log(`_px3: ${result.cookie}\n_pxvid: ${result.vid}\npxcts: ${result.cts}`);
```

</details>

---

## 📚 Documentation

### 🔧 SDK-Specific Guides

| Language | Documentation | Examples |
|----------|---------------|----------|
| Go | [Go SDK Guide](docs/go.md) | Complete API reference |
| TypeScript | [TypeScript SDK Guide](docs/typescript.md) | Async/await patterns |
| Python | [Python SDK Guide](docs/python.md) | Asyncio support |
| Playwright | [Playwright SDK Guide](docs/playwright.md) | Browser integration |

### ���� Advanced Topics

- **[Authentication](docs/authentication.md)** - API key management and security
- **[Proxy Configuration](docs/proxies.md)** - Proxy setup and best practices
- **[Error Handling](docs/errors.md)** - Error codes and troubleshooting
- **[Rate Limits](docs/rate-limits.md)** - Understanding request limits and quotas
- **[Best Practices](docs/best-practices.md)** - Production deployment guidelines

---

## 💼 Get Started

<div align="center">

### Ready to bypass anti-bot protection?

[![Get API Key](https://img.shields.io/badge/Get_API_Key-Start_Free_Trial-00D4FF?style=for-the-badge&logo=key&logoColor=white)](https://www.parallaxsystems.io/signup)
[![View Pricing](https://img.shields.io/badge/View_Pricing-Transparent-green?style=for-the-badge&logo=pricetag&logoColor=white)](https://www.parallaxsystems.io/pricing)
[![Join Discord](https://img.shields.io/badge/Join_Discord-Get_Help-5865F2?style=for-the-badge&logo=discord&logoColor=white)](https://discord.com/invite/2QWbHcmWnf)

</div>

---

## 🛠️ Support

<table>
<tr>
<td align="center" width="25%">
<img src="https://img.icons8.com/color/96/000000/discord-logo.png" width="48"/><br/>
<strong>Discord Community</strong><br/>
<a href="https://discord.com/invite/2QWbHcmWnf">Join our server</a>
</td>
<td align="center" width="25%">
<img src="https://img.icons8.com/color/96/000000/domain.png" width="48"/><br/>
<strong>Website</strong><br/>
<a href="https://www.parallaxsystems.io">parallaxsystems.io</a>
</td>
<td align="center" width="25%">
<img src="https://img.icons8.com/color/96/000000/email.png" width="48"/><br/>
<strong>Email Support</strong><br/>
<a href="mailto:support@parallaxsystems.io">support@parallaxsystems.io</a>
</td>
<td align="center" width="25%">
<img src="https://img.icons8.com/color/96/000000/book.png" width="48"/><br/>
<strong>Documentation</strong><br/>
<a href="https://docs.parallaxsystems.io">docs.parallaxsystems.io</a>
</td>
</tr>
</table>

---

## 🔑 Keywords

**Anti-bot bypass** • **Bot detection bypass** • **DataDome bypass** • **PerimeterX bypass** • **CAPTCHA solver** • **Challenge solver** • **Cookie generator** • **Web scraping** • **Bot automation** • **WAF bypass** • **Cloudflare bypass** • **Akamai bypass** • **Automation testing** • **Headless browser alternative** • **Anti-bot protection** • **Bot mitigation bypass** • **Sensor data generation** • **Browser fingerprinting bypass**

---

<div align="center">

**Built with ❤️ by the Parallax Systems Team**

© 2025 Parallax Systems. All rights reserved.

[Terms of Service](https://www.parallaxsystems.io/terms) • [Privacy Policy](https://www.parallaxsystems.io/privacy) • [Security](https://www.parallaxsystems.io/security)

</div>
