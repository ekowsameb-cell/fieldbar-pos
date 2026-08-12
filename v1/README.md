# FieldBar POS

Offline-first **bar & nightclub POS** — tabs, waiters, customer credit, SMS bills. No printer, no server.

Built on the FieldSales Pro offline engine. All data stays on the device (localStorage). Works with zero internet.

## Features (v1)
- **Menu & stock** — items with price + stock; low-stock alert.
- **Floor / tickets** — open a ticket per table/tab, add items, mark **Served** when collected at the counter.
- **Waiters** — tag each ticket with a waiter; see **per-waiter sales** (top seller) on the owner dashboard.
- **Payment** — Cash / MoMo / **Credit (tab)** per ticket.
- **Customer credit** — running balances for regulars; record payments.
- **Owner dashboard** — today's sales, cash vs MoMo vs tab, ticket count, low-stock, top waiters.
- **Close Night** — summary (sales split, top waiters, low-stock list) → SMS to owner (gateway-ready, offline-safe).
- **Backup/export** — JSON export.
- **Installable PWA** — add to home screen; opens full-screen, offline.

## How to use (pilot)
1. Open the live link in the bar's counter tablet (and any waiter phone).
2. **Add to Home Screen** (Share → Add to Home Screen).
3. Owner sets up menu + waiters once. Staff open tickets per table.

## SMS (optional)
SMS is stubbed (`queueSMS` in `index.html`) so the app runs fully offline. To enable real SMS (Hubtel/Arkesel Ghana):
- Set `SMS_CONFIG.enabled = true`, `SMS_CONFIG.gateway`, `SMS_CONFIG.ownerPhone`.
- Implement the POST to the gateway inside `queueSMS`.

## Deploy
Static site — push to any static host (GitHub Pages used for the pilot). No backend required.

---
*Spec: marketing/FieldBar_POS_Spec.md. Status: MVP v1 (2026-08-13).*
