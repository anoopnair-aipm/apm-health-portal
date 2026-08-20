# APM Health Portal

An **APM-oriented** variant of the Customer Relationship Health portal for the fictional banking-software vendor *Lorum Ipsum Inc.* This site is **exclusive to APM identifiers** — the account selector is labelled **"Select APM"** and lists **APM1000001–APM1000008** instead of bank names.

It is a self-contained `dashboard.html` that reads its data from an external `data.json`. No build step, no framework, no backend.

**▶ Live demo: <https://anoopnair-aipm.github.io/apm-health-portal/>**

> This is a separate, standalone deployment. The original bank-name portal lives at
> <https://anoopnair-aipm.github.io/customer-relationship-health/> and is unaffected.

---

## What's different from the original portal

- The Bankers/APM toggle is **removed** — this site is APM-only.
- The account dropdown header reads **"Select APM"**.
- Each account is shown by its **APM number** (`APM1000001` … `APM1000008`), assigned in customer order.

Everything else — the health score computation, sub-score breakdown, incident/concern tracking, trend charts, export (PDF/CSV/PNG), share links, and the AI assistant — is identical to the original.

---

## Running locally

Because the dashboard loads `data.json` with `fetch()`, it must be served over HTTP:

```bash
python3 -m http.server 8000
```

Then open <http://localhost:8000/dashboard.html>.

---

> **Note:** All data is fictional and for demonstration only.
