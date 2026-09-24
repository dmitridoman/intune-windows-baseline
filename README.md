# intune-windows-baseline

Sample **illustrative** Windows 11 baseline fragments for a managed school or other shared-device estate. Nothing here is claimed to be copied from a live tenant export.

**Status:** illustrative samples, not a live tenant export.
**Runs on:** nothing: JSON and Markdown to read and recreate in Intune.
**Used by:** IT admins designing a Windows 11 baseline for shared devices.

## What is in this repo

- `policies/configuration/`: JSON shaped like settings catalogue / policy intent (BitLocker, Defender, firewall, local admin posture, authentication strength direction, updates, ASR).
- `policies/compliance/`: sample compliance policy shapes for Windows 11.
- `docs/`: why certain choices exist and what you give up when you tighten the baseline.

## How to use it

Treat the JSON as **documentation and structure**, not something to import blindly. In a real tenant you would recreate these in the Intune admin centre (or via IaC you trust), align to your risk register, and test on a pilot ring before wide assignment.

## What you must change

- Samples use **Harven-style illustrative IDs** (tenant `harvengroup.onmicrosoft.com`, custom domain `harven.co.uk`, tenant ID `a1b2c3d4-e5f6-7890-abcd-ef1234567890`, device prefix `HVN-`). Swap in your real assignments before production use.
- Map settings to your **edition** (e.g. Pro vs Education) and **licensing** (some controls assume certain SKUs).
- Validate **helpdesk impact**: shared devices and classrooms break in boring ways when local admin or credential UX is wrong.

## Disclaimer

These samples are for learning and portfolio context only. You are responsible for compliance with your organisation’s policies and for testing before production rollout.
