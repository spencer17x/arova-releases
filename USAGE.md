# Arova user guide

Token identities in GigaX, growth and wallet notifications use **symbol (full name)** consistently across Telegram, browser alerts and signal cards. Identical names are shown once; missing fields use the available value. Original provider text is unchanged.

## Website, wallet allowance and alert sounds

The website and Chrome extension share wallets, alerts, Telegram and sound settings. Arova manages monitoring nodes; no RPC setup is required. Accounts receive an initial allowance of 100 active addresses. One address across multiple chains uses one slot; pausing releases it. The initial allowance currently has no end date, which is not a promise of permanent free access. Check your account for its allowance and expiry. Under Alert sounds, select a tone or upload MP3/WAV/OGG (512 KB / 10 seconds maximum), preview and save; enable browser notifications too. Website audio requires a user gesture and stops when the page closes. Telegram controls its own sounds. Website sign-in supports email, Telegram and linked wallets; Google remains available in the extension.


Use **Monitored wallets** to add an address and note, then choose compatible networks and operations. Solana addresses use Solana; EVM addresses can use Robinhood, Base, BNB Chain and Ethereum. Monitoring starts from configuration; it does not import older trades. The previous Fomo/Pump login collectors, social feeds and renewal jobs are stopped in this mode. Legacy materials, if any, have an explicit cleanup entry in account settings. Existing Telegram rules remain intact. Internal native EVM transfers and some complex routes remain outside coverage; check the per-chain status for delays or recorded gaps.

The current website and extension no longer offer Fomo/Pump authorization or separate platform wallet lists. Use one Wallet monitoring source and operation filter. A partially checked option means saved rules differ; unchanged options are preserved. Only explicitly changing that option unifies it. Old authorization links lead to account settings, where existing legacy connections can be explicitly removed. Reload the updated extension to use the new client; it no longer requests platform session-reading permissions.

## Current wallet notifications

Telegram wallet alerts show the token name directly, followed by direction/network, wallet note or shortened address, and the full contract. Amount and market-cap fields use a compact tree layout without category headings. Buy/sell alerts omit the token-quantity row, “Token name” and “Reference” prefixes, provider explanations and external market-site buttons. Gross receipts and net received remain distinct. Estimates retain `≈`; stale caps stay labeled **Cached cap**. Beijing time (UTC+8) is the last body line. The only buttons are **View transaction** and **Copy contract**, when available. Website details still retain exact quantities, quote sources and timestamps.

If you reach your allowance, pause unneeded wallets or check the plans page for available upgrades. Excess wallets pause after an allowance expires; history and labels remain. Re-enable them after renewal. Old RPC settings remain encrypted and can be explicitly cleared in your account settings.

**English** | [简体中文](USAGE.zh-CN.md)

Updated: 2026-10-01. The wallet-address mode above describes the current client/server implementation; older extension packages may require an update. Platform login and social-feed instructions and screenshots below describe the older public beta; they do not apply in wallet mode.

The latest client links destination saving to the main Telegram switch: when the main switch is off and a destination is enabled, **Save and enable alerts** saves that destination and resumes all enabled destinations. Disabling the main switch preserves each destination’s settings. Saving a disabled destination or sending a test does not enable automatic alerts. The screenshots below predate this change; older release packages still require enabling the main switch separately.

