# Arova user guide

[Online Arova user guide](https://arova.top/#guide) — includes sign-in, wallets, plans, payments and troubleshooting. No RPC setup, platform login session or private key is needed.

**English** | [简体中文](USAGE.zh-CN.md)

Updated: 2026-10-18. Covers the current website/service and the beta.10 extension. Website updates do not automatically update the extension.

[Download](https://github.com/spencer17x/arova-releases/releases) · [Features](https://github.com/spencer17x/arova-releases/blob/main/FEATURES.md) · [Home](README.md)

## Installation and updates

Download the extension ZIP, extract it, and load the folder containing `manifest.json` through **Load unpacked** in `chrome://extensions` with Developer mode enabled. To update, replace the contents of the original folder, reload Arova, and refresh trading pages. Do not uninstall first if you want to retain local settings. GitHub packages do not update automatically.

Use `SHA256SUMS` and `release-info.json` to verify the downloaded package and build. The Source code archives are not installation packages.

## Sign-in and refresh

The website and extension share account data but store separate sign-in sessions. Signing in to the extension does not sign you in to the website. On refresh, the website verifies the session before showing the page, then loads account settings separately. Use Reconnect for network errors and Retry for settings errors; sign in again when the session expires.

This guide covers the website and beta.10 extension, including Fomo Signals, Arova Trend, Growth tracking and current account settings. Check the release page for available downloads. Refresh or force-refresh the website for its current interface. Update extension files using the installation steps above; refreshing the website does not replace them.

## Quick start

1. Open Arova settings from the Chrome toolbar and sign in or register.
2. In wallet monitoring, add an actual wallet address and optional private note.
3. Choose the compatible chains and operation types. Start with a small set you can verify.
4. Check monitoring status and your active-wallet allowance; Arova manages the nodes.
5. Open a supported XXYY, GMGN or DeBot page and enable the notification panel.
6. Configure browser alerts or Telegram destinations separately if needed.

Wallet monitoring does not require a Fomo/Pump login session or private key. A token contract or platform account ID is not a substitute for a wallet address. Existing legacy authorization materials, if present, have a separate explicit cleanup control in account settings; updating the extension does not automatically revoke them.

Fomo Signals reception is managed by Arova. The current client does not show receiver credential controls; choose signal types and notification destinations in settings. Chain-delay notices appear only for chains where the account has a saved wallet, including a paused wallet, and polling pauses while the browser tab is hidden.

## Wallets, allowances and transaction types

Free accounts have 10 active-address slots. One address across multiple chains uses one slot; pausing releases it. Check your account for its allowance and expiry. Old private RPC credentials remain encrypted until you explicitly clear them in account settings.

A wallet can monitor one or more compatible networks. Enable or pause each record independently. Private notes belong to your Arova account. Saved operation filters determine which events enter your wallet activity and notifications.

Monitoring starts from its configured boundary, not from the wallet's entire history. RPC outages, quotas and unavailable historical blocks can leave gaps; check the displayed state instead of assuming complete coverage. Node recovery does not guarantee that all gaps can be filled.

A route that sends a token to a wallet is not sufficient proof of a buy. If the service cannot establish owner execution or source ownership, it records an incoming transfer. To see those receipts, include incoming transfers in the wallet's operation selection and the relevant Telegram transfer categories. They should not be interpreted as verified buys.

Token names remain unchanged by translation. Cached values are estimates, not proof of executed spend or proceeds. Open the transaction link when checking a particular notification.

## Telegram alerts

Create a destination, enter its Chat ID and label, select its rules and language, then save that destination. The notification bot needs permission to send to the destination. Saving does not send a test. After saving, use the separate test button and check Telegram before retrying an uncertain result.

Check both the main notification switch and the destination's enabled state. Each target's rules, note visibility and language are independent. Panel filters do not replace Telegram rules. Disabling automatic notifications preserves saved target settings; existing messages are not changed or replayed.

## Trend monitors and Telegram forwarding

**Fomo Signals** highlight smart-wallet activity and are available in public discovery. **Arova Trend** covers trend and anomaly signals for the signed-in account. **Growth tracking** shows subsequent multiple changes relative to the relevant signal baseline; it is not a realized trading return.

Use the dedicated settings to configure trend monitors or forwarding rules. Select supported chains individually or together. Arova Trend notifications use Chinese body text even when the interface is English.

Forwarding uses a Telegram account login with API ID/API Hash and the required login steps; the notification Bot has separate settings. Follow the current page's instructions, review credential handling, and enter sensitive values only in the intended form. Saved fields are masked; reveal supported fields only when necessary. The session, login code and two-step password are not exportable through reveal controls.

Review the selected monitor before confirming deletion. Removing a monitor affects that monitor and its rules; it does not grant access to another account's settings.

## Language, sound and display

The interface follows the browser language by default and supports a local English/Simplified Chinese override. Each Telegram target saves its own language. Source text, token names and private notes are not translated; Arova Trend message bodies remain in Chinese.

Configure sound and custom audio in preferences. Closing the panel, closing Chrome, or signing out does not by itself revoke server-side monitoring or stored credentials. Use the relevant monitoring or account controls.

## Plans, access and payments

Open Settings → Plans & access for your current plan, wallet usage, monthly/yearly plans and orders. All accounts follow the same rules: no registration-date exemptions, automatic 100-wallet gifts or automatic trials. Purchased memberships and individual administrator grants retain their terms.

| Tier | Default active wallets | Default price / activation |
| --- | --- | --- |
| Free | 10 | Free basic access |
| Plus | 100 | $29/month or $290/year |
| Pro | 300 | $79/month or $790/year |
| Unlimit | No plan quota | Contact for an explicit grant |

These are default plans; the plan page and frozen order determine the applicable price, limits and term. Plans that are not open for purchase can still be compared but cannot be ordered. Removed plans are hidden. A plan does not grant administrator access or access to another account's data.

The subscription-purchase switch controls only new orders and initiating payments. Closing purchases does not remove quotas, block Free features or cancel existing memberships. **Purchases are currently open.** Previously submitted payments continue to be verified; do not pay again.

New subscriptions accept only **native Circle USDC on Solana**. SOL is for network fees. Real mainnet payment acceptance has not been exercised end to end. Follow a valid order and approve the signature yourself in your wallet; do not send funds to expired orders or on another network. Transfers of other tokens or on other chains are not credited automatically. Memberships use calendar months/years with manual renewal and no automatic charges. Annual forwarding allowances reset monthly. Upgrades within the same billing interval are prorated; downgrades take effect next period.

Plus is marked as recommended. When only one payment channel is available, the plan page shows the network and stablecoin instead of a dropdown. At 7, 3 and 1 days before expiry, the page shows the remaining days, the end date and a renew action. There is no automatic email or Telegram reminder. When the wallet allowance is full, the page compares the current allowance with the next plan. Checkout keeps an insufficient-balance or network-fee warning above the pay button and shows the time left on the quote. The SOL check includes the receiving-account deposit, network fee and the paying wallet's rent-exempt minimum; if SOL is short, the pay button is disabled and the page offers a balance recheck. Once a payment is detected or confirming, there is no need to pay again. If a payment arrives after the quote expires, or the payment does not match the order, checkout says the money will not be lost and not to pay again.

Unlimit requires an explicit account grant; a username or role does not grant it automatically. Contact [thugz on Telegram](https://t.me/thugz1) or [X](https://x.com/thugz001). Security checks, account suspension and provider rate limits still apply. Revocation or expiry returns the account to its valid membership, or Free. A legacy permanent-duration grant is not an Unlimit quota grant.

One address across multiple chains uses one slot; pausing releases it. If expiry puts an account over its allowance, the earliest-added wallets within the allowance remain active and the rest pause. Addresses, notes and history remain; re-enable wallets after restoring capacity. Neither a plan nor this guide authorizes trading or custody of wallet private keys.

## Troubleshooting

| Problem | Check |
| --- | --- |
| Old interface | Refresh or force-refresh the website; for the extension, replace its folder, reload it and refresh trading pages |
| Missing activity | Wallet enabled state, selected networks/operations, monitoring boundary, RPC status and account access |
| Missing buy alert for a cross-chain receipt | It may be classified as an incoming transfer because ownership is unverified |
| No panel | Supported page, panel visibility, extension site permissions and page reload |
| No browser alert | Browser/device alert settings and operating system permissions |
| No Telegram alert | Main switch, target enabled state, categories, bot permissions and monitoring boundary |
| Test unavailable | Save the destination first and wait for the draft/save operation to finish |
| Uncertain delivery | Check the actual Telegram destination before retrying |

When reporting a problem, include the release/build, time, chain and a transaction link where relevant. Redact credentials, private notes, group identifiers and unrelated account data. Never send passwords, keys, cookies or login codes.

Earlier screenshot assets in this repository depict older clients, including retired authorization flows. They are retained as historical assets and are not instructions for beta.10.

Fomo Signals cards and notifications omit the price row; market cap, growth, contract and original provider text remain available.

Token details retain update times and cached-data indicators. Trading links keep their destination names; updating preserves saved monitoring and notification rules.


## Receiving-account creation

If the receiving account needs to be created, the paying wallet covers its SOL creation cost separately from the USDC plan amount. The pre-sign check also reserves the paying wallet's rent-exempt SOL minimum so the transaction does not fail after signing. Checkout shows an estimate before the wallet signature; review the actual cost in the wallet. Creation and payment are in one transaction, and access is granted only after the USDC payment is verified.
