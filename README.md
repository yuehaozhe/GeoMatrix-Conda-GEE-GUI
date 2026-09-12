<!-- 标题 -->
# GeoMatrix Studio: Visual Management GUI for Conda, GCP & Google Earth Engine
> **A system-friendly, privacy-first macOS desktop client engineered to streamline Python Conda environments and Earth Engine workflows for geoscientists.**
<!-- 徽章区域 -->
[![VirusTotal](https://img.shields.io/badge/VirusTotal-0%2F73%20Clean-brightgreen)](https://www.virustotal.com/gui/file/286fbd6faa469c84e13ffbdac13474b7c694b09a0f849ad9e845d4fbe1798f75/detection)
![Telemetry](https://img.shields.io/badge/Telemetry-Zero%20Tracking-blueviolet)
![Local-First](https://img.shields.io/badge/Architecture-Local--First-success)
![Windows](https://img.shields.io/badge/Windows-x64-0078D6?logo=windows&logoColor=white)
![macOS](https://img.shields.io/badge/macOS-Apple%20Silicon%20%26%20Intel-000000?logo=apple&logoColor=white)

<!-- 官网 + 社交媒体 -->
## Want to learn more or chat with us?
[![Website](https://img.shields.io/badge/Website-geomatrix.dev-2563eb)](https://geomatrix.dev)
[![X](https://img.shields.io/badge/X-@GeoMatrix__Dev-000000?logo=x&logoColor=white)](https://x.com/GeoMatrix_Dev)
[![Email](https://img.shields.io/badge/Email-contact%40geomatrix.dev-EA4335)](mailto:contact@geomatrix.dev)

<!-- 图片 -->
![GeoMatrix Studio](assets/welcome.png)

<!-- 特点 -->
## I. Visual Preview & 6 Core Features
Discover how GeoMatrix Studio transforms the cumbersome and inefficient management of Conda environments and GCP projects into an elegant and efficient engineering experience.

### A. Conda Visual Management
> **Encapsulate the lightning-fast Micromamba package management kernel within a pure, uncontaminated graphical sandbox.**

| Dimension | Traditional Conda CLI / Anaconda Navigator | 🚀**GeoMatrix Studio (Micromamba Sandbox)** |
| --- | --- | --- |
| 🛠️ System Invasiveness | ⚠️Automatically overwrites the global PATH, which can easily cause conflicts between multiple Python versions | ✅Fully sandboxed, uses temporary environment variables, leaving no trace on the system |
| 🧹 Installation and Cleanup | ❌Uninstallation leaves behind large amounts of cache, configuration files, and unused packages | ✨Folder-level data locking; one-click complete destruction leaves no junk files |
| 👁️ Package Information Awareness | ⚠️Command line displays only package names and versions; difficult to track size and licenses | ✅Visualized panoramic analysis provides an intuitive overview of the size and license of each dependency |
| ⚡ User Experience | ❌High learning curve for the command line; Navigator launches slowly and is laggy | ✨Minimalist, modern UI with millisecond-level responsiveness; no need to memorize any terminal parameters |
<!-- 图片 -->
![Conda Visual Management](assets/conda.png)


<!-- 二、Conda环境内管理包及包模版 -->
### B. Package Management & Environment Templates
> **Intelligently matches dependencies from both PyPI and Conda, enabling seamless team collaboration and the reproduction of research results with a single click.**

| Dimension | Traditional Command Line (CLI) / Traditional Tools | 🚀GeoMatrix Studio (Package & Template Engine) |
| --- | --- | --- |
| 🔒 Channel Management | ⚠️Mixing Default, Anaconda, and Conda-forge channels can easily lead to environment failures | ✅ Lock down Conda-forge to ensure package version compatibility and security at the source |
| 🔀 Mixing PyPI & Conda | ❌Prone to corrupting the Conda dependency tree (e.g., when pip overwrites Conda libraries) | ✨ Intelligent Diff isolation mechanism that elegantly parses and installs both types of dependencies in parallel |
| ⚡Operational Efficiency | ❌ Requires entering each entry individually or manually editing complex `environment.yml` files | ✨Visual batch addition with built-in smart search and one-click batch injection |
| 🔬Team Collaboration and Reproducibility | ⚠️ Exported YAML files often contain local absolute paths or system-specific binaries, making remote reproduction prone to errors | ✅ Standardized, lightweight template export ensures 100% reproducibility of research results and code across different devices |

![Package Management & Environment Templates](assets/package.png)



<!-- 三、针对实验室和课题组的功能 -->
### C. Designed specifically for laboratories and research groups
> **Maintain a consistent environment so that reproducibility is no longer a challenge, and focus on the research itself rather than tedious environment configuration.**

| Dimension | Traditional Lab Collaboration Methods | 🚀 GeoMatrix Studio (Lab Workflow) |
| --- | --- | --- |
|💻 Changing Development Devices |❌ Re-fetch all packages; often encounter issues where older package versions have been discontinued or compilation fails | ✨ One-click export of an offline device-swap package; instantly restore the entire environment offline |
| 👥 Adding New Members to the Group | ⚠️ Manually running `install` commands line by line according to documentation, taking several days and prone to errors | ✅ Import a standardized environment package template to align the group’s development environment in seconds |
| ☁️ HPC / On-Premises Deployment (Future Plans) | ❌ Severe disconnect between local Windows/Mac and remote Linux HPC dependency environments | ✨ One-click synchronization from local to cluster (Roadmap), ensuring seamless migration of computing power |gee

![C. Designed specifically for laboratories and research groups](assets/export.png)

<!-- 四、针对Windwos操作系统的创新性架构设计 -->
### D. Innovative Architectural Design for the Windows Operating System
> **The innovative Hybrid Sandbox architecture lets you seamlessly set up AI training infrastructure in a native Windows environment.**

| Dimension | Traditional Windows Native Configuration | WSL2 / Docker Virtualization Solution | 🚀GeoMatrix Studio (Hybrid Sandbox) |
| --- | --- | --- | --- |
| 🛡️Dependency Deadlocks & DLL Conflicts |❌ Extremely frequent (GDAL and PyTorch C++ libraries often overwrite each other) | ⚠️Avoided through Linux isolation, but path and file mapping is extremely cumbersome | ✨ Underlying sandbox isolation fundamentally isolates C++ and CUDA dependencies |
|⚡Computing Power and Performance Loss | ⚠️Native zero loss, but the environment is extremely fragile | ❌ Hyper-V virtual machine overhead, GPU virtualization loss, and I/O bottlenecks exist | ✅ Native zero loss, 100% direct connection to local GPU and file system |
| ⚙️Configuration Complexity | ❌ Requires manual configuration of complex PATH settings and CUDA drivers | ⚠️ Requires installing WSL, configuring the Linux subsystem, and setting up Docker mounts | ✨ Graphical, one-click deployment with no need to modify system-level environment variables |



<!-- 五、GCP的极简化管理 -->
### E. Streamlined GCP & Earth Engine Management
> **Consolidate GCP initialization, multi-tab task monitoring, and cloud billing analytics into a single responsive workstation.**

| Dimension | Google Official Web Console | 🚀 GeoMatrix Studio (GCP Dashboard) |
| --- | --- | --- |
| ⚙️GCP Basic Configuration | ⚠️ Requires repeatedly switching between multiple web pages, such as IAM, API libraries, and Billing | ✨ End-to-end integration in a single form; complete GEE authentication and API activation with one click |
| 📊 Task Progress Monitoring | ❌ Consumes a significant amount of browser memory; switching back and forth between multiple tabs is extremely inefficient | ✅ Unified single-screen monitoring with millisecond-level, lightweight responses that completely free up system memory |
| 🔔 Task Completion Alerts | ❌ No system-level or audio alerts; requires manual, repeated page refreshes, causing anxiety | ✨ Intelligent audio effects and notifications; instant voice or sound alerts for task success or failure |
| 💾 Log Persistence | ⚠️ Official logs are retained for only 10 days; records are lost after expiration and cannot be traced | ✅ Built-in high-performance SQLite database for permanent local storage of the full task history |
| 💳 Quota and Cost Statistics | ❌ Severe billing delays make it difficult to intuitively understand how much of the quota the current research group has consumed | ✨ Four-tier visual cost dashboard for real-time control over cumulative consumption and remaining quota |

![GEE_information](assets/gee_1.png)

![GEE_Task_List](assets/gee_2.png)

![GEE_EECU_Quota](assets/gee_3.png)

<!-- 六、高性能与本地优先架构与充分的隐私保护 -->
### F. High-Performance Local-First Architecture & Zero-Trust Privacy
> **Redefining the limits of performance with the Tauri 2 engine and a local-first architecture, we build end-to-end communication with zero relays and zero tracking to safeguard the privacy of research data.**

| Dimension | Traditional Web/Electron Framework Software | 🚀 GeoMatrix Studio (Tauri 2 Local-First) |
| --- | --- | --- |
| 🏗️Underlying Architecture | ⚠️ Heavyweight Chromium + Node.js | ✨ Tauri 2 + Rust native engine, directly calling the system’s native rendering layer |
| ⚡Resource Consumption | ❌ High memory usage (often several GB), installation package is several hundred MB | ✅ Extremely low memory usage, lightweight installation package (tens of MB), ultra-fast startup in milliseconds |
| 🌐 Network Communication | ❌ Data must be routed through and parsed by the vendor’s developer servers | ✨ Local-first direct connection, end-to-end communication only with Google and Conda’s official servers |
| 🔒 Data Security & Privacy | ⚠️ Generally includes behavioral tracking, data reporting, and user tracking | ✅ Zero tracking, zero reporting; all network endpoints are publicly disclosed; supports full packet capture auditing |

![Launch_Latency](assets/Launch_Latency.png)
![GEE_EECU_Quota](assets/Memory_Footprint.png)
![GEE_EECU_Quota](assets/Package_Footprint.png)
![GEE_EECU_Quota](assets/privacy.png)

<!-- 快速开始 -->
## II. Quick Start
We have launched a free beta test, and we invite everyone to download and try it out! You can download it using the link below, or via our **official website** or **GitHub Releases**.
| Platform | Architecture | Get started |
| --- | --- | --- |
| Windows | x64 | [Join Windows beta](https://tally.so/r/ja8LqJ) |
| macOS | Apple Silicon (M series) | [Join macOS beta](https://tally.so/r/ja8LqJ) |
| macOS | Intel | [Join macOS beta](https://tally.so/r/ja8LqJ) |


<!-- FAQ -->
## III. FAQ

### A. Why does Windows SmartScreen warn me during installation?

GeoMatrix Studio is still in independent development and early beta. We have not yet completed Microsoft’s costly enterprise EV code-signing certificate. A formal Microsoft Store release is planned for the stable launch.

- **Security commitment:** GeoMatrix Studio is fully aligned with open-source and local-first principles. There is no malware and no hidden behavior.
- **Apple already verified:** The macOS build is signed and notarized through the official Apple Developer Program.
- **Transparent network audit:** Windows users can inspect all outbound traffic with tools such as Wireshark or Fiddler. You can safely dismiss the SmartScreen warning and continue installing.

### B. Is the beta free?

Yes — completely free. All core features during the beta are available at no cost, with no hidden charges.

### C. What benefits do beta testers get?

- **Early-bird lifetime discount:** Users who join the beta and share feedback will receive an Early-Bird offer at the official release — a low-priced one-time purchase.
- **Contributor lifetime license:** Contributors who submit constructive issues, PRs, feature suggestions, or useful bug reports may receive a lifetime free license, including all future major updates.

### D. How can I share feedback or suggestions?

| Channel | Get started |
| --- | --- |
| GitHub Issues | [Open an issue](https://github.com/yuehaozhe/GeoMatrix-Conda-GEE-GUI/issues) |
| In-app Feedback | Use the Feedback panel inside GeoMatrix Studio |
| X (Twitter) | [@GeoMatrix_Dev](https://x.com/GeoMatrix_Dev) |
| Email | [contact@geomatrix.dev](mailto:contact@geomatrix.dev) |
| Website | [geomatrix.dev](https://geomatrix.dev) |

