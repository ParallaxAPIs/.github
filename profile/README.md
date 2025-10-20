<div align="center">

# Parallax API SDK's

**Request-based anti-bot bypass solution for DataDome & PerimeterX.**

[![Discord](https://img.shields.io/badge/Discord-Join%20Us-5865F2?style=for-the-badge&logo=discord&logoColor=white)](https://www.parallaxsystems.io/join?s=gh)
[![Website](https://img.shields.io/badge/Website-Visit-00D4FF?style=for-the-badge&logo=google-chrome&logoColor=white)](https://www.parallaxsystems.io)

[Quick Start](#-quick-start) • [Installation](#-installation) • [Features](#-features) • [Code Examples](#-code-examples) • [Documentation](#-documentation) • [Discord](https://www.parallaxsystems.io/join?s=gh)

</div>

---

## 🎯 What is Parallax API SDK's?

**Multiple SDKs** for bypassing anti-bot protection systems including **DataDome** and **PerimeterX**. Generate valid authentication cookies through a simple request-based API without the overhead of browser automation or headless browsers.

Perfect for **web scraping**, **automation**, **testing**, and **bot development** that requires bypassing bot detection systems.

---

## 🚀 Quick Start

Get started with Parallax API SDK's in under 5 minutes:

1. **Join our [Discord](https://www.parallaxsystems.io/join?s=gh)** - Connect with our community
2. **Create a ticket** - Request your API key
3. **Get your free trial** - Start testing immediately
4. **[Install the SDK](#-installation)** - Choose your preferred language
5. **Solve all anti-bots in seconds** - Start bypassing DataDome, PerimeterX & more

![PerimeterX Demo](parallax_perimeterx.gif)

---

## 📦 Installation

| Language | Package | Installation |
|----------|---------|--------------|
| **Go** | [parallax-sdk-go](https://github.com/ParallaxAPIs/parallax-sdk-go) | `go get github.com/ParallaxAPIs/parallax-sdk-go` |
| **TypeScript** | [parallax-sdk-ts](https://github.com/ParallaxAPIs/parallax-sdk-ts) | `npm install parallax-sdk-ts` |
| **Python** | [parallax-sdk-py](https://github.com/ParallaxAPIs/parallax-sdk-py) | `pip install parallax-sdk-py` |
| **Playwright** | [parallax-sdk-playwright](https://github.com/ParallaxAPIs/parallax-sdk-playwright) | `npm install parallax-sdk-playwright` |

---

## ✨ Features

We provide solutions for all challenges served by these leading anti-bot systems.

### DataDome

**What we solve:**

- ✅ **Slider Captchas** - Automatic slider puzzle solving
- ✅ **Interstitial Pages** - Solve interstitial challenge pages
- ✅ **Tags Payload** - Create valid tags payloads
- ✅ **Cookie Generation** - Valid DataDome cookies in ~200ms
- ✅ **User Agent Generation** - Generate matching user agents

### PerimeterX

**What we solve:**

- ✅ **Cookie Generation** - Valid _px3 cookies in ~350-400ms
- ✅ **Challenge Solver** - Solve Hold Captcha challenges
- ✅ **Vid & Cts Tokens** - Complete token generation

### Additional Features

- 🌍 **Geo-Targeting** - Support for all regions worldwide
- 🔌 **Proxy Support** - HTTP/HTTPS/SOCKS5 compatible
- ⚡ **Lightning Fast** - Sub-millisecond response times for our solutions
- 🔒 **Enterprise Security** - End-to-end encryption

### Use Cases

- **Web Scraping** - Bypass bot detection for data collection
- **Automation Testing** - Test websites protected by anti-bot systems
- **Price Monitoring** - Monitor competitor prices without detection
- **SEO Tools** - Build SEO tools that work with protected sites
- **E-commerce Bots** - Automate purchase flows on protected platforms
- **Market Research** - Gather market intelligence from protected websites
- **Inventory Tracking** - Monitor stock levels across multiple retailers
- **Lead Generation** - Extract business data from protected directories
- **Travel Aggregation** - Collect pricing data from flight and hotel booking sites
- **Social Media Analytics** - Access and analyze data from protected social platforms
- **Real Estate Data** - Scrape property listings and market trends
- **Job Market Analysis** - Aggregate job postings from protected career sites

---

## Why Choose Parallax?

<table>
<tr>
<td width="50%">

### ⚡ Lightning Fast
• DataDome cookies in **~200ms**
• PerimeterX cookies in **~350-400ms**
• Request-based, no browser overhead

</td>
<td width="50%">

### 🛠️ Developer Friendly
• Simple REST API
• 4+ language SDKs
• Comprehensive documentation

</td>
</tr>
<tr>
<td width="50%">

### 🔒 Enterprise Security
• End-to-end encryption
• SOC 2 compliant infrastructure

</td>
<td width="50%">

### 📦 Production Ready
• 99.9% uptime SLA
• Scalable infrastructure
• 24/7 support on Discord available

</td>
</tr>
</table>

---

## 🚀 Why Request-Based?

<table>
<tr>
<th width="50%">🌐 Browser-Based Solutions</th>
<th width="50%">⚡ Request-Based (Parallax)</th>
</tr>
<tr>
<td valign="top">

**Challenges:**
- ❌ Slow performance (2-5+ seconds per request)
- ❌ High resource consumption (RAM, CPU)
- ❌ Complex infrastructure requirements
- ❌ Difficult to scale horizontally
- ❌ Browser detection & fingerprinting issues
- ❌ Maintenance overhead for browser versions

</td>
<td valign="top">

**Benefits:**
- ✅ Lightning fast (200-400ms response time)
- ✅ Minimal resource usage
- ✅ Simple API integration
- ✅ Easily scales to millions of requests
- ✅ No browser fingerprinting concerns
- ✅ Zero maintenance overhead

</td>
</tr>
<tr>
<td valign="top">

**Use When:**
- You want to be slower than your competitors
- You want to get your device banned

</td>
<td valign="top">

**Use When:**
- Speed and efficiency are priorities
- High-volume operations required
- Simple cookie/token generation needed
- Infrastructure costs matter

</td>
</tr>
</table>

---

## 💻 Code Examples

### DataDome Cookie Generation

<details open>
<summary><strong>Go Example</strong></summary>

```go
package main

import (
    "fmt"
    "github.com/parallaxsystems/parallax-sdk-go"
)

func main() {
    sdk := parallaxsdk.NewDatadomeSDK("YOUR_API_KEY", "")

    response, _ := sdk.GenerateDatadomeCookie(parallaxsdk.TaskDatadomeCookie{
        Site:        "example",
        Region:      "us",
        Proxyregion: "us",
        Proxy:       "http://user:pass@proxy:port",
        Pd:          parallaxsdk.PD_Init,
    })

    fmt.Printf("Cookie: %s\n", response.Message)
}
```

</details>

<details>
<summary><strong>TypeScript Example</strong></summary>

```typescript
import { DatadomeSDK, ProductType } from "parallax-sdk-ts";

const sdk = new DatadomeSDK({ apiKey: "YOUR_API_KEY" });

const cookie = await sdk.generateCookie({
    site: "example",
    region: "us",
    proxy: "http://user:pass@proxy:port",
    proxyregion: "us",
    pd: ProductType.Init,
    data: {} as any
});

console.log(cookie.message);
```

</details>

<details>
<summary><strong>Python Example</strong></summary>

```python
from parallax_sdk_py import DatadomeSDK, ProductType

sdk = DatadomeSDK(host="", api_key="YOUR_API_KEY")

response = await sdk.generate_cookie(
    site="example",
    region="us",
    proxy="http://user:pass@proxy:port",
    proxyregion="us",
    pd=ProductType.Init
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
import { PerimeterxSDK } from "parallax-sdk-ts";

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

<details>
<summary><strong>Python Example</strong></summary>

```python
from src import PerimeterxSDK, TaskGeneratePXCookies

sdk = PerimeterxSDK(host="", api_key="YOUR_API_KEY")

task = TaskGeneratePXCookies(
    site="example",
    region="com",
    proxy="http://user:pass@proxy:port",
    proxyregion="us"
)

result = await sdk.generate_cookies(task)

print(f"_px3: {result['cookie']}\n_pxvid: {result['vid']}\npxcts: {result['cts']}")
```

</details>

---

## 📚 Documentation

### SDK-Specific Guides

| Language | Documentation | Examples |
|----------|---------------|----------|
| Go | [Go SDK Guide](parallax-sdk-go/README.md) | Complete API reference |
| TypeScript | [TypeScript SDK Guide](parallax-sdk-ts/README.md) | Async/await patterns |
| Python | [Python SDK Guide](parallax-sdk-py/README.md) | Asyncio support |
| Playwright | [Playwright SDK Guide](parallax-sdk-playwright/README.md) | Browser integration |

---

<div align="center">

© 2025 Parallax Systems. All rights reserved.

[Terms of Service](https://www.parallaxsystems.io/terms) • [Privacy Policy](https://www.parallaxsystems.io/privacy) • [Security](https://www.parallaxsystems.io/security)

</div>
