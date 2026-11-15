# Commission 4 - Ryan Minor

CS4320 Software Design | November 14, 2026

## Individual architectural design defense

[Design Assessment Report 4 (PDF)](Ryan_Minor_Design_Assessment_Report_4.pdf)

[Editable report text](Ryan_Minor_Design_Assessment_Report_4.txt)

The report evaluates the shared Nexus deactivation audit design, including the file-backed persistence extension, alternatives, tradeoffs, reviewer concerns, and verification limits. It includes a short code and output appendix plus source links.

## Implementation and actual evidence

- [Lifecycle service and audit protocol](../nexus2/src/northstar/services.py)
- [In-memory and file-backed audit stores](../nexus2/src/northstar/audit.py)
- [Notification behavior](../nexus2/src/northstar/notifications.py)
- [Lab wiring](../nexus2/lab/adapter.py)
- [Ten contract checks](../nexus2/lab/test_contract.py)
- [Shared lab evidence and persistence update](../evidence.md)
- [Fresh November 14 contract output: 10 tests OK](verified-contract.txt)
- [Fresh November 14 regression output: 23 passed](verified-regression.txt)

Verification used an isolated snapshot of team commit 8f2fdae with Python 3.12.1. From nexus2, commands were `python3 -B run_lab.py` and `python3 -B -m pytest tests`; both exited 0. Fresh-instance persistence is tested; the report's separate-process check remains proposed. Crash durability, concurrency, and production file security are not established.

## Attribution and submission

Ryan Minor and Jacob Yepez collaborated on the lab. Jacob supplied the initial audit component and later persistence extension; Codex assisted with integration, verification, evidence organization, and report preparation. Team source: [presidentjacob/Nexus_Coding_Lab](https://github.com/presidentjacob/Nexus_Coding_Lab), [merged PR #1](https://github.com/presidentjacob/Nexus_Coding_Lab/pull/1).

This folder provides the individual report and inspectable implementation/evidence link. It does not claim that PR4 or the portfolio Google Doc was submitted. Submit the report PDF in the existing Canvas DA4 assignment as directed; the portfolio remains in the existing Google Doc.
