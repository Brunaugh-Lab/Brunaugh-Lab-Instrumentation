# Brunaugh Lab — Instrumentation & Measurement Standards

This repository contains **public, read-only documentation** describing how instruments are configured, used, and interpreted in the Brunaugh Lab.

The goal of this repository is to make **measurement practices explicit, reproducible, and teachable**, without exposing internal project management, data, or analysis code.

---

## Scope of This Repository

This repository documents:

- Instrument-specific setup and usage conventions  
- Definitions of measurement settings and metadata fields  
- Template and SOP philosophy (what is fixed vs configurable)  
- Data export expectations and naming conventions  
- Conceptual guidance for interpreting measurements  

It is intended to support:
- consistent data generation
- onboarding and self-service learning
- reduction of ad hoc or undocumented instrument usage

---

## What This Repository Does *Not* Contain

This repository does **not** include:

- Raw or processed experimental data  
- Analysis code or pipelines  
- Project trackers, issues, or planning documents  
- Grant materials or unpublished results  

Those materials are maintained separately in **private lab repositories**.

---

## Repository Structure

Documentation is organized by instrument under `/docs/`, for example:
```
docs/
└── instrumentation/
└── sympatec_LD/
├── measurement_setting_fields.md
├── templates_and_sops.md
├── data_export_and_naming.md
└── conceptual_overview.m
```
Each document is intended to be:
- readable directly in GitHub
- linkable from lab wikis or bookmarks
- stable enough to serve as a reference during measurements

---

## Relationship to Internal Lab Resources

This repository is intentionally **decoupled** from internal lab coordination tools.

- Internal project tracking, active development, and planning live elsewhere.
- This repository represents the **published standard**, not the working notebook.

When procedures evolve, updates are made deliberately and transparently.

---

## Usage Notes

- All content here is **read-only** for most users.
- If you believe documentation is unclear or incomplete, raise the issue with the lab lead rather than modifying practices ad hoc.
- Instrument software settings should always take precedence over memory or habit.

---

## License / Use

This documentation is provided for educational and reproducibility purposes.
Reuse outside the Brunaugh Lab should be attributed appropriately.
