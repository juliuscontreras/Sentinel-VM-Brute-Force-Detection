# Sentinel-VM-Brute-Force-Detection

## Description
This repository contains materials for setting up Microsoft Sentinel alert rules to detect brute-force attacks targeting Azure virtual machines, along with associated incident response procedures aligned with NIST 800-61.

## Table of Contents
- [Overview](#overview)
- [Setup / Prerequisites](#setup--prerequisites)
- [Contents](#contents)
  - [Documentation](#documentation)
  - [KQL Queries](#kql-queries)
  - [Incident Response](#incident-response)
- [Contributing](#contributing)
- [License](#license)
- [Author](#author)

## Overview
This project demonstrates how to detect and respond to brute-force login attempts on Azure VMs using Microsoft Sentinel and Microsoft Defender for Endpoint (MDE).

The scenario includes:
- Creating alert rules in Sentinel using KQL
- Investigating brute-force attempts
- Performing incident response following the NIST 800-61 lifecycle

## Setup / Prerequisites
- Virtual machine(s) onboarded to Microsoft Defender for Endpoint
- Logs being ingested into Azure Log Analytics workspace connected to Microsoft Sentinel
- Reference material available via Skool or Microsoft documentation for VM onboarding and Sentinel setup

## Contents

### Documentation
- [`Scenario-1-VM-Brute-Forcing.md`](Documentation/Scenario-1-VM-Brute-Forcing.md): Full walkthrough of the brute-force detection lab scenario

### KQL Queries
- [`Brute-Force-Detection.kql`](KQL_Queries/Brute-Force-Detection.kql): Detects failed logon attempts over a specified threshold
- [`Check-Successful-Logons.kql`](KQL_Queries/Check-Successful-Logons.kql): Checks for successful logons from suspicious IPs
- [`NSG-Lockdown.kql`](KQL_Queries/NSG-Lockdown.kql): Placeholder or script to document/automate NSG lockdown (RDP restriction)

### Incident Response
- [`NIST-800-61-Lifecycle.md`](Incident_Response/NIST-800-61-Lifecycle.md): Outlines the incident response process using NIST guidelines

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

## License
MIT License (or replace with preferred license)

## Author
[Your Name or Organization]
