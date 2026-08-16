# From Friday Data Pull to Monday Recruiting Plan

## Purpose

The technical labs use a single fictional scenario to show how a recruiting organization can move from fragmented operational data to a reviewable, evidence-backed plan. Rather than automating recruiting decisions about people they improve visibility, prioritization, research, and preparation for human decisions.

The scenario is fictional. All people, places, units, opportunities, data, and outcomes are invented for instruction. No applicant PII, medical information, waiver information, conduct information, security information, or real unit vacancies are used.

## Scenario

It is Friday afternoon at Ravenwood Recruiting Company. The company has four recruiters covering several ZIP codes and school/community markets. A commander wants a practical plan for Monday morning:

> Where should we focus next week, what opportunities should we discuss, what evidence supports the plan, and what needs human review before anyone acts?

The available data is useful but imperfect. It comes from separate systems, uses inconsistent definitions, and changes at different rates. The technical track builds a small, governed decision-support workflow around that reality.

## Baseline Workflow

Without the labs' capabilities, a leader or analyst works manually:

1. Export weekly pipeline, activity, campaign, capacity, market, and opportunity reports.
2. Reconcile inconsistent counts, duplicate records, shifting stage names, and stale information in spreadsheets.
3. Review markets and recruiter workloads using experience and local knowledge.
4. Look up policy, opportunity, and process information across documents and systems.
5. Draft a weekly plan and ask recruiters or leaders to correct missing context.
6. Execute only after the responsible leader reviews the plan.

This workflow is necessary, but it is slow, difficult to reproduce, and vulnerable to unexamined assumptions. The labs improve it in stages while preserving human accountability.

## Synthetic Data Package

Each source represents a familiar category of operational data. The instructional point is that no one source is complete or automatically authoritative.

| Source | Example content | Intended use | Common issue introduced in the lab |
|---|---|---|---|
| CRM pipeline extract | Fictional prospect ID, assigned recruiter, pipeline stage, stage dates, source code | Pipeline visibility | Duplicates, missing dates, inconsistent stage names |
| Recruiter activity extract | Fictional contact, appointment, and follow-up events | Identify work queues and funnel movement | Missing activity links, conflicting timestamps |
| Campaign/source extract | Campaign, event, referral, and web lead records | Understand provenance and market response | Source labels do not reconcile across systems |
| Station capacity roster | Recruiter assignment, workload, leave, and training availability | Check whether a plan is feasible | Stale availability or incomplete roster data |
| Market reference table | ZIP/territory, school/community indicators, access, and aggregate market signals | Compare geographic market opportunities | ZIP formatting and territory mapping issues |
| Mission/opportunity snapshot | Fictional occupational demand and dated local opportunity snapshot | Inform market-level planning | Snapshot is stale or contains an already-filled opportunity |
| Historical aggregate outcomes | Market-by-period activity and funnel outcomes | Build and evaluate market recommendations | Different time windows and incomplete records |
| Reference-data tables | Stage definitions, territory mapping, source-code dictionary | Establish common definitions | Definitions conflict with the exports |
| Approved document corpus | Fictional role summaries, FAQs, process guidance, messaging guidance, and snapshot notes | Grounded research and citation | Conflicting or outdated documents |

The data package intentionally distinguishes a dated planning snapshot from an authoritative determination. It must never be used to make an eligibility, waiver, medical, conduct, security, or final assignment decision.

## The Arc

### 1. Pipeline Integrity: Can We Trust the Operating Picture?

The first lab receives the Friday data pull. Learners profile sources, establish a canonical schema, validate stage transitions and timestamps, identify duplicates and stale records, and preserve source lineage.

The output is not merely a cleaned table. It is a decision-readiness report that states:

- what data is fit to support a market-level recommendation;
- what needs reconciliation or human review;
- the owner and freshness of each important field; and
- what must be excluded from downstream analysis.

Learners also label a small sample of stalled-pipeline records against a written rubric. They compare agreement, identify ambiguity, and refine the rubric before treating labels as evaluation data. This connects data quality to trustworthy analytics.

**Automation gained:** repeatable validation and clear visibility into what the data can support.

**Human responsibility retained:** define operational terms, resolve source conflicts, approve labeling guidance, and decide whether the data is sufficiently current.

### 2. Recommender: Where Does Analyst Attention Go First?

The second lab uses only validated, market-level and operational inputs. It ranks geographic markets or market plays for analyst review against a stated mission need. Example features include opportunity availability, station capacity, aggregate funnel performance, education or workforce signals, source freshness, and travel/access constraints.

The recommender produces a ranked shortlist with explanations, not a binary prediction and not a judgment about an individual person. Learners compare a transparent baseline to a more structured scoring approach and evaluate the output as a ranked list.

**Automation gained:** consistent triage of many possible markets into a manageable, explainable review queue.

**Human responsibility retained:** set the mission objective and constraints, inspect explanations, reject stale or implausible recommendations, and determine the actual outreach plan.

### 3. RAG Assistant: What Evidence Supports the Plan?

The third lab adds an approved fictional knowledge base. The assistant retrieves relevant documents and produces concise answers with citations for questions such as:

- What does the dated opportunity snapshot say about this market?
- What approved messaging guidance is relevant to this outreach plan?
- What process information should a recruiter communicate?

The assistant is required to cite the supporting passages, distinguish fact from inference, and abstain when the documents do not support an answer. It does not make eligibility or other protected determinations.

**Automation gained:** faster research and synthesis from a bounded, approved document set.

**Human responsibility retained:** approve the corpus, verify citations, correct outdated documents, and make decisions outside the assistant's scope.

### 4. Agentic Integration and Evaluation: Can We Produce a Governed Draft?

The final lab orchestrates the prior capabilities into a constrained workflow:

1. Run data-quality checks and surface warnings.
2. Rank markets that warrant analyst review.
3. Retrieve supporting evidence from approved documents.
4. Draft a Monday Recruiting Operations Brief.
5. Stop for a human approval decision before any action.

The draft brief includes recommended market plays, relevant evidence, assumptions, data-quality warnings, and questions requiring review. The agent cannot send messages, change CRM records, or make determinations. It only prepares a traceable draft.

Learners then evaluate the workflow with a test set that includes stale opportunities, conflicting documents, unsupported factual claims, ambiguous inputs, and requests outside the allowed scope. Success is measured by groundedness, citation coverage, relevance, abstention behavior, and reproducibility, not whether the prose sounds persuasive.

**Automation gained:** repeatable assembly of a reviewable operational brief.

**Human responsibility retained:** approve, modify, reject, or escalate the plan; own all contact, eligibility, and mission decisions.

## Capstone Output

By the end of the day, each group can produce a fictional Monday Recruiting Operations Brief containing:

- the top market priorities for analyst and leader review;
- a rationale tied to validated data and dated sources;
- operational constraints such as capacity and data freshness;
- citations to the approved document corpus;
- explicit uncertainty, rejected recommendations, and review items; and
- an approval gate that prevents the draft from becoming an autonomous action.

## Design Principle

The technical sequence is deliberately cumulative:

```text
Requirements -> trusted data -> prioritized options -> grounded explanation -> governed draft -> evaluation
```

Better automation is not more autonomy. It is a more reliable, transparent, and testable way to help people make operational decisions.
