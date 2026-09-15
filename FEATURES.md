# Arova features

**English** | [简体中文](FEATURES.zh-CN.md)

Applies to the current public beta. Updated: 2026-09-15.

[Download](https://github.com/spencer17x/arova-releases/releases) · [User guide](USAGE.md) · [Home](README.md)

Arova brings activity from Fomo, Pump, and other configured sources to trading pages, with browser and Telegram alerts to help you recognize followed accounts, inspect associated tokens, and return to the original content.

## Platforms and activity

The panel appears on supported **XXYY, GMGN, and DeBot** trading pages. Account and notification settings live in the extension's standalone settings page.

| View | Content | Purpose |
| --- | --- | --- |
| Following | Fomo Alerts, Pump Friends, and configured Telegram inbound messages | Track activity associated with connected accounts' follows |
| Platform activity | Fomo Feed and Pump platform home-feed activity | Browse platform-wide information; this is not a personal following list |
| Pump Top | Rankings supplied by Pump | View the platform leaderboard; this is not an Arova score |

Data comes from third-party platforms. Authorization, provider responses, and network conditions affect availability. Arova does not guarantee complete history or instant delivery of every message.

## Main capabilities

| Feature | What it does |
| --- | --- |
| English and Chinese | Interface follows the browser, with a manual English / Simplified Chinese choice; each Telegram destination chooses its own language |
| Standalone settings | Manage sign-in identities, connections, notifications, watchlists, display preferences, and themes |
| Sign-in and linking | Email/password, Google, Telegram, Solana wallet, and EVM wallet entry points; availability depends on the service configuration |
| Fomo / Pump connections | Connect, pause, or revoke each provider separately; status and follow-up inputs appear in that provider's section |
| Renewal | Choose browser or server renewal and inspect status / expiry; Fomo can fill session fields from a selected website tab after confirmation, with separate consent before server custody |
| Account notes | Read actual follows, search platform accounts and their follow status, add private notes, and open user profiles |
| Notification panel | Filter by source, view, and current token; open originals, copy contracts, and open trading pages |
| Quick switches | Toggle browser alerts, the Telegram master switch, and the token info card from the panel |
| Telegram destinations | Configure sources, categories, note visibility, and language per group / channel; save and test independently |
| Watchlist | Maintain tokens by chain and contract; received activity still depends on provider access and notification rules |
| Appearance and device preferences | Themes, panel visibility and size, and per-site position memory |
| Plans and access | View access, available plans, and orders; when paid access is enabled, pay through a separate checkout page |

Account lists and notes default to **10 rows per page**, with 10 / 20 / 50 / 100 options. Order history uses 10 rows per page.

## Settings have different scopes

| Setting | Scope |
| --- | --- |
| Panel visibility, theme, position, token card, interface language | Display on this browser; closing the panel does not stop server monitoring or Telegram alerts |
| Browser alerts | Desktop notifications, subject to Chrome and operating system permissions |
| Telegram destination rules and language | Content sent to that group / channel, independent of panel filters and browser alerts |

Notes belong to the current Arova user and do not change platform names or follow relationships. Each Telegram destination can show or hide them. Changes do not rewrite previously sent messages. Source posts, names, notes, token names, and administrator-written plan descriptions retain their original language.

## Service access

**Plans & access** shows free mode, expiry, permanent access, or suspension. Operators can grant time or unlimited access. Payments and manual grants are reflected by the server.

No purchase is needed while access is free. Prices, durations, networks, and stablecoins depend on available plans and checkout. Payment cannot start without an available plan. Permanent access has no expiry but can still be changed or suspended by a super administrator.

The user's extension settings page is separate from the internal administration console. Buying a plan or receiving permanent access does not grant administrator permissions.

## Scope and authorization boundaries

- This version provides monitoring and alerts, not automated buying / selling, swaps, copy trading, or an Arova Alpha Score / backtest.
- Platform activity, opinions, and rankings are not promises of returns. Consider the timestamp, source, and original content.
- Arova wallet sign-in proves identity. It is separate from Pump server key custody.
- Server renewal is experimental. Fomo long-lived sessions and full Pump Solana private keys are not read-only access. Read [Renewal methods](USAGE.md#renewal-methods) first.
- This public repository distributes official builds and documentation. Application source remains private; see [LICENSE](LICENSE).
