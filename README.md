# Preservation of Government Information
### An Information Stewardship Call to Action

**Live site:** [publicinformationtrust.org](https://publicinformationtrust.org)

> *Government information is far more fragile than it should be. This is a call for library and archives professionals to act.*

---

## About

This repository hosts the public-facing website for the **Preservation of Government Information: An Information Stewardship Call to Action**, authored by James Jacobs and Jim Jacobs. The site was drafted at the **Information Stewardship Forum 2026, San Francisco**, and published in conjunction with [Free Government Information (FGI)](https://freegovinfo.info).

The website provides:
- A full embedded rendering of the call to action.
- A sign-on form for individuals and organizations wishing to publicly endorse it.
- A curated public list of signatories.

---

## Repository Structure

```
publicinformationtrust-org/
├── index.html          # Main single-page site (Swiss Style design)
├── signatories.json    # Curated list of public signatories
├── CNAME               # Custom domain configuration for GitHub Pages
└── README.md           # This file
```

---

## How It Works

### Sign-on Form
The site uses [Web3Forms](https://web3forms.com) to collect signatory submissions. When someone fills out the form, an email is delivered directly to `jrjacobs@stanford.edu` containing their full submission details.

Submissions are **not automatically published**. Each signatory must be manually reviewed and approved before being added to the public list.

### Signatories List
Public signatories are stored in `signatories.json` and rendered dynamically on the page. To add a new signatory after reviewing their submission:

1. Open `signatories.json` on GitHub
2. Add a new entry using one of the templates below
3. When saving, always choose **"Commit directly to master"** — not "Create a new branch"

The site updates automatically within a few minutes of each commit.

#### Entry templates

**Individual, name only:**
```json
{ "type": "individual", "name": "Jane Smith" },
```

**Individual with affiliation:**
```json
{ "type": "individual", "name": "Jane Smith", "affiliation": "Stanford University Libraries" },
```

**Individual with affiliation and date:**
```json
{ "type": "individual", "name": "Jane Smith", "affiliation": "Stanford University Libraries", "date": "2026-04-10" },
```

**Organization, name only:**
```json
{ "type": "organization", "name": "Data Rescue Project" },
```

**Organization with contact person:**
```json
{ "type": "organization", "name": "CA Public Library Advocates", "affiliation": "Deborah Doyle, President" },
```

#### Fields

| Field | Required | Notes |
|---|---|---|
| `type` | No | `"individual"` or `"organization"` — metadata only, not displayed |
| `name` | Yes | Displayed as the bold headline |
| `affiliation` | No | Displayed as a second line below the name |
| `date` | No | Format `"YYYY-MM-DD"` — displayed as e.g. April 10, 2026 |

#### Rules

1. Always wrap text in `"double quotes"`
2. Put a `,` after each `}` — **except the very last entry in the file**
3. Commit directly to `master` — not a new branch

```json
  { "type": "individual", "name": "Second to Last Person" },
  { "type": "individual", "name": "Last Person" }
```

**Reference spreadsheet** (private, access-controlled):
[Preservation of Government Information Submissions](https://docs.google.com/spreadsheets/d/1i1z0TbPr_p0Qvf8kbbh7aMATRAau08tG5ekS83LXI3U/edit?gid=0#gid=0)

---

## Hosting & Deployment

The site is hosted on **GitHub Pages** at the custom domain `publicinformationtrust.org`.
- **HTTPS:** Enforced via GitHub Pages SSL
- **Deployment:** Automatic — any push to `master` goes live within ~2 minutes.

---

## Design

The site uses the **International Typographic Style** (Swiss Style), with inspiration from [freegovinfo.info/pgi](https://freegovinfo.info/pgi). Key design principles:

- Grid-based asymmetric layout
- High-contrast typographic hierarchy (Inter / Helvetica Neue)
- Strict geometric forms — no gradients, no rounded corners
- FGI heritage slate blue (`#3e6487`) as the primary brand color
- Generous whitespace for academic readability

---

## The Statement

The call to action is embedded from Google Docs using its **"Publish to Web"** URL to ensure it renders for all visitors without requiring Google authentication or cookies.

- **Published document:** [View](https://docs.google.com/document/d/e/2PACX-1vRGDfZQSQqv4HylBNwHm_kiO_p84VWRGZErlehqyqVuT8pRkz2uqvjay39UHIsvts6HUPVITPR9bUMR/pub)
