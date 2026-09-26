Analytical Specification
Purpose

This document defines the analytical direction of the Toronto Mobility Analytics project.

The project should answer questions about typical mobility patterns and current deviations from those patterns using TTC and Bike Share Toronto data.

The exact metrics and methodology should be refined after investigating the actual public datasets.

Analytical Framework

The project follows a two-stage analytical framework:

Stage 1
Understand historical mobility patterns
            ↓
Stage 2
Compare current conditions against those patterns


This prevents the project from becoming a collection of disconnected charts.

Question 1: Historical Mobility Patterns
Primary Question

How do mobility patterns vary across time and location for TTC and Bike Share Toronto?

Objective

Determine what typical conditions look like across different temporal and geographic contexts.

Dimensions

Potential dimensions include:

Transportation system

Date

Hour

Day of week

Weekday/weekend

Month or season

Station

Route

Geographic area

Only dimensions supported by the available data should be used.

Potential Analysis

Depending on the available datasets, analysis may include:

Average or median conditions by hour

Conditions by day of week

Weekday versus weekend comparisons

Temporal heatmaps

Station-level patterns

Route-level patterns

Seasonal changes

Spatial concentration of activity

Variability between locations

Important Consideration

"Typical" must be defined explicitly.

Possible approaches include:

Mean

Median

Percentiles

Historical distributions

Rolling statistics

The appropriate method should be determined based on the characteristics of the data.

Question 2: Current Conditions Versus Historical Patterns
Primary Question

How do current TTC and Bike Share conditions compare with their historical patterns, and where are the largest deviations occurring?

Objective

Use live/current observations together with historical data to identify conditions that differ meaningfully from what would normally be expected.

Comparison Framework

Conceptually:

Current Observation
        ↓
Identify Comparable Historical Context
        ↓
Historical Baseline
        ↓
Compare
        ↓
Measure Deviation
        ↓
Identify Locations / Periods of Interest


A current observation should not be compared against an arbitrary historical average.

For example, a current Monday at 8:00 AM should ideally be compared against appropriate historical Monday 8:00 AM observations rather than all historical observations.

The exact comparison groups should be determined during implementation.

Historical Baseline

A baseline represents the expected or typical value for a comparable historical context.

Potential baseline dimensions include:

Location

Hour

Day of week

Weekday/weekend

Season

Transportation system

The baseline methodology must account for the available amount and quality of historical data.

Deviation

A deviation represents the difference between a current observation and its historical expectation.

Possible approaches include:

Absolute Difference
Current Value - Historical Baseline

Relative Difference
(Current Value - Historical Baseline)
-------------------------------------
Historical Baseline

Standardized Difference

Where appropriate, the analysis could account for historical variability rather than only comparing against a central value.

The final methodology should be selected after examining the data.

The project should avoid inventing a sophisticated statistical method merely to appear advanced.

Cross-System Analysis

TTC and Bike Share should be analyzed as two transportation systems contributing to the same mobility question.

The project should not force direct comparisons between metrics that do not measure the same thing.

Instead, the systems can be compared at the level of:

Temporal patterns

Spatial patterns

Current versus historical behavior

Locations experiencing unusual conditions

Changes across time

Where metrics are not directly comparable, the dashboard should clearly communicate that distinction.

Potential Analytical Outputs

The final analysis may include:

Historical Pattern Views

Mobility patterns by hour

Mobility patterns by day of week

Weekday/weekend differences

Historical station behavior

Geographic patterns

Current Condition Views

Current system conditions

Current station conditions

Current conditions by location

Recent changes

Comparison Views

Current versus historical baseline

Absolute deviation

Relative deviation

Locations with unusual conditions

Time periods with unusual conditions

Station-Level Investigation

For Bike Share stations, the analysis may support a detailed station view.

A station detail page/view could show:

Current station conditions

Historical typical conditions

Current versus historical difference

Historical patterns by hour

Historical patterns by day of week

Recent observations

Geographic context

The exact station metrics depend on the available public data.

Geographic Analysis

Geography should be used where it provides analytical value.

Potential geographic analysis includes:

Station-level maps

Spatial distribution of activity

Current availability by location

Historical patterns by location

Locations with unusually high deviations

An interactive map should not exist independently of the analytical framework.

Data Quality Requirements

Before analytical results are trusted, the project should investigate:

Missing records

Duplicate records

Invalid values

Timestamp consistency

Time zone handling

Changes in station identifiers

Changes in station capacity

Feed outages

API failures

Unexpected values

Historical coverage

Data-quality decisions should be documented.

Analytical Validation

The developer should be able to explain:

What each metric measures

Why each metric was selected

How historical baselines are calculated

How current observations are matched to historical contexts

How deviations are calculated

What limitations exist

What conclusions the data does and does not support

The project should distinguish between:

Observed facts

Calculated metrics

Analytical interpretations

Assumptions

Final Analytical Story

The final dashboard and project documentation should communicate a coherent story:

What normally happens?
        ↓
Where and when does it happen?
        ↓
What is happening now?
        ↓
How does now compare with normal?
        ↓
Where are the largest differences?
        ↓
What patterns can we observe?


This progression should be reflected in the final BI experience.