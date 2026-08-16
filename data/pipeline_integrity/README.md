# Pipeline Integrity Lab Data

All files in this directory are fictional instructional data for the Ravenwood Recruiting Company scenario. They do not represent USARD systems, real applicants, real recruiting activity, or real vacancies.

The scenario date is `2026-08-14`. Files are deliberately inconsistent so learners can practice data validation, source reconciliation, and decision-readiness assessment.

| File | Role in the scenario |
|---|---|
| `crm_pipeline_extract.csv` | Current pipeline snapshot exported from the fictional CRM |
| `recruiter_activity_extract.csv` | Contact and appointment activity events |
| `campaign_lead_extract.csv` | Campaign and source-attribution records |
| `stage_reference.csv` | Authoritative instructional stage definitions |
| `recruiter_capacity_snapshot.csv` | Recruiter capacity and snapshot freshness information |

The lab intentionally includes duplicate prospects, unmapped stages, missing or future timestamps, malformed ZIP codes, activities that do not reconcile to the CRM, source-attribution conflicts, and a stale capacity record.
