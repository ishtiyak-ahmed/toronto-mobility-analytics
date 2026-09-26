Toronto Mobility Analytics
Project Overview

Toronto Mobility Analytics is a data analytics and business intelligence project that uses TTC and Bike Share Toronto data to analyze how Toronto's mobility conditions change across time and location.

The project is intentionally designed as a data analytics / BI project first, while incorporating a meaningful amount of data engineering through the collection, storage, cleaning, transformation, and validation of live transportation data.

The project should demonstrate that the developer can work with both:

Historical transportation data

Continuously updated or live transportation data

Structured and semi-structured data

Time-series data

Location-based data

Analytical databases

Interactive BI visualizations

The project should answer analytical questions rather than simply display transportation information.

Project Thesis

The central idea is to compare current mobility conditions with historical patterns.

Historical data establishes what is normally expected for a particular transportation context, such as a location, time of day, or day of week. Live data allows the project to determine what is happening now and whether current conditions resemble, differ from, or deviate from those historical patterns.

This creates a natural relationship between the analytics and data engineering components:

Historical data provides context and baselines.

Live data provides current observations.

Data engineering processes collect and organize both types of data.

Analytical transformations make the datasets comparable.

Analytics identifies meaningful differences and patterns.

BI visualizations communicate those findings interactively.

The project should therefore demonstrate more than the ability to build a dashboard. It should demonstrate the ability to build a small analytical data system and use it to answer meaningful questions.

Transportation Systems

The project will focus on two transportation systems:

TTC

Bike Share Toronto

GO Transit will not be included in the initial scope.

The two systems were selected because they provide different but related views of urban mobility.

TTC

TTC data can provide information about transit service, routes, vehicles, stops, schedules, and/or real-time service conditions depending on the available public datasets.

Bike Share Toronto

Bike Share data can provide information about stations, available bikes, available docks, station capacity, and station status over time depending on the available public feeds.

The project should use the actual available public datasets rather than assuming that every desired metric is available.

Primary Analytical Questions

The project should revolve around two closely connected questions.

Question 1 — What does typical mobility look like?

How do mobility patterns vary across time and location for TTC and Bike Share Toronto?

This question establishes the historical context.

The analysis should investigate patterns such as:

Hour of day

Day of week

Weekday versus weekend

Location

Transportation system

Route or station where appropriate

Seasonal patterns where sufficient historical data exists

The goal is to understand what normal or typical conditions look like rather than simply reporting raw counts.

Question 2 — How do current conditions compare with those patterns?

How do current TTC and Bike Share conditions compare with their historical patterns, and where are the largest deviations occurring?

This question connects the historical analysis to the live-data component.

The analysis should investigate:

Current conditions

Historical expectations for comparable periods

Differences between current and historical conditions

Locations experiencing unusual conditions

Time periods experiencing unusual conditions

Magnitude and persistence of deviations where the data supports it

The exact definition of "deviation" must be determined during the analytical design phase rather than arbitrarily chosen.

Why These Questions Work Together

The questions form a single analytical progression:

Historical Data
      ↓
Understand Typical Patterns
      ↓
Establish Historical Baselines
      ↓
Collect Current Data
      ↓
Compare Current Conditions
      ↓
Identify Meaningful Deviations
      ↓
Investigate Where and When They Occur


The project therefore does not consist of unrelated TTC and Bike Share analyses.

Instead, both systems contribute to the same broader investigation:

Understand normal mobility patterns and use live data to determine how current conditions compare with those patterns.

Data Strategy

The project should use both historical and live/current data where available.

Historical Data

Historical data will be used to:

Identify recurring patterns

Establish analytical baselines

Compare different time periods

Understand spatial differences

Provide context for current observations

Live Data

Live or frequently updated data will be used to:

Capture current transportation conditions

Demonstrate automated data extraction

Create observations that can be compared against historical data

Support future refreshes of the analytical system

The project should avoid treating live data as merely a visual feature. Its purpose is to support the central analytical question.

Interactive Map

An interactive map should be included if it contributes to the analysis.

The map is not required simply because the developer has a CS/frontend background.

Potential uses include:

Showing Bike Share stations geographically

Showing current station conditions

Highlighting locations with unusually high or low availability

Showing TTC-related locations or spatial patterns where the data supports it

Allowing users to select a location and inspect its historical/current context

The map should answer or support an analytical question.

It should not become a decorative frontend feature disconnected from the analysis.

Station-Level Analysis

Bike Share station-level analysis is expected to be an important part of the project.

A station detail view may allow a user to investigate:

Current station status

Historical station behavior

Typical availability

Differences between current and historical conditions

Relevant time-of-day patterns

Other metrics supported by the data

The exact metrics should be determined after examining the available data.

Data Engineering Scope

This is not intended to be a dedicated data engineering project.

However, the project should contain enough engineering work to demonstrate that the developer can work with real-world data pipelines.

Potential components include:

Extracting data from public APIs or feeds

Handling live/frequently updated data

Storing raw observations

Cleaning and transforming data

Handling timestamps and time zones

Deduplicating records where necessary

Validating incoming data

Loading data into an analytical database

Creating reproducible transformations

Supporting repeated data refreshes

The engineering architecture should remain proportional to the project's primary goal: analytics.

BI / Visualization Goals

The final BI layer should communicate analytical findings rather than simply expose raw data.

Potential visualizations include:

Historical time-series trends

Hour/day heatmaps

Historical versus current comparisons

Deviation indicators

Station-level analysis

Geographic visualizations

Filters for date, time, transportation system, and location

The final dashboard should help a user answer the project's analytical questions without requiring them to inspect raw data.

Technical Learning Goals

By completing this project, the developer should gain practical experience with:

Python for data work

APIs and public data feeds

JSON and other structured/semi-structured data

Data ingestion

Data cleaning

SQL

Relational databases

Time-series analysis

Data validation

Historical baselines

Comparative analysis

BI/dashboard development

Geospatial visualization

Git and GitHub

Basic data pipeline design

The developer should understand the reasoning behind the implementation rather than merely reproducing generated code.

Scope Principles

The project should follow these principles:

Analytics comes first.

Every major component should support an analytical purpose.

Live data should be used meaningfully, not simply because it looks impressive.

Historical and current data should be comparable.

The available public data should determine what can actually be analyzed.

Technical complexity should serve the analytical goal.

The project should remain achievable as a first data project.

The final system should be explainable in an internship interview.

AI may assist with implementation, but the developer must understand the resulting system.

The project should prioritize depth over unnecessary feature count.