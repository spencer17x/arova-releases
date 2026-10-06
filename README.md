# Arova Chrome downloads

**English** | [简体中文](README.zh-CN.md)

[Download releases](https://github.com/spencer17x/arova-releases/releases) · [Features](FEATURES.md) · [User guide](USAGE.md)

This repository distributes official compiled Arova Chrome packages, checksums and release metadata. Application source and private development history are not included.

Arova combines public GigaX discovery with private, address-based wallet monitoring. The website and Chrome extension share account data. The extension displays notifications on supported XXYY, GMGN and DeBot pages; account, wallet and notification settings are managed separately. Arova manages monitoring RPC nodes. Free accounts have 10 active-address slots; multi-chain monitoring of the same address uses one slot, and pausing releases it.

The current client replaces the former Fomo/Pump connection workflow with wallet addresses. It does not require Fomo/Pump sessions or private keys. Legacy platform feeds, Pump Top and Arova smart-wallet/resonance signals are retired.

## Install or update

1. Download `arova-chrome-VERSION.zip` from Releases and extract it to a permanent folder.
2. Open `chrome://extensions` and enable **Developer mode**.
3. For a first install, choose **Load unpacked** and select the folder containing `manifest.json`.
4. For an update, replace the contents of the original folder, click **Reload**, then refresh trading pages. Keep the existing extension installed to retain browser settings.
5. Click the Arova toolbar icon, sign in, and add wallet addresses and notification destinations.

GitHub ZIP packages do not update automatically. Install the extension ZIP, not GitHub's **Source code** archive. Beta versions remain prereleases; use the specific release page rather than relying on GitHub's Latest shortcut.

## Release contents

- `arova-chrome-VERSION.zip`: extension package, including proprietary and third-party notices.
- `SHA256SUMS`: package checksum.
- `release-info.json`: version, build commit, production API, extension ID and checksum.

Fixed extension ID: `gedflalfmklfccgaabdbcnjjchlfemfo`. Production API: `https://api.arova.top`.

Public tags are isolated distribution snapshots. Automatic Source code archives contain public documentation and distribution artifacts, not the private application repository. Compiled JavaScript needed by the extension is included in the extension package.

## Scope and license

Arova provides monitoring and alerts, not automatic trading or guaranteed investment returns. Missing RPC history, unsupported routes and uncertain cross-chain ownership can reduce coverage. See the [user guide](USAGE.md).

Arova uses a proprietary commercial license; see [LICENSE](LICENSE). Third-party notices remain in `THIRD_PARTY_NOTICES.txt`. Public downloads do not make the application open source. Plans and account access are controlled by the server.

Memberships: Free includes 10 active wallets; Plus includes 100 ($29/month or $290/year); Pro includes 300 ($79/month or $790/year). All accounts follow the same rules. Automatic 100-wallet signup gifts and trials have ended; purchased memberships and individual administrator gifts retain their terms. Excess wallets are paused with addresses, notes and history retained. Purchases remain disabled. When enabled, subscription payments accept only native Circle USDC on Solana, with manual renewal and SOL for network fees. Memberships use calendar months/years; annual forwarding allowances reset monthly. Unlimit removes plan quotas through an explicit account grant: [contact thugz on Telegram](https://t.me/thugz1) or [X](https://x.com/thugz001). Account isolation, suspension and platform/provider rate limits still apply.

GigaX cards and notifications omit the price row; market cap, growth, contract and original provider text remain available.
