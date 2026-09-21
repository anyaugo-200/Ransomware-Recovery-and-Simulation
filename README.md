# Project 04 - Ransomware Simulation and Verified Recovery

## Overview

This project demonstrates a safe incident-response and recovery workflow using a harmless file-disruption simulation in a controlled VirtualBox lab. It shows how to define scope, prepare backups, validate monitoring, preserve evidence, restore files, verify integrity, and communicate limits clearly.

**Evidence report:** [project-04-ransomware-simulation-and-recovery.pdf](project-04-ransomware-simulation-and-recovery.pdf)

## Scope

- Environment: Ubuntu and Kali in a controlled VirtualBox lab
- Simulation type: harmless filename-change exercise using synthetic invoice files
- Evidence: 15 images across numbered project sections
- Classification: public portfolio sample / capability demonstration

This project did not use real ransomware, destructive malware, credential theft, or unauthorized access. Five synthetic invoices were renamed and then restored from backup.

## Verified Result

- Five synthetic invoices were renamed with `.simulated-locked`
- Marked copies were preserved separately
- The archive checksum passed
- All twenty restored invoice files matched the backup manifest
- The first flawed restore attempt was rejected, and the corrected retry used checksum and file verification before reporting success

## Evidence Sections

| Test | Section | What was demonstrated |
| --- | --- | --- |
| 01 | Scope and Authorization | Lab boundary, exclusions, and portfolio scope record. |
| 02 | Lab Setup and Backups | Ubuntu/Kali lab setup, baseline snapshot, archive backup, and pre-exercise checks. |
| 03 | Ubuntu Endpoint Setup | SSH, auditd, and file-monitoring readiness on the Ubuntu endpoint. |
| 04 | File Monitoring and Detection | A controlled file event was recorded with audit evidence. |
| 05 | Alert Review and Reporting | A known benign event was translated into analyst-style business language. |
| 06 | Network Isolation Evidence | Lab connectivity and lack of ordinary default route from the testing workstation were checked. |
| 07 | Simulation Evidence | Five-file disruption simulation using disposable business-like data. |
| 08 | Incident Timeline | Command-output checkpoints before recovery. |
| 09 | Containment and Recovery | Marked copies preserved; five originals restored; all twenty invoices verified. |
| 10 | Final Report and Authorized Client Workflow | Evidence-backed outcome, client workflow, recovery handover, and assurance boundaries. |
| 11 | Privacy and AI Use | Proposed data-handling and AI-use recommendations for client work. |

## Tools Used

- VirtualBox
- Ubuntu
- Kali Linux
- OpenSSH
- auditd and ausearch
- tar
- sha256sum
- shell scripting

## Skills Demonstrated

- Incident response scoping
- Backup and restore validation
- File integrity verification
- Evidence preservation
- Lab network boundary checking
- Detection and analyst reporting workflow
- Business recovery communication
- Clear assurance boundaries

## What Can Be Claimed

The five-file simulation and checked file recovery are complete. No content mismatch was detected across the twenty invoices against the backup manifest.

## What Is Not Claimed

This project does not claim to stop real ransomware, prove zero business data loss, meet a recovery-time objective, isolate a malicious process, or certify a production environment.
