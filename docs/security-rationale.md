# Security rationale

Short version: these controls exist to reduce **opportunistic compromise**, **silent data loss**, and **unmanaged drift** on estates where devices are shared, borrowed, or touched by lots of hands.

## Encryption (BitLocker)

If a device walks out of a building, encryption is the difference between an asset loss and a data breach conversation. Schools still handle identifiable data; finance and insurance are stricter. BitLocker is the boring baseline that supports that reality.

## Antimalware (Defender)

You want consistent AV on, signatures reasonably fresh, and tamper protection considered (not duplicated in these samples — add it in real life). The goal is not “perfect detection”; it is **uniform coverage** so you are not hunting one-off machines running whatever the student installed.

## Firewall

Host firewall is a cheap layer against lateral noise and random inbound rubbish. The point is consistent defaults, not pretending it replaces network segmentation.

## Local admin restrictions

Local admin is how ransomware and persistent junk spreads on shared machines. Removing it hurts convenience; keeping it without a controlled alternative hurts everyone eventually.

## Stronger authentication direction

Reusable passwords lose to phishing. The direction is to move high-value accounts to stronger factors and reduce admin reliance on passwords. Device policies should not fight Conditional Access — they should support the same story.

## Attack surface reduction

ASR targets common malware chains (Office spawning processes, suspicious child processes, etc.). It is effective and occasionally breaks legitimate software. That is why audit mode exists.

## Compliance

Compliance is not “security”; it is a **measurable minimum bar** so reporting and conditional access can trust a baseline. If you set rules you cannot enforce, you train people to ignore the dashboard.

## Updates

Most commodity attacks are easier on stale builds. Update rings exist so you can patch fast without pretending every device can take change on the same day.
