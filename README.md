# Pustaka Terbuka — FRIM (Perpustakaan Institut Penyelidikan Perhutanan Malaysia)

> **Pustaka Terbuka: Katalog Induk Terbuka untuk Perpustakaan dan Sekolah Malaysia.**  
> *Official Perpustakaan Institut Penyelidikan Perhutanan Malaysia (FRIM) Bibliographic Dataset & Standalone Harvester.*

This repository contains the harvested open MARCXML collection and harvester pipeline for **Perpustakaan Institut Penyelidikan Perhutanan Malaysia** (`FRIM`), contributing to the national Malaysian union catalog at [pustaka-terbuka/opac](https://github.com/pustaka-terbuka/opac).

---

## Institutional Metadata

| Attribute | Value |
| :--- | :--- |
| **Institution Code** | `frim` |
| **Agency Code** | `FRIM` |
| **Official Name** | Perpustakaan Institut Penyelidikan Perhutanan Malaysia |
| **Institution Type** | `special` |
| **State / Territory** | Selangor |
| **Target End Bib** | 100,000 |
| **OPAC Base URL** | [https://library.frim.gov.my/](https://library.frim.gov.my/) |
| **Subject Focus** | Tropical forestry, silviculture, botanical sciences, and wood biodiversity |

---

## Directory Structure

```text
frim/
├── README.md                      # Institutional repository documentation
├── package.json                   # Node.js project specification & scripts
├── harvest/
│   └── inbox/frim/             # Sealed MARCXML batch chunks and manifests
│       └── <run-id>-chunk-001/
│           ├── manifest.json      # Chunk SHA-256 manifest & metadata
│           ├── provenance.jsonl   # Record-level attribution and fetch logs
│           └── records/           # Batched MARC21 slim XML files
├── tools/
│   ├── harvesters/frim/        # Automated OPAC crawler & XML converter
│   └── lib/                       # Supporting MARCXML and validation utilities
└── tests/
    └── harvester-frim.test.js  # Autonomous test suite
```

---

## Usage

```bash
# Install dependencies
npm install

# Test run harvester (10 sample records)
npm run harvest:sample

# Run full collection sweep
npm run harvest:full

# Validate dataset integrity
npm run validate-inbox harvest/inbox/frim/<chunk-directory>
```

---

## Attribution & License

Dataset harvested and preserved under open library metadata standards for educational, civic, and cooperative indexing. Attribution: **Perpustakaan Institut Penyelidikan Perhutanan Malaysia (FRIM)** & **Pustaka Terbuka**.
