# 📊 CMS Encounter Submission Engine & Quality Dashboards

### End-to-End Requirements Ownership for CMS Encounter Submission at a Nonprofit Health Plan | Power BI Analytics for Medicaid Encounter Quality and HEDIS Performance

---

## Overview

This repository documents two connected workstreams I owned as Senior Business Analyst / Digital Product Owner at a nonprofit Medicare Advantage and Medicaid health plan in Minnesota:

1. **CMS Encounter Submission Engine** — end-to-end requirements ownership for building the health plan's outbound CMS encounter submission engine, aligned to CMS documentation standards for T-MSIS (Medicaid) and EDPS/RAPS (Medicare Advantage), achieving **95%+ first-pass CMS acceptance rate**
2. **Encounter Submission Quality & HEDIS Dashboards** — Power BI dashboards built on top of the engine to give operations, compliance, and leadership teams ongoing visibility into submission quality and clinical HEDIS measure performance

Both workstreams sit at the intersection of regulatory compliance, operational execution, and product ownership in a highly regulated payer environment.

**Role:** Senior Business Analyst / Digital Product Owner
**Domain:** Medicare Advantage, Medicaid (T-MSIS), CMS Encounter Submission
**Tools:** CMS Encounter Submission Standards, Power BI, EDI 837, RAPS/EDPS, HL7/FHIR
**Key Outcome:** 95%+ first-pass CMS encounter acceptance rate

---

## Part 1: CMS Encounter Submission Engine

### The Problem

UCare's Medicaid and Medicare Advantage encounter submissions were generating persistent rejections across multiple error categories. The root cause wasn't just bad data — it was that the outbound encounter submission process lacked a structured requirements foundation aligned to current CMS documentation standards.

Every rejection represented more than a technical failure:

| Rejection Type | Business Impact |
|---|---|
| **TA1 / 999 rejections** | Entire encounter file rejected at interchange or transaction level |
| **Missing or invalid diagnosis codes** | Encounter records rejected; HCC coding gaps downstream |
| **Provider NPI mismatches** | Encounters rejected due to NPI not matching CMS provider registry |
| **Duplicate submissions** | Rejected encounters creating resubmission burden and compliance noise |
| **RAPS / EDPS rejections** | Risk adjustment data gaps directly affecting RAF scores and capitation accuracy |

Without a correctly functioning submission engine, downstream risk adjustment, HEDIS measure calculation, and STAR ratings were all at risk.

---

### My Role: End-to-End Requirements Ownership

I owned the end-to-end requirements for building UCare's CMS outbound encounter submission engine — working directly from CMS encounter submission documentation standards to define the business and system requirements for generating properly formatted outbound 837 encounter records.

**What this involved:**

- **Translated CMS documentation standards** into structured business and system requirements for the submission engine, covering T-MSIS encounter submission for Medicaid and EDPS/RAPS for Medicare Advantage
- **Defined outbound encounter record logic** — field-level validation rules, format specifications, and submission logic aligned to CMS 837 transaction standards and encounter submission guidelines
- **Authored requirements across the full submission lifecycle** — from internal claims and clinical data inputs through format transformation, validation, and outbound file generation to CMS
- **Partnered with internal engineering and data teams** to build and validate the engine against CMS specifications, documenting edge cases, exception handling, and resubmission workflows
- **Established acceptance criteria and led UAT** against CMS submission requirements across Medicaid and Medicare Advantage populations
- **Drove cross-functional alignment** across compliance, finance, clinical quality, and technology teams to ensure requirements reflected both CMS standards and operational realities

---

### Outcome

- **95%+ first-pass CMS encounter acceptance rate** — up from persistent, multi-category rejections with no systematic quality baseline
- Eliminated reactive, ad hoc rejection management in favor of a structured, requirements-driven submission process
- Submission engine output directly feeds CMS risk adjustment (RAF scoring), HEDIS measure calculation, and STAR ratings — protecting downstream capitation accuracy and quality performance
- Established root cause documentation and resolution playbooks that reduced recurrence across submission cycles

---

## Part 2: Encounter Submission Quality & HEDIS Dashboards

Once the submission engine was functioning correctly, the next requirement was visibility. The dashboards below were built on top of the engine foundation to give operations, compliance, and leadership teams ongoing data-driven insight into submission quality and clinical performance.

---

### Dashboard 1: Encounter Submission Quality

#### Problem

Even with a correctly built engine, ongoing submission quality required active monitoring. Errors still occurred — from upstream provider data issues, NPI registry mismatches, and edge cases in clinical data — and without structured visibility, teams were discovering rejections reactively and resolving them ad hoc.

#### Solution

A Power BI dashboard giving operations and compliance teams real-time visibility into encounter submission errors — by type, volume, trend, and root cause — paired with structured resolution playbooks.

#### What the Dashboard Tracked

