# TeleWeave
### Project Overview

**Project Type:** Data Engineering Platform  
**Domain:** Telecommunications and Financial Data  
**Status:** Planning and Design  
**Academic Context:** WeThinkCode_ Data Engineering Capstone 2026

---

## 1. Introduction

TeleWeave is an end-to-end telecommunications data engineering platform designed to ingest, process, store and analyse data from multiple sources.

The platform models a fictional telecommunications provider, combining cellular usage records, customer information and foreign exchange data to generate meaningful operational and analytical insights.

TeleWeave demonstrates how data engineering technologies can work together to transform raw information into structured, reliable and accessible data.

## 2. Problem Statement

Telecommunications providers generate large volumes of data from customer interactions, mobile network activity and financial transactions.

When this information is distributed across different systems, obtaining a unified view of customer activity and network usage becomes challenging.

TeleWeave aims to address this problem by creating interconnected data pipelines that support near-real-time processing, persistent storage, usage analysis and reporting.

## 3. Project Objectives

The objectives of TeleWeave are to:

1. Build reliable pipelines that ingest data from multiple sources.
2. Process streaming events and calculate customer usage statistics.
3. Store raw and processed information in appropriate databases.
4. Generate analytical datasets for customer, network and financial insights.
5. Expose selected information through an authenticated REST API.
6. Implement automated tests and reproducible deployment processes.
7. Demonstrate a maintainable, observable and well-documented data engineering architecture.

## 4. Data Sources

The platform will work with three primary data sources defined in the capstone curriculum.

| Source | Description |
|---|---|
| Call Data Records (CDR) | Voice calls and mobile data usage, delivered as CSV files through SFTP |
| Customer Relationship Management (CRM) | Customer accounts, addresses and connected devices maintained in PostgreSQL |
| Foreign Exchange (Forex) | Simulated currency exchange ticks for MRVZAR and WAKMRV, published to Redpanda |

## 5. Curriculum Deliverables

The WeThinkCode_ curriculum identifies seven software deliverables:

1. **CDR Ingestion:** Transfer CDR records from SFTP into Redpanda.
2. **CRM Change Data Capture:** Stream CRM database changes into Redpanda.
3. **CDR Stream Processing:** Calculate daily usage and billing statistics per MSISDN, targeting processing latency below 60 seconds.
4. **High-Velocity Store:** Store processed usage information for efficient retrieval.
5. **Usage REST API:** Provide authenticated access to daily usage statistics.
6. **Persistence:** Store source data from Redpanda and SFTP in the relevant PostgreSQL databases.
7. **Prepared Analytical Layers:** Transform raw stored data into structured datasets.

The prepared analytical layers cover four outputs:

- CDR usage summaries at 15-minute, 30-minute and hourly intervals.
- Cell tower interaction sessions per customer.
- Hourly customer and device summaries with accumulated usage charges.
- Forex OHLC summaries for M1, M30 and H1 intervals, including EMA and ATR indicators using 8-period and 21-period lookbacks.

## 6. Engineering and Quality Requirements

The curriculum also specifies:

- Python as the preferred programming language.
- Unit tests for all developed code.
- Scripts for setting up virtual environments, installing dependencies and executing tests.
- Deployment scripts for application initialisation, startup and graceful shutdown.
- A technical demonstration and presentation of the solution.

Containerisation, structured logging, metrics, alert definitions and architectural resilience are recommended improvements.

## 7. Proposed Project Scope

TeleWeave will be developed incrementally through five milestones:

| Milestone | Focus |
|---|---|
| 01. Planning & Setup | Requirements, architecture, development environment and testing foundations |
| 02. Data Ingestion | CDR pipelines and CRM change capture |
| 03. Stream Processing & APIs | Persistence, streaming calculations, high-velocity storage and REST API |
| 04. Data Transformation & Analytics | Prepared analytical datasets |
| 05. Monitoring, Deployment & Demo | Observability, documentation, deployment and demonstration |

The order of implementation may change as dependencies, resources and team priorities are clarified.

## 8. Future Enhancements

Once the core curriculum deliverables are functional, potential enhancements may include:

- An interactive analytics dashboard.
- Additional visualisations of telecommunications usage.
- Expanded data-quality monitoring.
- Additional performance and reliability testing.

These features are **optional extensions**, not curriculum requirements.

## 9. Development Approach

TeleWeave will follow an iterative development process:

**Understand → Design → Implement → Test → Document → Commit**

Each deliverable will have a corresponding GitHub issue with defined acceptance criteria.

The project will be developed with emphasis on correctness, maintainability, clear technical reasoning and reproducibility.

---

**Project Repository:** https://github.com/beko-1enkosi/teleweave

**Reference:** WeThinkCode_ Data Engineering Project Curriculum, 2026.