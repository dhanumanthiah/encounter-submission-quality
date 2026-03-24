# 📊 Encounter Submission Quality & HEDIS Measures Dashboards
### Power BI Analytics for Medicaid Encounter Quality and Clinical Performance at a Nonprofit Health Plan

---

## Overview

This repository documents two Power BI dashboards built to give operations, compliance, and leadership teams real-time visibility into two critical performance domains at a nonprofit health plan in Minnesota:

1. **Encounter Submission Quality Dashboard** — tracking Medicaid T-MSIS encounter rejection rates across five error categories, driving systematic fixes that achieved a **95% first-pass acceptance rate**
2. **HEDIS Measures Dashboard** — tracking clinical quality performance across four HEDIS measures for leadership reporting and quality improvement prioritization

Both dashboards replaced reactive, manual reporting with structured, data-driven visibility across two critical performance domains.

**Role:** Senior Business Analyst / Product Owner (requirements, data analysis, dashboard definition)
**Tool:** Power BI
**Encounter Type:** Medicaid (T-MSIS)
**Key Outcome:** 95% first-pass encounter acceptance rate achieved

---

## Dashboard 1: Encounter Submission Quality

### Problem

Medicaid encounter submissions were being rejected at unacceptable rates across multiple error categories. Each rejection represented a compliance gap, a potential T-MSIS reporting failure, and — depending on the error type — a risk to accurate RAF scores and capitation payments.

The core problem was not that errors were occurring. It was that **no one had visibility into where errors were concentrated, why they were happening, or whether fixes were working.** Errors were discovered reactively, resolved ad hoc, and recurred because root causes were never systematically addressed.

**Error categories driving rejections:**

| Error Type | Impact |
|---|---|
| **TA1 / 999 rejections** | Entire encounter file rejected at interchange or transaction level |
| **Missing or invalid diagnosis codes** | Encounter records rejected; HCC coding gaps downstream |
| **Provider NPI mismatches** | Encounters rejected due to NPI not matching CMS provider registry |
| **Duplicate submissions** | Rejected encounters creating reconciliation noise and resubmission burden |
| **RAPS / EDPS encounter rejections** | Risk adjustment data gaps affecting RAF scores and capitation accuracy |

### Solution

A Power BI dashboard giving operations and compliance teams real-time visibility into encounter submission errors — by type, volume, trend, and root cause — paired with structured resolution playbooks.

### What the Dashboard Tracked

| View | Description |
|---|---|
| **Error volume by type** | Daily and weekly rejection counts segmented by error category |
| **Trend over time** | Error rate trajectory showing whether fixes were holding |
| **Root cause attribution** | Errors mapped to upstream source — provider data, internal processing, or file formatting |
| **Resubmission status** | Tracking of corrected encounters through the resubmission cycle |
| **First-pass acceptance rate** | Headline metric — percentage of encounters accepted without rejection on first submission |

### My Role
- Analyzed raw rejection data from T-MSIS and CMS systems to identify error patterns and root causes across all five error categories
- Defined dashboard requirements and worked with the IT and data team to build the Power BI reporting layer
- Documented root cause findings and translated them into structured resolution playbooks for operations and compliance teams
- Drove fixes with internal teams — provider data corrections, NPI registry reconciliation, file formatting standards
- Tracked first-pass acceptance rate as the primary success metric across successive submission cycles

### Outcome
- Achieved **95% first-pass encounter acceptance rate** — up from a baseline of persistent, multi-category rejections with no systematic tracking
- Eliminated reactive, ad hoc error resolution in favor of a structured, data-driven quality management workflow
- Established root cause documentation and resolution playbooks that reduced recurrence across submission cycles

---

## Dashboard 2: HEDIS Measures

### Problem

Leadership had no consolidated view of HEDIS measure performance across the health plan's Medicaid population. Clinical quality data existed in disparate systems, and measure performance was reported manually and inconsistently — making it difficult to identify where to prioritize quality improvement efforts or track whether interventions were working.

### Solution

A Power BI dashboard giving leadership a consolidated view of HEDIS measure performance — by measure, by population, and by trend over time — enabling data-driven quality improvement prioritization.

### Measures Tracked

| HEDIS Measure | Description |
|---|---|
| **Prenatal / Postpartum Care (PPC)** | Timeliness of prenatal visits and postpartum follow-up for Medicaid pregnant members |
| **Diabetes Care Measures** | HbA1c testing, eye exams, and kidney health monitoring for members with diabetes |
| **Breast Cancer Screening** | Mammography rates for eligible female members |
| **Annual Wellness Visits** | Preventive care visit completion rates across the Medicaid population |

### What the Dashboard Tracked

| View | Description |
|---|---|
| **Measure rate by period** | HEDIS measure performance rates by reporting period |
| **Trend over time** | Performance trajectory showing whether quality initiatives were moving the needle |
| **Gap identification** | Members with open care gaps by measure — actionable for care coordination outreach |
| **Population segmentation** | Performance breakdowns by member population and plan type |

### My Role
- Defined dashboard requirements in collaboration with the clinical quality team and leadership
- Worked with the data team to identify and validate source data for each HEDIS measure
- Designed the reporting structure to support both leadership review and operational gap-closure workflows
- Led UAT to validate measure calculation accuracy against HEDIS technical specifications

### Outcome
- Gave leadership a consolidated, real-time view of HEDIS performance across four measures for the first time
- Enabled data-driven prioritization of quality improvement initiatives based on gap volume and trend
- Supported care coordination teams with actionable gap lists for member outreach

---

## Key Learnings & PM Reflection

These two dashboards reinforced a core product principle: **visibility is necessary but not sufficient.** The encounter dashboard solved the visibility problem — but working through hundreds of rejected encounters manually made it clear that the bottleneck is the reasoning loop between seeing an error and knowing exactly what to do about it.

The HEDIS dashboard reinforced the same principle from a different angle. Leadership could now see where gaps were — but translating that visibility into coordinated member outreach at scale still required significant manual effort.

Both dashboards pointed toward the same next step: tooling that not only shows what's wrong, but tells you why and what to do about it. That insight shaped how I think about the next generation of payer-side analytics tools.

---

## Artifacts Available

> *Note: All artifacts are sanitized to remove PHI and proprietary system details in compliance with HIPAA.*

- [ ] Dashboard requirements document — sanitized
- [ ] Encounter error category taxonomy & root cause analysis
- [ ] Resolution playbook — encounter resubmission workflow
- [ ] HEDIS measure technical specification mapping
- [ ] First-pass acceptance rate trend (anonymized)

---

*This repository documents product ownership work completed at a nonprofit Medicare and Medicaid health plan. All data, member records, and system details have been sanitized or synthesized for public sharing.*
