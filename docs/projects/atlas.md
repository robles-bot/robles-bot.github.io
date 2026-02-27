# ATLAS Tier-3 Analysis Facilities Benchmarking

**Position:** Operations Specialist
**Organization:** US-ATLAS
**Location:** SCIPP, UC Santa Cruz
**Duration:** 2024–2026

---

## Overview

Developed and maintained benchmarking infrastructure for ATLAS Tier-3 Analysis Facilities across four major computing sites in the United States:

| Site | Institution |
|------|-------------|
| **UC** | University of Chicago |
| **BNL** | Brookhaven National Laboratory |
| **SLAC** | Stanford Linear Accelerator Center |
| **NERSC** | National Energy Research Scientific Computing Center |

## Benchmarking Framework

### Job Types

| Job Type | Purpose |
|----------|---------|
| **Rucio Download** | Network connectivity benchmark for data retrieval |
| **EVNT** | Event generation job |
| **TRUTH3** | DAOD-style output through ATHENA Transform |
| **Ntuple-to-Hist** | Histogram generation using multiple analysis frameworks |

### Analysis Frameworks Compared

- **Coffea** - Columnar analysis framework
- **func_adl (FF)** - Functional analysis description language
- **EventLoop** - ATLAS standard analysis framework (columnar and standard variants)

## Infrastructure

### Monitoring Pipeline

```
Job Execution → Log Parsing → Elasticsearch → Kibana Dashboard
```

Developed parsing scripts to:

1. Extract metrics from benchmark job logs
2. Compare against previously sent entries
3. Send new data to Elasticsearch
4. Visualize results in Kibana dashboards

### Automation

| Site | Scheduling Method |
|------|-------------------|
| UC | GitHub Actions via Kubernetes/Flux |
| BNL | Crontab |
| SLAC | Crontab |
| NERSC | Scrontab |

### UC Kubernetes Setup

Configured automated job scheduling using:

- **Flux** with Helm for GitOps
- **GitHub App** for repository permissions
- **ArcRunners** for job execution
- Log files uploaded as GitHub artifacts

## Key Accomplishments

- Deployed benchmarking jobs across all four Tier-3 sites
- Implemented parsing scripts for automated metric collection
- Set up Kibana dashboards for performance visualization
- Configured Kubernetes/Flux automation at UC
- Created MkDocs documentation site with workflow flowcharts
- Tested across multiple environments (Native, EL9, CentOS7)
- Served on University of Chicago admin team for user account approvals

## Technical Skills

- **Languages:** Python, Bash
- **Infrastructure:** Kubernetes, Flux, GitHub Actions, Crontab
- **Data Pipeline:** Elasticsearch, Kibana
- **HPC Systems:** NERSC, BNL clusters, SLAC computing
- **ATLAS Tools:** Rucio, ATHENA, Coffea, func_adl, EventLoop
- **Containers:** Singularity/Apptainer

## Acknowledgments

This work was conducted as part of the **US-ATLAS** collaboration, supporting the computing infrastructure for the ATLAS experiment at CERN's Large Hadron Collider.
