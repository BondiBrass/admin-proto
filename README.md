# 🎺 Bondi Brass – Admin Prototype

![GitHub repo size](https://img.shields.io/github/repo-size/BondiBrass/admin-proto)
![GitHub last commit](https://img.shields.io/github/last-commit/BondiBrass/admin-proto)
![GitHub issues](https://img.shields.io/github/issues/BondiBrass/admin-proto)
![License](https://img.shields.io/badge/license-MIT-green)

A lightweight **band administration dashboard** powered entirely by a **single Google Sheet**.

No backend.  
No database.  
Just **HTML + JavaScript + Google Sheets**.

Designed for **community bands** who want simple administration tools without complicated software.

---

# 🚀 Live site

Once GitHub Pages is enabled the prototype will run here:

https://bondibrass.github.io/admin-proto/

---

# ✨ Features

### 🎼 Tonight
Shows the **next upcoming event**

Includes:

- event details  
- venue  
- uniform  
- map link  
- concert program  
- RSVP summary  

---

### 🎶 Library

Searchable band music library.

Filters include:

- search text  
- grade  
- duration  

Displays:

- title  
- composer  
- missing parts  
- PDF score  
- rehearsal audio  

---

### 📅 Gigs

Shows:

- upcoming events  
- gig preparation tasks  

---

### 🎵 Sets

Defines **pre-planned performance sets**

Examples:

- marching sets  
- park concerts  
- festival repertoires  

---

### 🏛 Committee

Band administration information:

- committee roles  
- band assets  
- equipment register  

---

# 🧠 Architecture

```mermaid
flowchart LR

Sheet["Google Sheet\n(11 tabs)"] -->|"CSV via GViz"| App["index.html\nStatic dashboard"]

App --> Tonight["Tonight view"]
App --> Library["Library view"]
App --> Gigs["Gigs view"]
App --> Sets["Sets view"]
App --> Committee["Committee view"]

subgraph Tabs["Google Sheet tabs"]
Members
Roles
Assets
Pieces
Parts
SetsTab["Sets"]
SetPieces
Events
Program
Tasks
RSVP
end

Tabs --> Sheet
