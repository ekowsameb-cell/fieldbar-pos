# FieldBar POS v2

Offline-first bar POS for Ghanaian businesses (bars, nightclubs, lounges).
Built for three distinct roles on the same PWA:

- 🔵 **Counter** — walk-in sales (own float), fulfills waiter orders, owns stock.
- 🟢 **Waiter** — takes table orders, collects money, sends to counter.
- 🟣 **Boss** — dashboard, close-night summary, menu/stock/staff management (PIN-locked).

## How it works

- **No internet needed.** All data is stored on the device (localStorage).
- **Bad internet?** Staff converge on the **Counter device**, which is the single
  source of truth. Waiter→Counter handoff works via **Export file → Import on Counter**
  (tap "Send to Counter" → export JSON → boss/counter imports → tap Fulfill).
- **Good internet? (optional)** Enable Cloud Sync in Boss → Settings by pasting a
  Supabase URL + anon key. Then waiter orders push live and the counter fulfills them
  in real time.

## Install (Android / Chrome)

1. Open the GitHub Pages URL in Chrome.
2. ⋮ menu → "Install app" / "Add to Home screen".
3. Choose your role on launch.

## Roles at a glance

| Role    | Records sales | Owns stock | Takes money | PIN? |
|---------|---------------|-----------|------------|------|
| Counter | Yes (walk-in) | Yes       | Yes        | No   |
| Waiter  | Yes (tables)  | No        | Yes        | No   |
| Boss    | View only     | Manages   | No         | Yes  |

## Data & backup

- Tap **Boss → Close Night → Export Backup** to download a JSON snapshot.
- No account, no server required. Your data stays on your device.

## Files

- `index.html` — the whole app (3 roles, offline ledger)
- `manifest.json`, `sw.js`, icons — PWA install/offline support
