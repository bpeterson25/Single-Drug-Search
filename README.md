# DrugMaster Query – Single Drug Search

## Overview

DrugMaster Query is a Python/Jupyter Notebook designed to retrieve and consolidate drug information from publicly available drug reference sources.

The notebook allows users to search by:

- Brand Name
- Generic Name
- National Drug Code (NDC)

Data is retrieved and integrated from:

- OpenFDA
- DailyMed
- RxNorm

The goal is to provide a consolidated view of drug products, package configurations, manufacturers, dosage forms, routes of administration, and clinical drug concepts.

---

## Business Use Cases

### Medical Economics

- Drug landscape reviews
- Competitive product assessments
- Manufacturer identification
- Product packaging analysis

### Pharmacy Operations

- NDC validation
- Drug master maintenance
- Product normalization

### Formulary Management

- Product research
- Package comparisons
- Clinical concept review

---

## Features

### Single Drug Search

```python
search_drug("Opdivo")
```

Returns:

- Products
- Packages
- DailyMed Metadata
- RxNorm Information

### NDC Search

```python
search_ndc("00006-5026-01")
```

Returns:

- Product Information
- Package Information
- DailyMed Metadata

### Excel Export

```python
export_excel(results, drug_name)
```

Creates:

```text
DrugMaster_Opdivo.xlsx
```

---

## Data Sources

### OpenFDA

Primary source for:

- Product NDC
- Package NDC
- Manufacturer
- Dosage Form
- Route
- Application Number
- Marketing Category

### DailyMed

Provides:

- SPL Metadata
- Published Label Information

### RxNorm

Provides:

- RxCUI
- Clinical Drug Concepts
- Ingredient Relationships
- Clinical Hierarchy

---

## Output Tables

### Products

One row per product.

### Packages

One row per package configuration.

### DailyMed

Structured Product Label metadata.

### RxNorm

Clinical concept relationships.

---

## Requirements

Python libraries:

```python
pandas
requests
openpyxl
```

---

## Future Enhancements

Planned additions include:

- Orange Book
- NADAC
- ASP Pricing
- HCPCS / J-Code Crosswalks
- Therapeutic Classifications
- Repository Integration

---

## Author

DrugMaster Initiative

Purpose-built to support Medical Economics, Pharmacy Analytics, Value-Based Pharmacy, and Drug Intelligence initiatives.
