# Arova features

**English** | [简体中文](FEATURES.zh-CN.md)

Updated: 2026-10-07. Covers the current website/service and the beta.6 extension.

[Download](https://github.com/spencer17x/arova-releases/releases) · [User guide](USAGE.md) · [Home](README.md)

| Capability | Current behavior |
| --- | --- |
| Discovery | Public GigaX signals; private wallet activity requires sign-in |
| Wallet monitoring | Add a wallet address, select compatible chains and choose buys, sells, incoming transfers, outgoing transfers or other activity |
| Networks | Solana, Ethereum, BSC, Base and Robinhood |
| Shared workspace | Website and extension use the same account data, private notes and server-side monitoring rules |
| Monitoring infrastructure | Platform-managed RPC nodes; no user setup required. Existing private credentials remain encrypted until explicitly cleared by their owner |
| Wallet allowance | Free: 10 active addresses; one address across multiple chains uses one slot. Pausing releases it. Plan limits and expiry appear in the account |
| Wallet cards | Token identity, chain, full contract, asset flows, timestamps and transaction links; uncertain or missing values remain labeled |
| Routed trades | Evidence-based settlement without inventing wallet debits or credits; a router payout alone does not establish that the recipient bought |
| Telegram | Independent destinations, rules, languages and note visibility; saving and sending a test are separate actions |
| Trends and forwarding | Dedicated trend monitors and Telegram message-forwarding settings; chain selection supports multiple networks |
| Languages | English and Simplified Chinese UI; source content and token names retain their original language |
| Sound and layout | Shared sound preferences/custom audio, compact panels, responsive settings and per-site panel positioning |
| Account access | Account settings, available plans and access status; ordinary users do not receive internal administrator permissions |

Token headings use `symbol (name)`, omitting duplicates or missing fields. Market quotes and estimates are not necessarily executed trade prices. Existing Telegram messages are not rewritten when settings change.

XXYY trend, multiple and related report messages retain the original Chinese content, layout, buttons and image descriptions. They are not translated by the generic interface-language setting.

Telegram forwarding account credentials and sessions are encrypted per user; forwarding account login is separate from the notification Bot configuration. Saved sensitive configuration is masked by default, with owner-scoped reveal controls for supported fields. Login sessions, codes and two-step passwords are not revealed.

## Coverage limits

- Only activity after the configured monitoring start is expected; old history is not backfilled automatically.
- Internal EVM native-currency transfers and complex routes are not fully covered.
- Cross-chain receipts without source ownership evidence are treated as incoming transfers. A buys-only filter can therefore omit some genuine cross-chain buys.
- Arova smart-wallet/resonance signals, legacy platform feeds, Pump Top and Fomo/Pump login-renewal entry points are retired.
- This release does not implement automated trading, an Arova Alpha Score, or guaranteed performance.

[License](LICENSE) · [Setup and troubleshooting](USAGE.md)

Memberships: Free includes 10 active wallets; Plus includes 100 ($29/month or $290/year); Pro includes 300 ($79/month or $790/year). All accounts follow the same rules. Automatic 100-wallet signup gifts and trials have ended; purchased memberships and individual administrator gifts retain their terms. Excess wallets are paused with addresses, notes and history retained. Purchases remain disabled. When enabled, subscription payments accept only native Circle USDC on Solana, with manual renewal and SOL for network fees. Memberships use calendar months/years; annual forwarding allowances reset monthly. Unlimit removes plan quotas through an explicit account grant: [contact thugz on Telegram](https://t.me/thugz1) or [X](https://x.com/thugz001). Account isolation, suspension and platform/provider rate limits still apply.

GigaX cards and notifications omit the price row; market cap, growth, contract and original provider text remain available.

The website and admin interface include the October 7, 2026 updates: session verification shows a loading state, plan comparisons and contact-button alignment are corrected, and the purchase switch controls new orders without changing plan access. Purchases remain closed. The public extension is still beta.6; website deployments do not update extension files. See the [user guide](USAGE.md).
