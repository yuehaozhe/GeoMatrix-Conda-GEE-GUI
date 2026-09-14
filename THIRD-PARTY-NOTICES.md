# Third-Party Notices

GeoMatrix Studio (closed beta) incorporates open-source and third-party software.
This notice lists **direct runtime dependencies** of the desktop app, plus **notable
bundled or separately downloaded** components. Transitive crates and npm packages
are omitted unless they carry attribution-sensitive terms (for example MPL-2.0)
or are material to the product (SQLite, TLS).

Unless otherwise noted, licenses are as declared by the upstream projects at the
versions used in GeoMatrix Studio `0.3.0-beta.3`. Full license texts are available from
the linked repositories and from the dependency trees in the GeoMatrix Studio source
(`package.json` / `pnpm-lock.yaml`, `src-tauri/Cargo.toml` / `Cargo.lock`).

User-installed Conda / PyPI / PyTorch packages are **not** part of GeoMatrix Studio
itself; they keep their own licenses between you and those package authors.

---

## 1. Frontend (Vue / npm — production)

| Component | Version (approx.) | License | Homepage |
| --- | --- | --- | --- |
| Vue | 3.5.x | MIT | https://github.com/vuejs/core |
| vue-i18n | 11.4.x | MIT | https://github.com/intlify/vue-i18n |
| @lucide/vue | 1.25.x | ISC | https://github.com/lucide-icons/lucide |
| canvas-confetti | 1.9.x | ISC | https://github.com/catdad/canvas-confetti |
| echarts | 6.1.x | Apache-2.0 | https://github.com/apache/echarts |
| zrender *(via ECharts)* | — | BSD-3-Clause | https://github.com/ecomfe/zrender |
| nanoid | 6.0.x | MIT | https://github.com/ai/nanoid |
| @tauri-apps/api | 2.x | Apache-2.0 OR MIT | https://github.com/tauri-apps/tauri |
| @tauri-apps/plugin-log | 2.9.x | MIT OR Apache-2.0 | https://github.com/tauri-apps/plugins-workspace |
| @tauri-apps/plugin-notification | 2.3.x | MIT OR Apache-2.0 | https://github.com/tauri-apps/plugins-workspace |
| @tauri-apps/plugin-opener | 2.x | MIT OR Apache-2.0 | https://github.com/tauri-apps/plugins-workspace |
| @tauri-apps/plugin-process | 2.3.x | MIT OR Apache-2.0 | https://github.com/tauri-apps/plugins-workspace |
| @tauri-apps/plugin-updater | 2.10.x | MIT OR Apache-2.0 | https://github.com/tauri-apps/plugins-workspace |

Build-time / test-only npm tools (Vite, Vitest, `@tauri-apps/cli`, Sharp, etc.)
are used to produce the app and are **not** redistributed as application runtime
dependencies.

---

## 2. Desktop shell & Rust (Tauri 2)

| Component | Version (approx.) | License | Homepage |
| --- | --- | --- | --- |
| tauri | 2.11.x | Apache-2.0 OR MIT | https://github.com/tauri-apps/tauri |
| tauri-build | 2.6.x | Apache-2.0 OR MIT | https://github.com/tauri-apps/tauri |
| tauri-plugin-log | 2.9.x | Apache-2.0 OR MIT | https://github.com/tauri-apps/plugins-workspace |
| tauri-plugin-notification | 2.3.x | Apache-2.0 OR MIT | https://github.com/tauri-apps/plugins-workspace |
| tauri-plugin-opener | 2.5.x | Apache-2.0 OR MIT | https://github.com/tauri-apps/plugins-workspace |
| tauri-plugin-process | 2.3.x | Apache-2.0 OR MIT | https://github.com/tauri-apps/plugins-workspace |
| tauri-plugin-updater | 2.10.x | Apache-2.0 OR MIT | https://github.com/tauri-apps/plugins-workspace |
| tauri-plugin-single-instance | 2.4.x | Apache-2.0 OR MIT | https://github.com/tauri-apps/plugins-workspace |
| wry *(webview)* | 0.55.x | Apache-2.0 OR MIT | https://github.com/tauri-apps/wry |
| tao *(window)* | 0.35.x | Apache-2.0 | https://github.com/tauri-apps/tao |
| tokio | 1.53.x | MIT | https://github.com/tokio-rs/tokio |
| serde / serde_json | 1.x | MIT OR Apache-2.0 | https://github.com/serde-rs/serde |
| reqwest *(rustls-tls)* | 0.12.x | MIT OR Apache-2.0 | https://github.com/seanmonstar/reqwest |
| rusqlite *(bundled SQLite)* | 0.32.x | MIT | https://github.com/rusqlite/rusqlite |
| zip | 2.4.x | MIT | https://github.com/zip-rs/zip2 |
| thiserror | 1.x | MIT OR Apache-2.0 | https://github.com/dtolnay/thiserror |
| log | 0.4.x | MIT OR Apache-2.0 | https://github.com/rust-lang/log |
| tempfile | 3.x | MIT OR Apache-2.0 | https://github.com/Stebalien/tempfile |
| libc | 0.2.x | MIT OR Apache-2.0 | https://github.com/rust-lang/libc |
| base64 | 0.22.x | MIT OR Apache-2.0 | https://github.com/marshallpierce/rust-base64 |
| hex | 0.4.x | MIT OR Apache-2.0 | https://github.com/KokaKiwi/rust-hex |
| sha2 | 0.10.x | MIT OR Apache-2.0 | https://github.com/RustCrypto/hashes |
| ed25519-dalek | 2.x | BSD-3-Clause | https://github.com/dalek-cryptography/ed25519-dalek |
| specta / tauri-specta / specta-typescript | 2.0.0-rc.25 / 0.0.12 | MIT | https://github.com/specta-rs/specta |
| notify-rust *(macOS)* | 4.18.x | MIT OR Apache-2.0 | https://github.com/hoodie/notify-rust |
| windows *(Windows)* | 0.61.x | MIT OR Apache-2.0 | https://github.com/microsoft/windows-rs |

