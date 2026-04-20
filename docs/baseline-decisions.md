# Baseline decisions (plain English)

This is the sort of notes you write after the third meeting where someone asks why laptops are “slower” after hardening.

## Shared devices vs staff devices

**Tradeoff:** Tighter baselines reduce malware and casual misuse; they also increase helpdesk load when a teaching app needs elevation, odd firewall holes, or legacy USB kit.

**What I usually do:** Split baselines. Staff get stricter ASR and faster update deadlines. Teaching floor devices get longer deferrals during term and more exclusions — but exclusions are named, time-bounded, and owned by someone.

## BitLocker

**Tradeoff:** Encryption is non-negotiable for lost-device risk; recovery key flow is where projects die.

**Reality:** If escrow is wrong, you are either wiping machines or paying for ugly data recovery stories. Pilot BitLocker before you widen assignment, especially on mixed firmware estates.

## Defender and ASR

**Tradeoff:** Defender defaults are fine for many estates; ASR is where productivity hits.

**Reality:** Start in audit. If you jump straight to block mode because a checklist said so, you will learn more about legacy macros than you wanted.

## Firewall

**Tradeoff:** Default deny inbound is correct for most classroom PCs; multicast discovery and random vendor installers disagree.

**Reality:** Document the three apps that always need exceptions. Otherwise you get “IT disabled the network” when it is just UDP being UDP.

## Local admin

**Tradeoff:** Removing local admin fixes a lot; it also breaks quick fixes in classrooms.

**Reality:** Pair restrictions with LAPS (or your approved elevation process). A shared local password is a incident waiting to happen — it always leaks.

## Authentication direction

**Tradeoff:** Phishing-resistant credentials are great; not every account type or device tier supports them cleanly on day one.

**Reality:** Align Intune device settings with what Conditional Access actually enforces. Device policy without CA is half a story.

## Compliance

**Tradeoff:** Strict compliance sounds good in audits; if remediation is slow, you just create noisy non-compliance.

**Reality:** Each rule should have an owner and a fix path: policy change, wipe, replace, or exception with expiry.

## Updates

**Tradeoff:** Aggressive deadlines patch faster; they also reboot during lessons if you are careless.

**Reality:** Tie rings to the academic calendar. Exam weeks are not the time to discover your restart grace period is wrong.