[Features](https://github.com/spencer17x/arova-releases/blob/main/FEATURES.md) · [Download](https://github.com/spencer17x/arova-releases/releases) · [Home](README.md)

- [Installation and updates](#installation-and-updates)
- [Language settings](#language-settings)
- [Quick start](#quick-start)
- [Account and sign-in](#account-and-sign-in)
- [Connect monitoring sources](#connect-monitoring-sources)
- [Renewal methods](#renewal-methods)
- [Panel and browser alerts](#panel-and-browser-alerts)
- [Account notes and platform search](#account-notes-and-platform-search)
- [Telegram alerts](#telegram-alerts)
- [Watchlist](#watchlist)
- [Plans and access](#plans-and-access)
- [Troubleshooting](#troubleshooting)

## Installation and updates

### First installation

1. Open [Releases](https://github.com/spencer17x/arova-releases/releases) and download `arova-chrome-VERSION.zip`.
2. Extract it to a folder you will keep. The selected folder must directly contain `manifest.json`.
3. Enter `chrome://extensions` in Chrome and enable **Developer mode**.
4. Click **Load unpacked** and select the extracted folder.
5. Pin Arova through Chrome's extensions menu, then click its toolbar icon to open standalone settings.

Do not use GitHub's automatically generated **Source code (zip/tar.gz)** archive as the installation package, or select an unextracted ZIP. See [Chrome's official loading instructions](https://developer.chrome.com/docs/extensions/get-started/tutorial/hello-world#load-an-unpacked-extension).

### Updating an installed version

1. Download the new package, even if its version name has not changed.
2. Replace the contents of the original loaded folder, keeping its location.
3. Find Arova in `chrome://extensions` and click **Reload**.
4. Refresh open trading pages. Reopen or refresh settings if it still shows the old interface.

Do not uninstall first if you want to keep browser settings. GitHub ZIP packages do not update installed extensions automatically. Do not delete the folder while Chrome is using it.

A beta may be rebuilt with the same name and version. Check the release notes, build identifier in `release-info.json`, and `SHA256SUMS` to distinguish builds.

## Language settings

The settings sidebar offers **Interface language → Follow browser / 简体中文 / English**. Chinese browser locales default to Simplified Chinese; other locales default to English. A manual choice is stored on this browser. Settings, open panels, connection prompts, and browser alerts follow the choice without clearing current form drafts. Wallet sign-in and checkout use the selected language when opened.

Each Telegram destination has a separate **Alert language**, applied when that destination is saved. Existing destinations default to Chinese; new destinations default to the current interface language. Changing the interface does not change group alert languages. Messages already being delivered keep their original language on retries. Source posts, account names, notes, token names, and administrator-written plan descriptions stay in their original language.

## Quick start

1. Install the extension, open settings, and sign in or create an Arova account.
2. In **Connections**, connect the Fomo / Pump accounts you want to use.
3. Read the renewal information, choose browser or server renewal, and complete the required confirmation.
4. Enable the panel under **Panel & device**, then open a supported XXYY, GMGN, or DeBot trading page.
5. Start with **Following**, then configure browser alerts, account notes, or Telegram destinations as needed.

Settings provide feedback after saving. An empty list can simply mean there is no new activity. Check connections and filters before treating it as a fault.

## Account and sign-in

Under **Account & login**, use your Arova email and password, or an available Google, Telegram, Solana wallet, or EVM wallet entry point. Complete confirmation in the relevant authorization window. Availability depends on the service configuration and wallet support.

Your Arova password is separate from your Google / Telegram password. To use Google, click **Continue with Google**; do not enter your Google password as an Arova password. Google sign-in must run through the installed Chrome extension.

To add a sign-in method to an existing account, sign in to that account first and link the identity under **Account & login**. This keeps your settings and notes together. Matching emails or names do not automatically merge accounts.

Wallet sign-in uses your signature to prove identity. You do not provide a private key to the account sign-in page. Signing in does not authorize trades or enable Pump server custody.

## Connect monitoring sources

1. Sign in to Arova and open **Connections**.
2. For Fomo, read the custody notice, close other Fomo tabs, and click **Connect and enable server renewal**. Approve Chrome permissions if prompted and sign in on the official page if needed. Arova reads that page's session, verifies the account, and submits encrypted server custody automatically. The temporary authorization page closes when handing over the session; no Token form or second submit is needed.
3. For Pump, click **Connect account** and sign in on the official page if needed. After connecting, enter the matching account's full Solana private key in its card, review the custody notices, and submit. Arova does not automatically extract wallet keys.
4. Wait for the server renewal success status, then enable the desired monitoring and notification rules. A connected Pump session alone does not mean renewal is enabled.

The providers are independent. Pausing monitoring, revoking a connection, and turning off renewal are separate actions. Errors appear as feedback; an unconfirmed outcome must be checked before resubmitting. Changing accounts, leaving, or reloading may discard sensitive drafts.

## Renewal methods

This version uses **server renewal only** and stops legacy browser renewal jobs. Existing server custody is preserved; it is never silently recreated after revocation.

**Fomo:** the connection button explicitly authorizes reading the temporary official page's Access Token, Refresh Token, and optional Privy Access Token and storing them encrypted on Arova's server and backups. These are not read-only credentials. Other Fomo tabs block handover to avoid concurrent session refreshes; Arova does not close your existing tabs. Missing credentials, website changes, permission refusal, or an account change stops completion with a clear error. Website login or verification may still require your action.

**Pump:** server renewal requires the full Base58 Solana private key matching the connected account, entered manually with explicit consent. Ordinary wallet connection and login do not provide that key. Without the matching key, server renewal cannot be enabled. The key grants full wallet control; “login only, no trades” is a software restriction, not a limit on the key's permissions.

Server custody is experimental. Closing Chrome, signing out of Arova, or pausing monitoring does not revoke custody. Use **Turn off server renewal** or the credential removal button. Active credentials are removed on revocation; encrypted backups expire under retention rules, so immediate erasure cannot be guaranteed. Never share credentials in chats or screenshots. Website verification, re-login, or revocation can still require your action.

## Panel and browser alerts

Enable the panel under **Panel & device**. It appears on supported XXYY, GMGN, and DeBot trading pages. Adjust its position, size, and theme as needed.

Use the panel to switch between Following, Platform activity, and Pump Top, and filter by source or **All tokens / Current token**. Expand messages to view originals, copy contracts, or open trading pages. Each message uses its own contract address.

**Token info card** changes card visibility, not the current-token filter. Browser alerts and the Telegram master switch are available as quick controls in the panel; detailed rules stay in settings.

Browser alerts also require Chrome and operating system notification permissions. Closing the panel does not stop server monitoring or Telegram alerts. Closing Chrome stops browser desktop notifications.

## Account notes and platform search

Under **Account notes**, choose a view:

- **My follows** reads the connected platform account's actual following list.
- **Search platform users** queries a name or address and marks results as following, not following, or unknown.
- **Has note** manages your saved notes, including accounts you may have unfollowed.

Fomo and Pump are queried separately. Pages default to 10 rows, with 10 / 20 / 50 / 100 options. Follow relationships are cached briefly and show a query time. Reload later after recent platform changes. A failed query's “unknown” status does not mean “not following.”

Use **Add note / Edit note** to save a private note. **User profile** opens the platform page. Notes belong only to your Arova account and do not change platform names or follow relationships. Follow or unfollow accounts on the original platform.

## Telegram alerts

### Send alerts to groups or channels

1. Add the Arova notification bot supplied by the operator to the target group / channel and permit it to send messages.
2. Use the bot's `/chatid` command to obtain the Chat ID. Copy the full value, including any minus sign.
3. Add a destination under **Telegram alerts** and enter its group label and Chat ID.
4. Select the destination's alert language, sources, categories, and whether to **Show my account notes in alerts**.
5. Click **Save this destination**, or save and enable alerts when prompted.
6. After saving, click **Send test to this group** separately. Check the message in that group, then ensure both the Telegram master switch and destination are enabled.

Each destination is saved, deleted, and tested independently. Saving sends no message and does not overwrite other drafts. Tests use saved settings only; save any pending changes first. A destination with no valid categories will not receive automated alerts.

Fomo / Pump alerts may include the current post, token avatar, original link, and contract actions. Missing images fall back to text, and missing post bodies are omitted. Account note visibility follows each destination's switch.

### Monitor group or channel messages

**Monitor messages** adds messages the bot actually receives from specified groups / channels to activity. This is separate from outbound alert destinations. Enter the monitored Chat IDs and save; the bot must also be able to receive messages there. This does not read your personal Telegram account's full chat history.

## Watchlist

Under **Watchlist**, enter the token contract, chain, and name as offered by the form, then click **Add to watchlist**. You can also enter from the current token's `24/7` control in the panel; review the supplied information before confirming.

Disable or remove entries as needed. A watchlist does not execute trades. Actual activity depends on valid provider connections, monitoring state, service access, and notification rules.

## Plans and access

Open **Plans & access** to view current access and orders. Free mode requires no payment. Prices, durations, and available channels are shown in the interface. After an administrator grants or extends access, use **Refresh status** to check it.

Unlimited access has no expiry and may be displayed as **Permanent access**. It does not require renewal but can still be adjusted or suspended by a super administrator. Service access does not grant internal administrator permissions.

When paid access and an available plan are enabled: choose a plan, network, and stablecoin → create an order → connect your wallet and confirm in the separate checkout → wait for on-chain verification and access activation. Follow the current checkout instructions; do not substitute addresses from documentation or chat.

Cancelling a wallet action keeps the order. If broadcast status is unknown, verification is pending, or the order is paid but still activating, check the order before paying again. For an incorrect network, currency, or amount, keep the order ID and transaction hash for the operator to review. Automatic matching or refunds are not guaranteed.

Renewal extends an unexpired access period; expired access starts from activation. Orders refresh automatically and can also be refreshed manually. The service does not charge automatically.

## Troubleshooting

| Issue | What to check |
| --- | --- |
| Chrome cannot load the package | Extract the ZIP and select the folder directly containing manifest.json; do not use the Source code archive |
| Old interface after updating | Download the latest build, check its identifier, replace the original folder contents, reload the extension, and refresh trading pages |
| Connecting reports a user gesture error | Update to the current beta build, reload the extension, reopen settings, and click Connect again; permission requests must start directly from that click |
| Settings stays on loading | Reload the extension and reopen settings; check the network and Arova session. Keep redacted error details if it persists |
| No panel on a trading page | Check platform / page support, panel visibility, extension site permissions, and refresh the page |
| Expected activity is missing | Check provider authorization, monitoring switches, view / source filters, token scope, and service access |
| Browser alerts do not appear | Check account alerts, device switch, and OS permissions. Settings and initial loads do not replay historical alerts |
| Telegram test button disabled | Save that destination first; it cannot be tested while it has a draft or is submitting |
| Telegram test failed or unconfirmed | Check bot membership, send permissions, and Chat ID. Look for the message before retrying an uncertain delivery |
| Renewal incomplete | Check the selected method and actual saved status. The provider may need re-login or your signature |
| Follow status differs | Check query time and reload later. Platform search may return only part of the matches |
| Internal admin sign-in denied | Ordinary extension users have no admin permissions. Open your own settings using the Chrome toolbar icon |

When reporting an issue, include the version / build identifier, time, platform, and redacted error text. Do not include passwords, tokens, cookies, verification codes, or private keys.

## Illustrated walkthrough

### Installation and preparation
Download the official ZIP from the public release repository, extract it, and use Chrome's Load unpacked option. Replacing a package with the same version also requires reloading the extension.

### 1. Create an Arova account and sign in
Under Account & login, choose Create account, enter your email and a separate password of at least 12 characters, then select Create account and sign in. Your Arova password is separate from your Google password. Existing users can sign in directly or use a linked identity.

![Create an Arova account; email and password regions are redacted](assets/guide/01-register.png)

Existing users can select Return to sign in and use their Arova email and password. Screenshots show the Chinese interface; choose English in the sidebar language selector if preferred.

![Arova sign-in form](assets/guide/02-login.png)

After sign-in, Account & login shows the linked email/password identity. Linking Google, Telegram, or a wallet is optional and separate from connecting the Fomo/Pump monitoring sources below.

![Signed-in account settings with email redacted](assets/guide/03-account.png)

### 2. Connect Fomo
Open Connections, read the custody notice, close other Fomo tabs, and click Connect and enable server renewal. Complete any official login or verification. The extension then connects and enrolls the session automatically. Wait for Server renewal authorization saved.

![Connections before enrollment](assets/guide/04-providers-before.png)

A successful connection shows a Fomo connected and server renewal enabled toast, plus the saved authorization status in the Fomo section. No manual token entry is needed. If account changes, other official tabs, or verification errors block the operation, follow the displayed instructions before reconnecting.

![Fomo connection and server renewal authorization saved](assets/guide/05-fomo-success.png)

### 3. Connect Pump and configure server renewal
Click Connect account in the Pump section and complete the official login. The basic connection captures the current session; ongoing server renewal requires the separate manual custody configuration below.

![Pump account connection entry](assets/guide/06-pump-before.png)

If you choose private-key custody for renewal, personally obtain the matching account's key through the official Pump wallet export interface. This screenshot shows only the export entry, with the wallet identifier redacted; it contains no private key.

![Official Pump wallet export interface with wallet identifier redacted](assets/guide/07-pump-export.png)

Return to Arova and manually enter that account's Base58 Solana private key in the Pump section. Review and select both custody and ongoing login-signing confirmations, then submit to enable server renewal. Seed phrases, EVM private keys, and login tokens are not accepted.

This is not read-only access: the complete private key can control the wallet. Login-only behavior is a software constraint, not a limitation of the key's permissions. Materials are encrypted on the server and in backups until active custody is revoked; backups expire under their retention policy. Never send the key in chats or screenshots.

![User-completed custody form with the entire private-key input covered by a solid mask](assets/guide/08-pump-consent.png)

After Server renewal authorization saved appears, you do not need to enter the key again. Closing Chrome does not revoke custody. Use the stop-renewal and remove-active-key button to remove active custody. Waiting for the next schedule indicates saved authorization awaiting scheduling; it does not prove renewal after natural expiry.

![Pump server renewal authorization saved](assets/guide/09-pump-success.png)

### 4. Configure a Telegram destination
Add a destination under Telegram alerts, enter a label and Chat ID, and choose the notification language, sources, and whether to show your account notes. Save each destination separately; other destination drafts remain independent.

This example selects only Pump Friends and Fomo Alerts, with Fomo alerts restricted to buys and sells. Platform feeds and rankings are unchecked. Adjust these choices to suit your needs.

![Telegram destination language, account notes, and source filters; Chat ID redacted](assets/guide/10-telegram-config.png)

Click Save this destination. The confirmation explicitly states that the destination was saved without sending a test. Testing becomes available after saving.

![Destination saved independently without sending a test](assets/guide/11-telegram-saved.png)

### 5. Send a separate test message
Save the destination first, then click Send test to this group. Saving alone does not send a test. Check both the success feedback and the Arova test notification received in Telegram. Test messages are not trading signals.

![The page confirms that the test message was sent to this group](assets/guide/12-telegram-test.png)

![Test message actually received in Telegram; group information and unrelated messages cropped out](assets/guide/13-telegram-received.png)

The received message says automatic notifications are still off. A successful test proves that the bot can send to the destination. To receive subsequent live signals, also enable the main automatic-notification switch on the Telegram page and keep this destination enabled. New signals must match the selected sources and types. Sending a test does not replay historical alerts. If delivery is unconfirmed, check the group before clicking again.

### 6. Daily use and troubleshooting
Use the floating panel for alerts and quick switches, and the management page for full settings. Closing Chrome, signing out, pausing monitoring, and revoking custody are different actions. Use the relevant renewal/credential removal control to revoke active custody; backups expire under their retention policy.

The screenshot below shows a real Fomo Alerts buy notification received after the test. It includes the token image, source, trade value, market cap, event time, and links to the original and trading platforms. The account name and contract identifier are redacted. The earlier test message described the switch state at the time of that test; its text does not update when the switch changes later.

![Actual Fomo buy notification received, with account name and contract redacted](assets/guide/14-fomo-live.png)

This walkthrough verifies email registration and sign-in, Fomo/Pump connections and saved renewal authorization, independent Telegram saving and testing, and a received Fomo live alert. Pump live receipt and long-term renewal after natural expiry on either platform were not verified by this screenshot workflow.

### Screenshot privacy
Emails, personal names, wallet addresses, group identifiers, and sensitive details are covered with solid masks. Passwords and private keys are entered only by the user in the designated form and are never captured in full. Platform content, names, and custom notes retain their original language.

### Authorization progress and revocation (current repository)

While connecting, the provider section shows a loading indicator and the current stage: permission/website opening, waiting for sign-in, verifying and saving the connection, and reading/saving Fomo renewal authorization. Avoid repeated actions while processing. Disabling renewal removes active custody materials but retains the basic connection. Revoking authorization removes the Arova connection and active renewal materials. Neither clears the website’s own Chrome sign-in session. Existing encrypted backups expire under their retention policy.

The floating panel’s browser and Telegram switches save independently. Only the switch being saved is disabled and shows a loading indicator; labels and spacing remain fixed.

Each Telegram destination supports independent Pump type filters: Buy, Sell, Posts/Callouts, Updates, Replies/Quotes/Reposts, and Other. These apply to Pump Friends and Callouts; Pump Top remains controlled by its separate source checkbox. Existing configurations default to all types. Selecting none suppresses these Pump activity streams. Save the destination to apply changes; newly enabled types do not replay historical notifications. This requires both the updated server and extension.

When signed out, the management page shows only the sign-in screen, including when opened through a settings deep link. Configuration navigation appears after sign-in. With no stored session, opening the page does not load protected account/configuration APIs; a stored session is checked before workspace loading.

## Opt-in GigaX signal trial

Eligible accounts can create a scoped receiver config under **Monitoring authorization → GigaX**. The single-account server experiment can receive pushes without your Mac or Android. A local emulator receiver still requires both to remain online. Recreating the config disables the current receiver, including a server receiver, until its config is replaced. The direct server receiver renews its scoped upload credential before expiry. Revoked or already expired connections require explicit reconnection. In Telegram settings, select **GigaX Signals** and its types separately for each destination, then save that destination. Existing groups are not opted in automatically; saving does not send a test or replay history. This trial receives original App pushes, not trading Feed items. Keep receiver configs private. Availability, setup and limitations: [GigaX trial](docs/gigax-trial.md).

## Signal sources

Arova smart-wallet/convergence signals and their multiplier notifications have been removed. Use address-based Wallet Monitoring for your own wallets; GigaX signals remain available.

GigaX growth alerts continue to show the token, full contract, multiple, price and market cap. Telegram replies to the first corresponding notification when a receipt is available; missing quotes remain `--`.

### Website discovery

Browse GigaX signals without signing in. Filter by network or search a token/contract. Sign in to Wallet Monitoring to manage personal wallets and view private activity. Use Settings for Telegram and sound preferences. The website and extension share your account data.

Public signal lists show newest first, with 10/20/50 items per page. Search and source/network filters apply across the latest 100 public signals. Changing a filter returns to page one; later pages stay stable during polling. Custom menus support arrow keys, Enter and Escape. Animation respects reduced-motion settings.

Public cards show token artwork, name, DEX Paid (paid/unpaid/unknown), and available X, website, Telegram and Discord links. Details refresh independently through the server cache; source and time are shown. X search links are labeled as searches. These links and payment labels are source reports, not verification of safety or official ownership.

Market caps use K/M/B in both languages. Cards distinguish signal-time market cap from the latest cached XXYY price, with its update time. Quotes normally refresh every ten minutes; missing supplier prices remain --.

Wallet activity only lists operations from your monitored addresses; filter by network, with recent saved records read separately for each chain. Public signals remain in Discover. GigaX source controls are under Settings → Signal source; extension notifications and Telegram delivery rules are unchanged.

Add any supported wallet address under Wallet Monitoring; platform origin is not required. Pause or enable each address individually. Record lists use one pager, with 10/20/50 items per page. Wallet-note and Telegram-target drafts survive page changes. Existing notification routes/rules are preserved.

## Trending alerts and Telegram forwarding

In **Settings → Trending alerts**, create a monitor, select one or more chains, and save your own Bot Token. Add each destination Chat ID and save its notification mode independently. XXYY alerts and reports retain the original Chinese wording, layout and buttons. Saving does not send a message. Enable the monitor when ready. The first successful snapshot is a silent baseline; imported monitors retain their existing baselines. Daily, weekly and historical/current multiple reports are available on the page and through the configured bot.

In **Settings → Telegram forwarding**, add sources, destinations and optional keywords. Advanced rules preserve the original dev-labs format, including user, regex, media and combined filters. Choose whether to keep forwarding attribution or copy messages. Save rules separately from connecting an account.

Get your own **API ID and API Hash** from my.telegram.org, then connect with your phone number, login code and optional Telegram two-step verification password. These credentials are different from a Bot Token. Connecting requires explicit consent to encrypted server and backup storage of a Telegram login session. A person able to decrypt that session can use the Telegram account. Pausing stops forwarding; disconnecting deletes active login data, while backups expire under the retention policy. Telegram's device settings can revoke the session itself.

Imported monitors remain paused until ownership and the old-service cutover are verified. Do not run the same bot receiver or Telegram session in both systems. Messages with an unknown delivery outcome are not automatically replayed.

Use a dedicated bot for a trend monitor. A single bot can cover multiple chains and destinations; do not reuse the Arova system bot or a bot still being polled elsewhere.

Saved Bot Token, API ID, API Hash and phone fields are masked by default. Click the eye beside a field to show it, then click again to hide it. Values missing from an older import are marked as not saved. Use **Delete monitor** to remove a selected monitor after confirmation; this also removes its active credentials and history. Removing a forwarding rule changes the draft until you save.
