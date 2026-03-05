# 🎺 Band Admin Prototype

![GitHub repo size](https://img.shields.io/github/repo-size/BondiBrass/admin-proto)
![GitHub last commit](https://img.shields.io/github/last-commit/BondiBrass/admin-proto)
![GitHub issues](https://img.shields.io/github/issues/BondiBrass/admin-proto)
![License](https://img.shields.io/badge/license-MIT-green)

A lightweight brass band admin dashboard powered by a **single Google Sheet** (multiple tabs).

No backend. No database. Just **HTML + JavaScript + Google Sheets**.

---

## 🚀 Live demo

Once GitHub Pages is enabled:

**https://bondibrass.github.io/admin-proto/**

---

## ✨ What it does

- **Tonight**: next event + program + RSVP summary  
- **Library**: repertoire search + grade/duration filters + PDF/audio links  
- **Gigs**: upcoming events + tasks  
- **Sets**: predefined performance sets (Set → Pieces)  
- **Committee**: roles + assets register

---

## 🧠 Architecture

```mermaid
flowchart TD
  A[Google Sheet<br/>(11 tabs)] -->|GViz CSV per tab| B[index.html<br/>Static site]
  B --> C[Tonight<br/>Next event + program + RSVP]
  B --> D[Library<br/>Search + filters]
  B --> E[Gigs<br/>Events + tasks]
  B --> F[Sets<br/>Set → pieces]
  B --> G[Committee<br/>Roles + assets]

  subgraph Tabs in Google Sheet
    T1[Members]
    T2[Roles]
    T3[Assets]
    T4[Pieces]
    T5[Parts]
    T6[Sets]
    T7[SetPieces]
    T8[Events]
    T9[Program]
    T10[Tasks]
    T11[RSVP]
  end
