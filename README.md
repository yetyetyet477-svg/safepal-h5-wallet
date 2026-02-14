# SafePal H5 Wallet (WalletConnect)

A tiny **H5 web page** that connects to **SafePal** (or any WalletConnect-compatible wallet) and can:

- Connect / disconnect (WalletConnect v2)
- Switch chain (BSC / Ethereum / Polygon)
- Show address + native balance
- Send a native token transfer
- Sign a message

> This project **does not store private keys**. All signing happens in the user’s wallet app.

## 1) Configure WalletConnect Project ID

WalletConnect v2 requires a Project ID.

1. Create one here: https://cloud.walletconnect.com
2. Open `index.html` and set:

- `WC_PROJECT_ID = "..."`

## 2) Run locally (macOS)

Use a local server (don’t open via `file://`).

```bash
cd /path/to/this/repo
python3 -m http.server 5173
```

Then open:

- http://localhost:5173

## 3) Publish on GitHub Pages

In the repo:

- Settings → Pages → **Build and deployment** → Source: `Deploy from a branch`
- Branch: `main` / Folder: `/ (root)`

After it deploys, open the Pages URL and connect with SafePal.

## Notes

- WalletConnect typically requires `https://` (or `http://localhost`).
- If you want this to *auto-deeplink* into SafePal on mobile, we can add a dedicated “Open SafePal” button and WalletConnect URI handling.
