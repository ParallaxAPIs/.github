<div align="center">

# ParallaxAPIs SDK's

**Request-based anti-bot bypass solution for DataDome & PerimeterX.**

[![Discord](https://img.shields.io/badge/Discord-Join%20Us-5865F2?style=for-the-badge&logo=discord&logoColor=white)](https://www.parallaxsystems.io/join?s=gh)
[![Website](https://img.shields.io/badge/Website-Visit-00D4FF?style=for-the-badge&logo=google-chrome&logoColor=white)](https://www.parallaxsystems.io)

[Quick Start](#-quick-start) • [Installation](#-installation) • [Features](#-features) • [Code Examples](#-code-examples) • [Documentation](#-documentation) • [Discord](https://www.parallaxsystems.io/join?s=gh)

</div>

---

## 🎯 What is ParallaxAPIs SDK's?

**Multiple SDKs** for bypassing anti-bot protection systems including **DataDome** and **PerimeterX**. Generate valid antibot cookies through a simple request-based API without the overhead of browser automation or headless browsers.

Perfect for **web scraping**, **automation**, **testing**, and **bot development** that requires bypassing bot detection systems.

---

## 🚀 Quick Start

Get started with ParallaxAPIs SDK's in under 5 minutes:

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
| **Go** | [parallaxapis-sdk-go](https://github.com/ParallaxAPIs/parallaxapis-sdk-go) | `go get github.com/ParallaxAPIs/parallax-sdk-go` |
| **TypeScript** | [parallaxapis-sdk-ts](https://github.com/ParallaxAPIs/parallaxapis-sdk-ts) | `npm install parallaxapis-sdk-ts` |
| **Python** | [parallaxapis-sdk-py](https://github.com/ParallaxAPIs/parallaxapis-sdk-py) | `pip install parallaxapis-sdk-py` |
| **Playwright** | [parallaxapis-sdk-playwright](https://github.com/ParallaxAPIs/parallaxapis-sdk-playwright) | `npm install parallaxapis-sdk-playwright` |

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
- ✅ **Web and Mobile supported** - Generation on any device
- ✅ **Challenge Solver** - Automatic HoldCaptcha solving
- ✅ **_pxvid, pxcts & _pxhd Tokens** - Complete token generation

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

## Why Choose ParallaxAPIs?

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
- ✅ Lightweight infrastructure - No heavy browser dependencies or containers
- ✅ Minimal proxy usage - Efficient bandwidth consumption per request
- ✅ Simple API integration
- ✅ Parallel processing - Handle thousands of concurrent requests easily
- ✅ Easily scales to millions of requests
- ✅ No browser fingerprinting concerns
- ✅ Always working — we take care of the reverse engineering for you
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
    sdk := parallaxsdk.NewDatadomeSDK("Key", "")
    
    challengeURL := "https://www.example.com/captcha/?initialCid=initialCid&cid=cid&referer=referer&hash=hash&t=t&s=1&e=e"
    cookie := "cookie_value"
    
    taskData, productType, err := parallaxsdk.ParseChallengeURL(challengeURL, cookie)
    if err != nil {
        panic(err)
    }
    
    cookieResp, err := sdk.GenerateDatadomeCookie(parallaxsdk.TaskDatadomeCookie{
        Site: "site",
        Region: "com",
        Data: *taskData,
        Pd: productType,
        Proxy: "http://user:pas@addr:port",
        Proxyregion: "eu",
    })
    if err != nil {
        panic(err)
    }
    
    fmt.Println(cookieResp)
}
```

</details>

<details>
<summary><strong>TypeScript Example</strong></summary>

```typescript
import DatadomeSDK from "parallaxapis-sdk-ts";

const sdk = new DatadomeSDK({ apiKey: "Key" });

const [taskData, productType] = sdk.parseChallengeUrl(
    "https://www.example.com/captcha/?initialCid=initialCid&cid=cid&referer=referer&hash=hash&t=t&s=1&e=e",
    "cookie_value",
);

const cookie = await sdk.generateCookie({
    site: "site",
    region: "com",
    data: taskData,
    pd: productType,
    proxy: "http://user:pas@addr:port",
    proxyregion: "eu"
});

console.log(cookie);
```

</details>

<details>
<summary><strong>Python Example</strong></summary>

```python
from parallax_sdk_py.src.datadome import DatadomeSDK
from parallax_sdk_py.src.sdk import SDKConfig
from parallax_sdk_py.src.tasks import TaskGenerateDatadomeCookie

cfg = SDKConfig(
    host="host.com", # Optional
    api_key="Key",
    timeout=60,  # Optional: custom timeout
    proxy="http://user:pass@proxy.example.com:8080"  # Optional: SDK-level proxy
)

with DatadomeSDK(cfg=cfg) as sdk:
    challenge_url = "https://www.example.com/captcha/?initialCid=initialCid&cid=cid&referer=referer&hash=hash&t=t&s=s&e=e"
    cookie = "cookie_value"
    task_data, product_type = sdk.parse_challenge_url(challenge_url, cookie)

    cookie_response = sdk.generate_cookie(TaskGenerateDatadomeCookie(
        site="site",
        region="com",
        data=task_data,
        pd=product_type,
        proxy="http://user:pas@addr:port",  # Task-level proxy (for solving)
        proxyregion="eu"
    ))

    print(cookie_response)
```

</details>

<details>
<summary><strong>Playwright Example</strong></summary>

```javascript
import DatadomeHandler from 'parallaxapis-sdk-playwright';

async function main() {
    const [page, browser] = await DatadomeHandler.init({
        apiKey: "DD-KEY",
        apiHost: "parallaxhost.com", //optional
        proxy: `http://user:password@host:port`,
        proxyRegion: "eu",
        region: "com",
        site: "website",
    })

    await page.goto('https://www.website.com/');
    
    /*
    
        You can use your browser solution however you want, ParallaxAPIs 
        will handle the rest for you. 
        
    */
    
    await browser.close();
}

main().catch(console.error);
```

</details>

### PerimeterX Cookie Generation

<details open>
<summary><strong>Go Example</strong></summary>

```go
package main

import (
    "fmt"
    "github.com/parallaxsystems/parallax-sdk-go"
)

func main() {
    sdk := parallaxsdk.NewPerimeterxSDK("Key", "")

    result, err := sdk.GenerateCookies(parallaxsdk.TaskGeneratePXCookies{
        Proxy: "http://user:pas@addr:port",
        Proxyregion: "eu",
        Region: "com",
        Site: "site",
    })
    if err != nil {
        panic(err)
    }
    
    fmt.Printf(result)

    //holdcaptcha
    holdCaptchaResult, err := sdk.GenerateHoldCaptcha(parallaxsdk.TaskGenerateHoldCaptcha{
        Proxy: "http://user:pas@addr:port",
        Proxyregion: "eu",
        Region: "com",
        Site: "site",
        Data: result.Data,
        PowPro: "",
    })
    if err != nil {
        panic(err)
    }
    
    fmt.Printf(holdCaptchaResult)
}
```

</details>

<details>
<summary><strong>TypeScript Example</strong></summary>

```typescript
import PerimeterxSDK from "parallaxapis-sdk-ts";
import type { TaskGenerateHoldCaptcha, TaskGeneratePXCookies } from "parallaxapis-sdk-ts";

const sdk = new PerimeterxSDK({
    apiKey: "Key",
});

const result = await sdk.generateCookies({
    proxy: "http://user:pas@addr:port",
    proxyregion: "eu",
    region: "com",
    site: "site"
} satisfies TaskGeneratePXCookies);

console.log(JSON.stringify(result))

//holdcaptcha
const holdCaptchaResult = await sdk.generateHoldCaptcha({
    proxy: "http://user:pas@addr:port",
    proxyregion: "eu",
    region: "com",
    site: "site",
    data: result.data,
} satisfies TaskGenerateHoldCaptcha);

console.log(JSON.stringify(holdCaptchaResult))
```

</details>

<details>
<summary><strong>Python Example</strong></summary>

```python
from parallax_sdk_py.src.perimeterx import AsyncPerimeterxSDK
from parallax_sdk_py.src.sdk import SDKConfig
from parallax_sdk_py.src.tasks import TaskGeneratePXCookies, TaskGenerateHoldCaptcha

cfg = SDKConfig(
    host="host.com",
    api_key="Key",
    timeout=60  # Optional: custom timeout
)

async with AsyncPerimeterxSDK(cfg=cfg) as sdk:
    result = await sdk.generate_cookies(TaskGeneratePXCookies(
        proxy="http://user:pas@addr:port",
        proxyregion="eu",
        region="com",
        site="site"
    ))

    print(result)


    hold_captcha_result = await sdk.generate_hold_captcha(TaskGenerateHoldCaptcha(
        proxy="http://user:pas@addr:port",
        proxyregion="eu",
        region="com",
        site="site",
        data=result['data'],
        POW_PRO=None
    ))

    print(hold_captcha_result)
```

</details>

<details>
<summary><strong>Playwright Example</strong></summary>

```javascript
import { PerimeterxHandler } from 'parallaxapis-sdk-playwright';

async function main() {
    const [page, browser] = await PerimeterxHandler.init({
        apiKey: "PX-KEY",
        apiHost: "parallaxhost.com", //optional
        proxy: `http://user:password@host:port`,
        proxyRegion: "eu",
        region: "com",
        site: "website",
        websiteUrl: "https://www.website.com/"
    })

    await page.goto('https://www.website.com/');
    
    /*
    
        You can use your browser solution however you want, ParallaxAPIs 
        will handle the rest for you. 
        
    */
    
    await browser.close();
}

main().catch(console.error);
```

</details>

---

## 🏢 Enterprise

Unlock enterprise-grade performance with custom solutions, expanded limits, and expert support. Contact us to learn more.

---

<div align="center">

© 2025 ParallaxSystems. All rights reserved.

[Terms of Service](https://www.parallaxsystems.io/terms) • [Privacy Policy](https://www.parallaxsystems.io/privacy) • [Security](https://www.parallaxsystems.io/security)

</div>
