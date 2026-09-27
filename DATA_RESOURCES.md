Data Resources
Purpose

This document records the public data sources relevant to Toronto Mobility Reliability.

It distinguishes between:

Verified — supported by official/current documentation.

Needs inspection — source exists, but the actual files/feed schema still needs to be inspected locally.

Unknown — should not be assumed until verified.

TTC
TTC Historical Subway Delay Data
Status

Verified

Official source

Toronto Open Data — TTC Subway Delay Data.

The dataset is currently refreshed monthly and includes historical files from 2014 onward, including a current file for data since 2025.

Relevant information

The published metadata includes fields such as:

Date

Time

Day

Station

Code

Minimum delay

Minimum gap

Bound

Line

Vehicle

Potential analytical use

Supports historical analysis of:

delay frequency

delay duration

delay timing

station/location

direction

line

incident category

Needs inspection

Before implementation:

Download representative files.

Inspect actual schemas.

Check date/time parsing.

Check missing values.

Check duplicate records.

Check station naming consistency.

Inspect delay distributions.

Inspect code descriptions.

Determine whether schema changes occurred across years.

TTC Bus and Streetcar Delay Data
Status

Verified

Toronto Open Data also provides historical bus/streetcar delay information.

Published documentation describes fields including:

Report date

Route

Time

Day

Location

Incident

Minimum delay

Minimum gap

Direction

Vehicle

Potential analytical use

Supports analysis of:

route-level delay patterns

location-level delay patterns

incident categories

time-of-day patterns

direction

delay duration

Needs inspection

Determine whether including bus and streetcar data improves the project or creates unnecessary scope.

The project does not need to analyze every TTC mode simply because data exists.

TTC Real-Time Information
GTFS-Realtime / Current TTC Operational Information
Status

Verified

TTC provides current service information and real-time data.

Potential information includes:

vehicle/trip updates

arrival-related information where supported

service alerts

operational status

Important limitations

Current TTC documentation/audit identifies limitations including:

real-time subway location and arrival predictions not being included in GTFS-RT

Line 6 real-time information limitations

some custom/unstructured alerts not carrying all structured fields

Therefore the project must not assume complete real-time coverage of the TTC network.

Potential analytical use

current service conditions

current alerts

current supported operational information

historical/current contextualization

Needs inspection

Retrieve and inspect the actual current feed.

Determine:

endpoints

feed format

update frequency

fields

timestamps

identifiers

route/stop coverage

vehicle coverage

alert structure

Bike Share Toronto
Historical Ridership
Status

Verified

The City provides access to historical Bike Share ridership data, with current City material directing users to ridership data from 2014 through 2024.

Potential information

Historical trip records can support:

trip volume

trip timing

start station

end station

trip duration

station activity

origin/destination patterns

Potential analytical use

hourly demand

weekday/weekend patterns

seasonal patterns

station departures

station arrivals

station flow imbalance

Needs inspection

Determine:

exact current historical files

date coverage

schema

station identifiers

timestamp format

missing values

station changes

duplicate records

changes in data definitions

Bike Share Real-Time Station Status
Status

Verified

Toronto Open Data identifies Bike Share Station Information and Status as a real-time dataset containing current station information including:

active stations

bikes available

open docks

Bike Share uses the General Bikeshare Feed Specification (GBFS).

Potential analytical use

current bike availability

current dock availability

station status

current station imbalance

current spatial conditions

Engineering significance

The feed represents current station state.

It does not automatically provide the historical sequence of station states required for long-term historical station-state analysis.

Therefore, this project can periodically collect the live feed and create its own timestamped station-state history.

GBFS
Relevant concepts

GBFS station status supports fields such as:

station ID

station status

bikes available

docks available

station reporting timestamp

feed update timestamp

The specification provides standard concepts for determining feed/station freshness.

Data-quality checks

The ingestion process should validate:

feed timestamp

station timestamp

station ID

bike count

dock count

station status

missing records

unexpected values

Source Selection

The final project should use only the sources necessary to answer the analytical questions.

Potential initial source set:

TTC historical delay data

TTC current service/real-time information

Bike Share historical trip data

Bike Share current GBFS station status

Bike Share station metadata

Additional sources should only be added when they support a defined analytical need.

Data Investigation Requirements

Before final architecture:

Source validation

For each source:

Confirm official publisher.

Confirm current availability.

Confirm licensing.

Confirm refresh behavior.

Download or retrieve sample data.

Schema validation

Determine:

columns

data types

identifiers

timestamps

geographic fields

measures

categorical fields

Quality validation

Check:

nulls

duplicates

invalid values

inconsistent identifiers

timestamp problems

schema changes

station/route changes

Analytical validation

Determine:

What questions can this source answer?

What questions can it not answer?

What derived metrics are legitimate?

What comparisons are valid?

Storage Requirements

The final storage architecture has not yet been selected.

It must support:

historical datasets

repeated live ingestion

raw data preservation

transformed data

analytical queries

reproducible analysis

Candidate technologies may include:

PostgreSQL

DuckDB

Parquet

object/file storage

The final choice should be based on data volume, workload, refresh requirements, simplicity, and learning value rather than prestige.

Source Classification

The project should maintain this distinction:

Verified

The source/documentation confirms the capability exists.

Inspected

The actual downloaded/retrieved data has been examined.

Derived

A value is calculated from source data.

Assumed

A hypothesis about the data that has not yet been validated.

Architecture and analytical decisions should not depend on unverified assumptions.