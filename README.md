# 🕵️‍♂️ TotalOSINT

**The All-in-One, Privacy-First OSINT Investigation Toolkit.**

TotalOSINT is a client-side OSINT workbench designed for SOC analysts, threat hunters, and DFIR teams. Instantly extract indicators of compromise (IOCs) from raw logs and launch bulk investigations across dozens of threat intelligence sources. 

Built with OpSec in mind: **Zero data persistence. No backend APIs. Single-file deployment.**

[![Live Demo](https://img.shields.io/badge/demo-Live%20on%20GitHub%20Pages-brightgreen?style=for-the-badge&logo=github)](https://jhatzimalis.github.io/TotalOSINT)
![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Security](https://img.shields.io/badge/Security-Client%20Side%20Only-green.svg)
![Deployment](https://img.shields.io/badge/Deployment-Single%20HTML%20File-orange.svg)

## ✨ Features

* **⚡ Smart Extraction:** Automatically parses raw text, notes, or logs to extract and deduplicate IPv4/IPv6, Domains, URLs, and MD5/SHA hashes.
* **🛡️ OPSEC First:** Zero data persistence. Inputs and investigation notes are held in RAM only and wiped on page refresh. No data is sent to any backend server.
* **🚀 Bulk Investigation:** Select multiple sources (or trigger pre-configured Presets) and open them simultaneously in new tabs.
* **🎯 Source Presets & Favorites:** Star your favorite tools (💙) and map sources to quick-select Presets (🟢, 🟡, 🔴) for tiered investigation workflows.
* **📝 Advanced Reporting:** Triage entities (Clean, Suspicious, Malicious), add custom notes, and generate highly configurable, defanged text reports for your case files.
* **💾 Portability:** Export your Custom Sources, Settings, Favorites, and Presets to JSON text for easy backup or sharing across air-gapped workstations.
* **🌙 UI Customization:** Includes native Dark/Light modes and customizable layout pane sizing.

## 📊 Supported Indicators

| Indicator | Support | Example |
| :--- | :--- | :--- |
| **IPv4 / IPv6** | ✅ | `1[.]1[.]1[.]1`, `2606[:]4700...` |
| **Domains** | ✅ | `example[.]com` |
| **URLs** | ✅ | `hxxps[://]example[.]com/path` |
| **Hashes** | ✅ | `MD5`, `SHA-1`, `SHA-256` |

## 🚀 Usage

### Option 1: Live Web App (GitHub Pages)
Visit the live deployment via GitHub Pages. Link 🠊 [jhatzimalis.github.io/TotalOSINT](https://jhatzimalis.github.io/TotalOSINT)

### Option 2: Local / Air-Gapped (Recommended)
TotalOSINT is a static, zero-dependency web application. It runs entirely offline.
1. Download the latest `index.html` file.
2. Open `index.html` in any modern web browser (Chrome, Firefox, Edge, Safari).

## 🛠️ Configuration & Customization

TotalOSINT is designed to adapt to your specific workflow. Click the **Settings (⚙️)** icon in the top right to access backups and theme controls.

### 1. Adding Custom Sources
Click the **Edit Sources (✏️)** button in the Sources pane to enter Edit Mode. Click "Add Custom Source" to input your own internal or external tools.
* **Name:** Display name (e.g., `Internal Splunk`).
* **Home URL:** The base URL of the tool.
* **Lookup URL (Optional):** The URL used to execute a search. TotalOSINT appends the extracted entity to the end of this URL. 
  * *Example:* `hxxps[://]intel-db[.]local/search?q=`

### 2. Presets & Favorites
While in **Edit Mode (✏️)**, you can configure your toolset:
* Click the **Heart (💙)** to pin a tool to the top of your list.
* Click the **Preset Dots** to map a tool to Preset 1 (Green), Preset 2 (Yellow), or Preset 3 (Red). 

### 3. Hardcoding Sources (For Self-Hosted Deployments)
If you are deploying TotalOSINT for a team and want to permanently embed default internal tools, simply open `index.html` in a text editor, locate the `const sources = { ... }` block, and add your endpoints directly to the JavaScript object.

## 🔒 Security & Privacy

* **Client-Side Execution:** All logic runs locally in your browser context. Data extraction (RegEx) occurs entirely on your machine.
* **No Tracking:** No analytics, no cookies, no external fonts, and no API calls.
* **Fail-Safe Design:** Raw inputs are **not** stored in LocalStorage. If your browser crashes or the tab is closed, the data is permanently wiped from memory.
* **Global Defanging:** A built-in "Defang" toggle automatically neuters indicators (`1[.]1[.]1[.]1`, `hxxp[://]`) in the UI, clipboard copies, and generated reports to prevent accidental clicks.

## 🏷️ Tags

`osint` `threat-intelligence` `cybersecurity` `soc` `blue-team` `incident-response` `investigation` `ioc-extraction` `opsec` `malware-analysis` `security-tools` `infosec` `digital-forensics` `threat-hunting` `ioc-parser` `ioc-lookup` `reconnaissance` `client-side` `zero-persistence` `secops`

---

*Disclaimer: TotalOSINT is a tool for aggregation and workflow optimization. The author is not responsible for how the linked third-party services are used or the results they provide.*
