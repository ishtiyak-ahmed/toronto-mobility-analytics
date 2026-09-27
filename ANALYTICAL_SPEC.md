Analytical Specification
1. Core Analytical Framework

The project follows:

Historical Observations
        ↓
Expected / Typical Patterns
        ↓
Current Observations
        ↓
Deviation
        ↓
Investigation


The word expected does not automatically mean a statistical prediction.

A baseline may be:

historical average

median

percentile

distribution

time-of-day baseline

day-of-week baseline

seasonal baseline

The appropriate method must be determined from the data.

2. Question One
When and where do TTC service disruptions and Bike Share availability pressures typically occur?
TTC

Potential dimensions:

Date

Time

Day

Hour

Day of week

Route

Line

Station

Location

Direction

Incident type

Potential measures:

Number of delay incidents

Total delay minutes

Average delay

Median delay

Delay percentiles

Gap-related measures

Potential analyses:

Delay by hour

Delay by weekday

Delay by route/line

Delay by location

Delay by incident type

Seasonal changes

Distribution of delay duration

Do not assume these metrics are all appropriate until the actual datasets are inspected.

Bike Share

Potential dimensions:

Date

Time

Hour

Day of week

Season

Start station

End station

Station location

Potential measures:

Trip count

Departures

Arrivals

Net station flow

Origin/destination volume

Trip duration

Potential analyses:

Demand by hour

Demand by weekday

Station activity

Station inflow/outflow

Seasonal patterns

Commuter versus leisure-like temporal patterns where the data supports such interpretation

3. Question Two
Where do current TTC and Bike Share conditions deviate from expected patterns?

This question requires carefully defining what constitutes a deviation.

Bike Share

Possible approach:

Establish historical station activity patterns.

Establish expected conditions for comparable time periods.

Collect current station status.

Compare current availability with the relevant baseline.

Flag unusual conditions.

Allow the user to investigate the station historically.

Potential concepts:

unusually low bike availability

unusually high bike availability

unusually low dock availability

station imbalance

persistence of an unusual condition

Do not implement these definitions until the historical and live data have been inspected.

TTC

Possible approach:

Establish historical delay/service-disruption patterns.

Retrieve current service information.

Identify active/current conditions.

Provide historical context where a meaningful comparison exists.

Clearly distinguish live observations from historical delay measures.

TTC real-time limitations must be incorporated into the methodology.

4. Deviation Methodology

A deviation should be interpretable.

For example:

Current Value
      -
Expected Value
      =
Absolute Deviation


or:

Current Value / Expected Value


or a percentile-based approach.

The correct method depends on the variable.

Avoid arbitrary anomaly scores without an analytical justification.

5. Historical Baselines

A baseline must account for relevant temporal structure.

Potential comparison groups:

Same hour

Same weekday

Same season

Weekday versus weekend

Comparable station

Comparable operating period

The project must avoid comparing fundamentally different operating conditions.

For example, comparing a Monday 8 AM observation against an unconditional yearly average may be misleading.

6. Geographic Analysis

Location is an analytical dimension.

Potential spatial units:

TTC

Route

Line

Station

Recorded delay location

Bike Share

Station

Station cluster

Geographic area where justified

Maps should allow users to investigate analytical results.

A map is not itself an analytical conclusion.

7. Dashboard Structure

Potential BI structure:

Overview

Current system snapshot

Key historical context

Current unusual conditions

Links into deeper analysis

Historical Patterns

TTC delay patterns

Bike Share activity patterns

Time trends

Geographic patterns

Current Conditions

Current Bike Share station state

Current TTC service information

Current deviations where supported

Map

Spatial investigation

Station-level details

Current condition

Historical context

Detail View

Potentially:

Selected station/route

Historical distribution

Current observation

Expected condition

Deviation

Relevant metadata

8. Analytical Integrity Requirements

The project must distinguish:

Observed

Directly present in the source data.

Derived

Calculated from source data.

Inferred

An interpretation supported by evidence but not directly measured.

Unknown

Not supported by available data.

Do not describe inferred information as directly observed.

9. Data Limitations

Important limitations currently known include:

TTC

TTC real-time data has documented coverage limitations, including limitations involving subway real-time location/arrival predictions, Line 6 information, and some alert structure.

Bike Share

The live GBFS station-status feed represents current station state rather than providing an arbitrary historical archive of station states.

Therefore, this project should collect timestamped live observations if historical station-state analysis is required.

Cross-Mode Comparability

TTC and Bike Share should not be reduced to one common numerical mobility score.

Their metrics and data-generating processes differ.

The common framework is methodological:

historical pattern → expected condition → current observation → deviation

10. Success Criteria

The analysis is successful if a user can answer:

What are the major historical patterns?

When and where does pressure typically occur?

What is happening currently?

Is the current condition unusual?

How unusual is it?

Where is it occurring?

What historical context explains the result?

What limitations affect the interpretation?

The dashboard should not merely answer:

"What is happening right now?"

It should help answer:

"How does what is happening now compare with what normally happens?"