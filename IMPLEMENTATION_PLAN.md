Implementation Plan
Status

Planning phase

This document describes the intended implementation direction.

The exact architecture, technologies, schemas, and pipeline design should be refined after investigating the actual public data sources.

Phase 0 — Project Setup
Goals

Establish the project repository

Configure Git

Install the Cursor learning toolkit

Establish project documentation

Configure project-specific Cursor instructions

Deliverables

Git repository

Project documentation

.cursor/ learning toolkit

Project-specific Cursor rules

Phase 1 — Data Source Investigation
Goals

Understand what public data is actually available from:

TTC

Bike Share Toronto

Investigate both historical and live/frequently updated sources.

Questions to Answer

What datasets are available?

What does each dataset represent?

What fields are available?

What is the update frequency?

What historical coverage exists?

What identifiers exist?

How are timestamps represented?

What geographic information exists?

What are the data limitations?

Can the data support the two analytical questions?

Deliverable

A documented data-source assessment.

No major pipeline architecture should be finalized before this phase.

Phase 2 — Analytical Data Design
Goals

Translate the analytical questions into measurable metrics.

Determine:

Which historical metrics are useful

Which current metrics are available

How historical baselines should be calculated

How comparable historical observations should be selected

How deviations should be measured

Which dimensions are necessary

Which aggregations are appropriate

Deliverable

A documented analytical specification based on the actual data.

Phase 3 — Initial Data Ingestion
Goals

Build a small, working extraction process.

Potential responsibilities:

Request data from public sources

Parse responses

Handle timestamps

Validate responses

Store raw observations

Handle basic failures

The initial implementation should be intentionally small.

The goal is to establish a reliable path from:

Public Data Source
        ↓
Extraction
        ↓
Raw Data

Phase 4 — Data Storage
Goals

Determine an appropriate storage solution for the analytical workload.

Potential components may include:

Relational database

Raw data storage

Structured analytical tables

Metadata about ingestion

Timestamped observations

The exact database and schema should be selected based on project requirements rather than predetermined for the sake of complexity.

Phase 5 — Transformation
Goals

Transform raw data into analysis-ready datasets.

Potential tasks:

Cleaning

Type conversion

Timestamp normalization

Deduplication

Validation

Joining datasets

Aggregation

Historical baseline calculation

Current-versus-historical comparison

The transformations should be reproducible.

Phase 6 — Exploratory Analysis
Goals

Investigate whether the data actually supports the expected analytical story.

Explore:

Temporal patterns

Spatial patterns

Station-level patterns

Historical distributions

Current conditions

Variability

Potential anomalies or deviations

This phase may result in changes to the analytical methodology.

That is expected.

Phase 7 — Analytical Dataset

Create a clean dataset or set of datasets specifically designed to support the BI layer.

Potential outputs include:

Historical mobility metrics

Current mobility metrics

Historical baselines

Deviation metrics

Station-level metrics

Geographic metrics

The analytical model should prioritize clarity and usability.

Phase 8 — BI Dashboard
Goals

Build an interactive BI experience that answers the project's questions.

The dashboard should likely include:

Overview

Current conditions

Key analytical findings

Historical context

Historical Patterns

Time-of-day patterns

Day-of-week patterns

Geographic patterns

Current Versus Historical

Current values

Historical baseline

Deviations

Locations requiring attention

Station Detail

Where supported by the data:

Current station condition

Historical pattern

Current versus historical comparison

Recent observations

Interactive Map

Include a map if it provides analytical value.

Possible functionality:

Select stations

Inspect current conditions

View deviations

Filter by time/system

Connect geographic selection to analytical views

Phase 9 — Validation

Validate both the data system and analytical results.

Data Validation

Check:

Missing data

Duplicate records

Invalid values

Timestamp issues

Feed failures

Unexpected schema changes

Identifier changes

Data freshness

Analytical Validation

Check:

Baseline calculations

Aggregations

Comparability of time periods

Deviation calculations

Edge cases

Whether visualizations accurately represent the underlying data

Phase 10 — Documentation

Document:

Project motivation

Analytical questions

Data sources

Data architecture

Pipeline

Data model

Analytical methodology

BI design

Data-quality decisions

Limitations

Lessons learned

The README should eventually provide a concise overview suitable for a portfolio/GitHub visitor.

Phase 11 — Portfolio Preparation

The final project should communicate:

Analytics

Ability to formulate analytical questions

Ability to work with historical and current data

Ability to create meaningful metrics

Ability to interpret results

BI

Ability to design an analytical dashboard

Ability to communicate findings visually

Ability to use interactive filtering

Ability to use geographic visualization appropriately

Data Engineering

Ability to extract data from public sources

Ability to build a repeatable ingestion process

Ability to store and transform data

Ability to validate data

Understanding of basic pipeline architecture

The project should remain primarily an analytics/BI project rather than becoming a full-scale data engineering system.

Development Order

The intended high-level progression is:

Project Setup
      ↓
Data Source Investigation
      ↓
Analytical Design
      ↓
Initial Ingestion
      ↓
Storage
      ↓
Transformation
      ↓
Exploratory Analysis
      ↓
Analytical Dataset
      ↓
BI Dashboard
      ↓
Validation
      ↓
Documentation
      ↓
Portfolio Presentation


This is a proposed sequence, not a rigid requirement.

The implementation plan should be updated as new information about the data and analytical requirements is discovered.