| View | Description |
|---|---|
| **Error volume by type** | Daily and weekly rejection counts segmented by error category |
| **Trend over time** | Error rate trajectory showing whether fixes were holding |
| **Root cause attribution** | Errors mapped to upstream source — provider data, internal processing, or file formatting |
| **Resubmission status** | Tracking of corrected encounters through the resubmission cycle |
| **First-pass acceptance rate** | Headline metric — percentage of encounters accepted without rejection on first submission |

#### My Role

- Analyzed raw rejection data from T-MSIS and CMS systems to identify error patterns and root causes across all error categories
- Defined dashboard requirements and worked with the data team to build the Power BI reporting layer
- Documented root cause findings and translated them into structured resolution playbooks for operations and compliance teams
- Drove fixes with internal teams — provider data corrections, NPI registry reconciliation, file formatting standards
- Tracked first-pass acceptance rate as the primary success metric across successive submission cycles

#### Outcome

- Maintained 95%+ first-pass encounter acceptance rate through ongoing structured monitoring
- Replaced reactive error discovery with a proactive, data-driven quality management workflow
- Resolution playbooks reduced recurrence and created institutional knowledge for ongoing operations

---

### Dashboard 2: HEDIS Measures

#### Problem

Leadership had no consolidated view of HEDIS measure performance across the health plan's Medicaid and Medicare Advantage populations. Clinical quality data existed in disparate systems, and measure performance was reported manually and inconsistently — making it difficult to identify where to prioritize quality improvement efforts or track whether interventions were working.

#### Solution

A Power BI dashboard giving leadership a consolidated view of HEDIS measure performance — by measure, by population, and by trend over time — enabling data-driven quality improvement prioritization.

#### Measures Tracked

| HEDIS Measure | Description |
|---|---|
| **Prenatal / Postpartum Care (PPC)** | Timeliness of prenatal visits and postpartum follow-up for Medicaid pregnant members |
| **Diabetes Care Measures** | HbA1c testing, eye exams, and kidney health monitoring for members with diabetes |
| **Breast Cancer Screening** | Mammography rates for eligible female members |
| **Annual Wellness Visits** | Preventive care visit completion rates across the Medicaid population |

#### What the Dashboard Tracked

| View | Description |
|---|---|
| **Measure rate by period** | HEDIS measure performance rates by reporting period |
| **Trend over time** | Performance trajectory showing whether quality initiatives were moving the needle |
| **Gap identification** | Members with open care gaps by measure — actionable for care coordination outreach |
| **Population segmentation** | Performance breakdowns by member population and plan type |

#### My Role

- Defined dashboard requirements in collaboration with the clinical quality team and leadership
- Worked with the data team to identify and validate source data for each HEDIS measure
- Designed the reporting structure to support both leadership review and operational gap-closure workflows
- Led UAT to validate measure calculation accuracy against HEDIS technical specifications

#### Outcome

- Gave leadership a consolidated, real-time view of HEDIS performance across four measures for the first time
- Enabled data-driven prioritization of quality improvement initiatives based on gap volume and trend
- Supported care coordination teams with actionable gap lists for member outreach

---

## Key Learnings & PM Reflection

These two workstreams reinforced a core product principle: **visibility is necessary but not sufficient.**

The encounter submission engine solved the structural problem — but working through the rejection patterns made something else clear. The real bottleneck is the reasoning loop between seeing an anomaly in submitted data and knowing exactly what it means, why it happened, and what to do about it. Rules-based validation catches formatting errors. It doesn't catch behavioral patterns — a provider coding an HCC with no supporting clinical history, or billing from two locations hundreds of miles apart in the same week.

That insight directly shaped **ClaimGuard** — a pre-submission payment integrity AI tool for Medicare Advantage payers that moves the intervention earlier: detecting behavioral anomalies in HCC coding patterns, location conflicts, and provider upcoding before claims ever reach CMS submission. The goal isn't better dashboards after the fact. It's catching the problem before the encounter leaves the payer.

The natural next evolution is **Phase 4 of ClaimGuard**: inverting the same detection logic to surface members with likely undocumented conditions — not overcoding, but undercoding — where legitimate clinical risk is being missed and capitation payments are being left on the table. Same engine, same payer intelligence layer, inverted direction.

The encounter submission work is where the problem became clear. ClaimGuard is where it gets solved.

---

## Artifacts

> *Note: All artifacts are sanitized to remove PHI and proprietary system details in compliance with HIPAA.*

- CMS encounter submission requirements documentation — sanitized
- Encounter error category taxonomy and root cause analysis
- Resolution playbook — encounter resubmission workflow
- HEDIS measure technical specification mapping
- First-pass acceptance rate trend (anonymized)

---

## Connect

**Deepa Hanumanthiah** — Senior AI Product Manager | Healthcare AI & Payer Operations

[LinkedIn](https://www.linkedin.com/in/deepa-hanumanthiah-0a02b41b) • [GitHub](https://github.com/dhanumanthiah) • [ClaimGuard Live Demo](https://claimsight-frontend.onrender.com)

---

*This repository documents product ownership work completed at a nonprofit Medicare and Medicaid health plan. All data, member records, and system details have been sanitized or synthesized for public sharing.*
