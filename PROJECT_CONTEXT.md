Toronto Mobility Reliability — Project Context
Project Overview

Toronto Mobility Reliability is a portfolio project focused primarily on data analytics and business intelligence, with meaningful supporting data engineering work.

The project uses publicly available data from:

Toronto Transit Commission (TTC)

Bike Share Toronto

The project investigates historical mobility patterns and uses current/live operational data to identify conditions that differ from those historical patterns.

The project is intentionally designed as a first substantial data project for a computer science student transitioning toward data analytics, BI, and eventually data engineering.

Central Thesis

The project asks:

Where and when does Toronto's mobility system experience recurring service or availability pressure, and where do current conditions deviate from those expected patterns?

The project does not attempt to create a universal mobility score or force TTC and Bike Share into identical metrics.

Instead, both systems are analyzed using the measurements their public data actually supports.

The shared analytical framework is:

Historical Data
      ↓
Typical Patterns
      ↓
Expected Conditions
      ↓
Current Data
      ↓
Deviation
      ↓
Time + Location + Context

Analytical Questions
Question 1

When and where do TTC service disruptions and Bike Share availability pressures typically occur?

This establishes historical context.

For TTC, this may involve:

Delay frequency

Delay duration

Gap

Time of day

Day of week

Route or line

Station or location

Direction

Incident category

For Bike Share, this may involve:

Trip volume

Time of day

Day of week

Season

Station activity

Origin/destination patterns

Station inflow/outflow imbalance

The final metric definitions must be based on inspection of the actual datasets.

Question 2

Where do current TTC and Bike Share conditions deviate from their expected patterns?

This connects historical analytics with live data.

For Bike Share, current station availability can be compared with historical station activity and/or historically collected station-state observations.

For TTC, current service alerts and supported real-time operational information can be contextualized against historical delay patterns.

The project must not claim that current data measures something that the public feed does not actually measure.

Why Live Data Matters

Live data is not included merely to create an impressive-looking dashboard.

It has an analytical purpose.

Historical data answers:

What normally happens?

Current data answers:

What is happening now?

The project then asks:

How different is the current condition from what we would expect?

Bike Share is particularly suitable for this because its public GBFS station-status feed provides current station state. Repeatedly collecting those observations allows this project to build its own historical record of live station conditions.

TTC also provides current service information, but its real-time feed has documented coverage limitations. These limitations are part of the project and must be documented rather than hidden.

Why TTC and Bike Share Belong Together

TTC and Bike Share do not provide identical data.

That is intentional.

TTC provides a service-reliability case.

Bike Share provides a station-availability case.

The project connects them through a common analytical methodology rather than a fabricated common metric.

TTC
Historical delays → expected service conditions → current service information

Bike Share
Historical activity → expected station conditions → current station availability

Project Priorities

The project should prioritize:

Analytical validity

Data quality

Meaningful questions

Clear BI communication

Appropriate data engineering

Technical sophistication

Technical complexity should not be added unless it serves the analytical requirements.

Intended Skills Demonstrated

The finished project should demonstrate experience with:

Python

SQL

Data cleaning

Exploratory data analysis

Historical/time-series analysis

APIs and public data feeds

Real-time data ingestion

Data validation

Data storage

Data transformation

Analytical data modeling

Business intelligence

Interactive visualization

Geospatial visualization

Git/GitHub

Basic data engineering

Interactive Map

An interactive map is appropriate because location is important to both systems.

The map should support analysis rather than exist purely for visual appeal.

Potential uses include:

Bike Share station availability

Station-level historical/current comparison

Identification of unusual stations

TTC service alerts or supported operational information

Spatial investigation of anomalies

The map should only display information that is analytically meaningful and supported by the data.

Scope

Initial scope:

TTC

Bike Share Toronto

GO Transit is intentionally excluded.

The project is primarily a data analytics / BI project with supporting data engineering, not a dedicated data engineering project.

Guiding Principle

The project must follow the data.

Do not assume a desired metric exists.

Do not force historical and current data to represent the same concept.

Do not hide data limitations.

Do not build technical components simply because they look impressive.

The analytical questions, methodology, and architecture should be derived from the actual characteristics of the available data.