Platform webviews used by Tauri (WebKit / WebView2 / WebKitGTK) are provided by
the host OS or platform SDKs and remain subject to their respective terms.

---

## 3. Notable bundled / transitive components

| Component | Role | License | Notes |
| --- | --- | --- | --- |
| SQLite | Local task / app DB via `rusqlite` `bundled` | Public domain (SQLite blessing) | https://www.sqlite.org/copyright.html |
| rustls / ring | HTTPS (updater, downloads) | Apache-2.0 OR ISC OR MIT / Apache-2.0 AND ISC | No OpenSSL runtime dependency in the default TLS stack |
| webpki-roots | TLS trust anchors | CDLA-Permissive-2.0 | https://github.com/rustls/webpki-roots |
| ICU4X data crates | Unicode / i18n support in the Rust tree | Unicode-3.0 | https://github.com/unicode-org/icu4x |
| cssparser / selectors *(via Tauri stack)* | CSS parsing | MPL-2.0 | Source available from Mozilla / Servo upstreams |
| option-ext / dtoa-short | Small helpers in the tree | MPL-2.0 | See crates.io for source |

MPL-2.0 components are used in binary form as part of the dependency graph.
Corresponding source is available from the upstream projects named above and from
crates.io / the Cargo.lock pins used to build GeoMatrix Studio.

---

## 4. Separately downloaded tools (first-run / user machine)

These are **not** compiled into the GeoMatrix Studio binary. The app may download and
install them into the application data directory during setup or when you enable
related features. Their licenses and terms apply between you and the upstream
vendor.

| Component | Typical use in GeoMatrix Studio | License / terms | Source |
| --- | --- | --- | --- |
| Micromamba | Sandboxed Conda/Mamba package manager | BSD-3-Clause (upstream); redistributed builds may include additional MIT / OpenSSL notices | https://github.com/mamba-org/mamba — downloads via https://micro.mamba.pm |
| Google Cloud CLI / SDK (`gcloud`) | GCP project setup & Earth Engine workflows | Google Cloud SDK / Google Terms of Service (contains proprietary and open-source components) | https://cloud.google.com/sdk — downloads via Google Cloud CLI channels |

Packages you later install with Micromamba from Conda-Forge, PyPI, PyTorch, or
other channels are third-party software under **their** licenses; GeoMatrix Studio does
not relicense them.

Google Earth Engine / GCP APIs are cloud services. Using them is subject to
Google’s product terms and quotas; GeoMatrix Studio does not relay your research traffic
through a GeoMatrix Studio server (see `PRIVACY.md`).

---

## 5. Common license summaries (informational)

This section is a convenience summary only. The authoritative text is the
upstream license.

### MIT License (summary)

Permission is granted, free of charge, to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the software, subject to including
the copyright and permission notice. THE SOFTWARE IS PROVIDED “AS IS”, WITHOUT
WARRANTY OF ANY KIND.

### Apache License 2.0 (summary)

A permissive license with an express patent grant and NOTICE-file requirements.
You must retain copyright, patent, trademark, and attribution notices, and state
significant changes. See https://www.apache.org/licenses/LICENSE-2.0

### BSD-3-Clause (summary)

Redistribution in source and binary forms is permitted with copyright notice,
conditions, and disclaimer retained; the name of the copyright holder may not be
used to endorse derived products without permission.

### ISC (summary)

Similar in effect to a simplified MIT / 2-clause BSD style permissive license.

### MPL-2.0 (summary)

A weak copyleft license: modifications to MPL-covered files must remain under
MPL-2.0; larger works may combine with other licenses under the MPL terms.
See https://www.mozilla.org/MPL/2.0/

### SQLite blessing

SQLite is dedicated to the public domain (where recognized) / provided under the
SQLite blessing. See https://www.sqlite.org/copyright.html

---

## 6. Contact

Questions about this notice: [contact@geomatrix.dev](mailto:contact@geomatrix.dev)

Related documents:

- [Privacy Policy](./PRIVACY.md)
- [Closed Beta Terms](./TERMS.md)
