# Mori POS — Retail & Service Operations Workspace

**An AI-assisted, iterative POS and operations prototype designed to connect everyday sales, inventory, appointments, and business administration in one approachable workflow.**

> **Project:** Personal product development / portfolio showcase  
> **Platform:** Browser-based UI; Google Apps Script backend explored for deployment  
> **Status:** Prototype and QC/staging — **not approved for production transactions**  
> **Source availability:** This repository is a public showcase; private implementation and operational data are not included.

## Why I Built It

Small shops and service businesses often have to manage sales, stock, staff activities, and customer requests across disconnected tools or spreadsheets. I wanted to explore how a single, uncomplicated workspace could reduce repetitive administration while still giving owners visibility into daily operations.

Mori POS is also a hands-on exercise in **turning a practical business problem into a working product through AI-assisted development**. My role has focused on defining requirements, mapping workflows, reviewing interfaces, testing use cases, identifying defects, and iterating on performance and usability.

## What the Prototype Covers

| Area | Demonstrated design / prototype capability |
| --- | --- |
| **Point of sale** | Product selection, cart/bill workflow, checkout-oriented screens, receipts and configurable print layouts. |
| **Catalog & inventory** | Product and category administration, stock-in flows and inventory-oriented records. |
| **Store configuration** | Store/branch identity, contact details, branding and module settings. |
| **Payments & receipts** | Bank/QR configuration and receipt previews, including 58 mm, 80 mm and A4 formats. |
| **Customer-facing pages** | Concepts and preview pages for storefront/catalog, online orders, booking and order tracking. |
| **Staff operations** | Attendance-oriented interfaces and role-dependent navigation in the broader prototype. |
| **Data & auditability** | Google Sheets-backed staging architecture with separate operational datasets and audit records. |

These features have been documented across multiple prototype and staging versions. **Feature presence in a preview does not mean every workflow has been end-to-end verified in a deployed environment.**

## Product Workflow

```text
Merchant setup / branch settings
             |
             v
   Product catalog & inventory
             |
        +----+--------------------+
        |                         |
        v                         v
  In-store sales          Customer-facing pages
        |                   (browse / book / order)
        v                         |
    Bill & receipt <--------------+
        |
        v
 Operations records / review / audit
```

## Technical Approach

The project explores a low-infrastructure implementation that suits small internal applications:

- **HTML, CSS and JavaScript** for browser-based administration and customer-facing interfaces.
- **Google Apps Script** for web-app deployment and server-side business operations in the staging design.
- **Google Sheets** for structured operational records, with separate datasets for master data, items, stock-in, bills, bookings, attendance and audit information.
- **Google Drive** for supported image/file storage in the Apps Script deployment design.
- **Role and email-OTP checks** in the staging flow, with server-side authorization identified as an essential production requirement.

This architecture was chosen for **fast iteration, low initial infrastructure overhead and straightforward inspection of data flows**. It requires further hardening before any real commercial deployment.

## My Contribution & AI-Assisted Development

I approached this project as a product builder drawing on data engineering, operations and delivery experience:

1. Defined business scenarios: sales, stock movement, store configuration, staff and customer touchpoints.
2. Mapped screen flows and connected the user experience to the intended underlying data model.
3. Used AI development assistants to accelerate UI exploration, implementation experiments and troubleshooting.
4. Reviewed outputs, identified defects, clarified acceptance criteria and requested focused revisions.
5. Iterated on usability, consistency, data read/write behavior, and operational controls.

**AI was a development accelerator; product direction, requirements, testing priorities and acceptance decisions remained human-led.**

## Product Decisions & Lessons

- **Keep daily tasks simple:** make core actions visible and avoid overloading each screen with configuration.
- **Treat stock and money as controlled records:** sales, stock-in, payment confirmation and adjustments need explicit states and reviewable history.
- **Separate demonstration from production:** a convincing UI preview is not sufficient evidence of secure authentication or reliable financial transactions.
- **Design for constrained operations:** lightweight hosting and Sheets can be useful for a pilot, but performance, concurrency and permissions must be tested as usage grows.
- **Preserve change history:** audit records, QC checks and explicit deployment steps help reveal operational risks.

## Development Journey

- **UI prototype:** sales screens, branch settings, checkout concepts and responsive layouts.
- **Operational extensions:** product/stock flows, receipt printing, QR configuration and customer-facing page concepts.
- **Staging architecture:** Apps Script entry points, Google Sheets/Drive datasets, administrative access flows and setup/health checks.
- **Ongoing refinement:** inventory UX, forecasting ideas, read/write performance, status handling and error recovery.

## Screenshots & Demonstration

Add real captures from a sanitized test environment before publishing:

| Suggested asset | What it should demonstrate |
| --- | --- |
| `assets/01-dashboard.png` | Overall operations workspace and navigation |
| `assets/02-sales.png` | POS checkout and bill workflow |
| `assets/03-inventory.png` | Products, categories and stock-in flow |
| `assets/04-settings.png` | Branch, receipt or payment settings |
| `assets/05-customer-site.png` | Customer-facing storefront or booking preview |

> Do not publish real merchant accounts, customer information, receipts, API keys, Apps Script deployment secrets or internal spreadsheet IDs.

## Current Limitations

- **Prototype / QC only:** not certified or verified for production transactions, tax invoices or automatic payment confirmation.
- Some UI capabilities may be demonstrations rather than fully integrated services.
- A QR image is a payment instruction, **not** confirmation that funds have arrived.
- Real-world deployment needs complete testing for security, access control, concurrent writes, stock reconciliation, backups, data retention and failure recovery.
- Google Apps Script and Sheets have practical quotas and scale limits that must be assessed before production use.

## What This Project Demonstrates

**Business-process mapping · Product requirements · Data workflow thinking · AI-assisted development · UX iteration · Operational risk awareness**

Mori POS represents my interest in making everyday operations more accessible by combining a practical business perspective with automation and product development.

---

**Author:** Louis Lam (Nghiep Lam)  
**Focus:** Data Engineering · Product Operations · Practical AI · Workflow Automation  
**Portfolio note:** This is project documentation, not an offer of a production-ready POS service.
