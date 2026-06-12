---
title: Conference Management Software
linkTitle: Conference Management Software
---

## Overview

What tools FOSS conferences actually use and what's broken about them.

### Pretalx

Used by FOSDEM, COSCUP, BalCCon, and many others. Open source. The default choice for most events.

Congress (CCC) runs 11 pretalx instances joined together: <https://git.cccv.de/hub/hub>. This lets different content teams manage their own instances while sharing data. They're also experimenting with Openki: <https://gitlab.com/Openki/Openki>

**Issues:**
- Updates can lose data (BalCCon and OpenFest both reported this)
- CJK language support broken in export features (one of the things Eventyay fixed)
- API, which is a major pain point
- Schedule publishing is immediate. No "ready but not published yet" state.
- Korean translation missing and payment provider integration is hard

**Workarounds:** FOSDEM and others export to YAML and build their own static websites instead of using pretalx directly.

### Eventyay

FOSSASIA's platform: <https://eventyay.com/>

Not really a pretalx fork. Uses some of the code but reimplemented most of it with new database models and new features.

**Includes:**
- CFP and ticketing in one system
- Common login across tickets, badges, talks, and video
- Check-in app
- Volunteer management

GitHub: <https://github.com/fossasia/eventyay>

Fewer organizations use it but it's growing.

### Chemnitzer Linux-Tage

Built their own system from scratch: <https://chemnitzer.linux-tage.de/2026/en>

Django application integrated into their website.

**Features:**
- Building maps and floor plans
- Infrastructure maps (power sockets, etc.)
- Automated tooling via awk scripts and Makefiles
- Handles scheduling, CFP, everything

### P.I.W.O. (Poznań Free Software Fest)

Wanted to use pretalx but couldn't get a Polish translation finished.

Used a commercial but free-tier service for ticketing (not open source). Planning to move to Pretalx next year.

## Current state needs improvement

- Better APIs for integrations
- Better access control (devroom managers see only their devroom, not others)
- Ability to submit a talk to multiple tracks
- More flexible schedule management

## Standardisation

Everyone customizes tools differently. Speakers fill out different forms for different conferences. Volunteers learn different systems each time.

**Schedule2** is trying to create a standard format everyone could use:
<https://github.com/voc/schedule>

Uses LinkML so it's machine-readable. Focuses on events and submissions first.

If it works, speakers submit once and conferences share data. Volunteers move between events without relearning.

## Common issue

Every org thinks their event is special and needs custom tools. Sometimes true, sometimes it's just easier to build your own than learn someone else's. Result: we keep reinventing the wheel instead of building shared tools.
