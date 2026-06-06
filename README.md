# Invoices

A minimal, single-file invoice builder for two recurring household services — piano lessons and lawn care. Runs entirely in the browser with no backend, no dependencies, and no install.

**[Open →](https://baadaa.github.io/home-invoices/)**

## What it does

Two independent invoice tools in one page, switchable via a tab:

- **Piano Lessons** — schedule sessions by date, indicate which child (or both) is attending, flag makeup sessions, and tally the total. Rate: $45/child/session.
- **Lawn Service** — log mowing visits, select which services were included (flat yard at $75, hill cleaning at +$40), and generate a per-period total.

Each tool generates a clean, printer-ready invoice with a line-item table, per-category subtotals, and an optional notes field.

## Features

- Date picker for session/visit entry
- Checkbox-style toggles for attendees and services
- Automatic chronological sorting
- Per-category subtotals + grand total
- Optional notes field (appears on printed invoice)
- `localStorage` persistence — data survives page reloads until manually cleared
- Last active tab is remembered
- Print via browser (`File → Print` or `⌘P`) — UI chrome is hidden, only the invoice renders

## Usage

1. Open `index.html` in any modern browser, or visit the [GitHub Pages URL](https://baadaa.github.io/home-invoices/)
2. Select a tab (Piano or Lawn)
3. Fill in the invoice details (provider name, period, invoice number)
4. Add sessions or visits using the date picker and toggles
5. Hit **Print Invoice** to open the browser print dialog
6. Hit **Clear** to reset all data for that invoice type

## Notes

- No data leaves your browser — everything is stored locally via `localStorage`
- Print works when the file is opened directly or served over a domain; it will not work inside embedded iframes (e.g. GitHub's file preview)
- Rates are hardcoded in the file; edit the `RATE`, `RATE_FLAT`, and `RATE_HILL` constants at the top of each app's script block to adjust
