# Arova user guide

**English** | [简体中文](USAGE.zh-CN.md)

Applies to the current public beta. Updated: 2026-09-15.

[Features](FEATURES.md) · [Download](https://github.com/spencer17x/arova-releases/releases) · [Home](README.md)

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

1. Sign in to Arova and find the Fomo or Pump card under **Connections**.
2. Click **Connect account** and sign in to your own account on the official provider page.
3. Return to the matching provider section and complete the requested permissions and confirmation. Follow-up inputs, status, and prompts appear in that section.
4. Check connection status, then enable the desired monitoring and notification rules.

Providers are managed separately. Pausing monitoring, revoking a connection, and turning off renewal are different actions; check each status.

If authorization fails, read the feedback and correct your input. If the result is unconfirmed, check status before submitting again. Leaving the page, changing accounts, or reloading may discard unsaved sensitive credential drafts.

## Renewal methods

Server renewal is currently preselected on the authorization form. **Preselection does not activate custody.** The methods are mutually exclusive; the saved status determines which is active.

| Method | Requirements | What you do |
| --- | --- | --- |
| Automatic browser renewal | Chrome must be running, Arova signed in, and the website session recoverable | No long-lived credential or private-key entry; allow temporary background provider tabs to sync short-lived sessions for the same account |
| Automatic server renewal | Maintained by Arova's server, including when Chrome is closed | Enter credentials in the provider card (Fomo also offers confirmed local fill), read the risks, and explicitly confirm; the server must offer this feature |

**Fomo server renewal** requires the same session's Access Token, Refresh Token, and optional Privy Access Token. These are long-lived session credentials, not read-only credentials. Follow the help in the card and close website tabs sharing that session as instructed to avoid concurrent refreshes.

To fill Fomo credentials without copying them manually:

1. In the same Chrome profile, open `https://fomo.family` and sign in to the intended Fomo account.
2. In Arova settings → Connections → Fomo → Server renewal, click **Read from a signed-in Fomo page**.
3. Select the website tab, read the local-read notice, and check its consent box. Click **Confirm read and fill**, then approve the optional Chrome permission if prompted.
4. If both required fields are available, all three inputs are replaced with that session; an unavailable optional PAT is left empty. No credentials are uploaded and no renewal starts.
5. Review the account and inputs, follow the instructions for closing Fomo tabs sharing the session, then confirm custody and submit separately. The server verifies that it is the same connected account.

If a required field is missing or unrecognized, no fields are filled and your previous input is kept. Use the manual instructions below the button. Website storage may change, and signed-in state alone does not guarantee these fields are accessible. A tab reload, navigation, account change, or permission refusal cancels the read. Reading does not automatically close tabs, refresh tokens, or read any wallet keys.

**Pump server renewal** requires the full Solana private key in Base58 matching the connected account. It grants wallet control, not read-only access. “Login only, no trades” is a software restriction; it does not limit the key's actual permissions. Choose browser renewal if you do not understand the credentials or do not want custody.

Server credentials are stored encrypted on the service and in backups. Closing Chrome, signing out of Arova, or pausing monitoring does not revoke custody. Use **Turn off server renewal** or the relevant removal button. After active credentials are removed, existing backups expire according to retention rules; immediate erasure cannot be guaranteed. Never share tokens, private keys, recovery phrases, or verification codes in chats, groups, or issue screenshots.

Either method may need your action for website verification, re-login, or session revocation. To switch to browser renewal, turn off existing server renewal first, then explicitly enable browser renewal.

## Panel and browser alerts

Enable the panel under **Panel & device**. It appears on supported XXYY, GMGN, and DeBot trading pages. Adjust its position, size, and theme as needed.

Use the panel to switch between Following, Platform activity, and Pump Top, and filter by source or **All tokens / Current token**. Expand messages to view originals, copy contracts, or open trading pages. Each message uses its own contract address.

**Token info card** changes card visibility, not the current-token filter. Browser alerts and the Telegram master switch are available as quick controls in the panel; detailed rules stay in settings.

Browser alerts also require Chrome and operating system notification permissions. Closing the panel does not stop server monitoring or Telegram alerts. Closing Chrome stops browser renewal and browser desktop notifications.

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
