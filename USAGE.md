# Arova user guide

[Illustrated Fomo wallet monitoring guide](https://arova.top/#guide) — includes wallet setup, allowances and troubleshooting. No RPC setup, platform login session or private key is needed.

**English** | [简体中文](USAGE.zh-CN.md)

Updated: 2026-10-05. Applies to beta.3 and the compatible service.

[Download](https://github.com/spencer17x/arova-releases/releases) · [Features](FEATURES.md) · [Home](README.md)

## Installation and updates

Download the extension ZIP, extract it, and load the folder containing `manifest.json` through **Load unpacked** in `chrome://extensions` with Developer mode enabled. To update, replace the contents of the original folder, reload Arova, and refresh trading pages. Do not uninstall first if you want to retain local settings. GitHub packages do not update automatically.

Use `SHA256SUMS` and `release-info.json` to verify the downloaded package and build. The Source code archives are not installation packages.

## Quick start

1. Open Arova settings from the Chrome toolbar and sign in or register.
2. In wallet monitoring, add an actual wallet address and optional private note.
3. Choose the compatible chains and operation types. Start with a small set you can verify.
4. Check monitoring status and your active-wallet allowance; Arova manages the nodes.
5. Open a supported XXYY, GMGN or DeBot page and enable the notification panel.
6. Configure browser alerts or Telegram destinations separately if needed.

Wallet monitoring does not require a Fomo/Pump login session or private key. A token contract or platform account ID is not a substitute for a wallet address. Existing legacy authorization materials, if present, have a separate explicit cleanup control in account settings; updating the extension does not automatically revoke them.

## Wallets, allowances and transaction types

Accounts start with 100 active-address slots. One address across multiple chains uses one slot; pausing releases it. The initial allowance currently has no end date, which is not a promise of permanent free access. Check your account for its allowance and expiry. Old private RPC credentials remain encrypted until you explicitly clear them in account settings.

A wallet can monitor one or more compatible networks. Enable or pause each record independently. Private notes belong to your Arova account. Saved operation filters determine which events enter your wallet activity and notifications.

Monitoring starts from its configured boundary, not from the wallet's entire history. RPC outages, quotas and unavailable historical blocks can leave gaps; check the displayed state instead of assuming complete coverage. Node recovery does not guarantee that all gaps can be filled.

A route that sends a token to a wallet is not sufficient proof of a buy. If the service cannot establish owner execution or source ownership, it records an incoming transfer. To see those receipts, include incoming transfers in the wallet's operation selection and the relevant Telegram transfer categories. They should not be interpreted as verified buys.

Token names remain unchanged by translation. Cached values are estimates, not proof of executed spend or proceeds. Open the transaction link when checking a particular notification.

## Telegram alerts

Create a destination, enter its Chat ID and label, select its rules and language, then save that destination. The notification bot needs permission to send to the destination. Saving does not send a test. After saving, use the separate test button and check Telegram before retrying an uncertain result.

Check both the main notification switch and the destination's enabled state. Each target's rules, note visibility and language are independent. Panel filters do not replace Telegram rules. Disabling automatic notifications preserves saved target settings; existing messages are not changed or replayed.

## Trend monitors and Telegram forwarding

Use the dedicated settings to configure trend monitors or forwarding rules. Select supported chains individually or together. XXYY trend and multiple messages keep their original Chinese format even when the interface is English.

Forwarding uses a Telegram account login with API ID/API Hash and the required login steps; the notification Bot has separate settings. Follow the current page's instructions, review credential handling, and enter sensitive values only in the intended form. Saved fields are masked; reveal supported fields only when necessary. The session, login code and two-step password are not exportable through reveal controls.

Review the selected monitor before confirming deletion. Removing a monitor affects that monitor and its rules; it does not grant access to another account's settings.

## Language, sound and display

The interface follows the browser language by default and supports a local English/Simplified Chinese override. Each Telegram target saves its own language. Source text, token names and private notes are not translated; XXYY trend messages retain their original format.

Configure sound and custom audio in preferences. Closing the panel, closing Chrome, or signing out does not by itself revoke server-side monitoring or stored credentials. Use the relevant monitoring or account controls.

## Plans and access

Check the account's current access and available plans in settings. Orders freeze wallet capacity and duration. Same-tier periods extend sequentially; different tiers run independently. If capacity expires, the oldest addresses within the allowance remain enabled and excess addresses pause. History and notes remain; re-enable wallets after renewal. Prices, duration, payment options and eligibility are determined by the service. No payment is required while free access applies. A plan does not grant internal administrator access. This guide does not authorize trades or custody of wallet private keys.

## Troubleshooting

| Problem | Check |
| --- | --- |
| Old interface | Replace the original folder, reload the extension and refresh trading pages |
| Missing activity | Wallet enabled state, selected networks/operations, monitoring boundary, RPC status and account access |
| Missing buy alert for a cross-chain receipt | It may be classified as an incoming transfer because ownership is unverified |
| No panel | Supported page, panel visibility, extension site permissions and page reload |
| No browser alert | Browser/device alert settings and operating system permissions |
| No Telegram alert | Main switch, target enabled state, categories, bot permissions and monitoring boundary |
| Test unavailable | Save the destination first and wait for the draft/save operation to finish |
| Uncertain delivery | Check the actual Telegram destination before retrying |

When reporting a problem, include the release/build, time, chain and a transaction link where relevant. Redact credentials, private notes, group identifiers and unrelated account data. Never send passwords, keys, cookies or login codes.

Earlier screenshot assets in this repository depict older clients, including retired authorization flows. They are retained as historical assets and are not instructions for beta.3.
