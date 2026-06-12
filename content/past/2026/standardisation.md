---
title: Standardisation & Tooling
linkTitle: Standardisation & Tooling
---

## Overview

Why we need common formats between conference tools.

## The problem

Everyone customizes tools differently. Speakers fill out different forms for different conferences. Volunteers learn different systems each time.

Pretalx deployments look different at every event. Some places have custom systems. Some string together multiple tools with no common interface.

Goal: tools that work like Unix. Simple, reusable, things talk to each other.

## Schedule2

Latest effort to create a standard format for event schedules:
<https://github.com/voc/schedule>

Uses LinkML (write as YAML, generates other formats). Focuses on events and submissions first.

CCC already has a first implementation:
<https://git.cccv.de/hub/hub/-/merge_requests/1499>

Old schedule.xml didn't handle unpublished talks or ID collisions across different sources. Schedule2 fixes that.

Doesn't cover volunteers or other domains yet.

## Other schema efforts

- Person and organization data: <https://github.com/public-value-tech/rpoc/tree/main/schema>
- Inventory tracking: <https://inventree.org>

## Why this is hard

Everyone thinks their event is special and needs custom tools. Sometimes true. Sometimes just easier to build your own than learn someone else's.

Result: constant wheel reinvention.

Smaller events can't build from scratch, so they use whatever big events use even if it doesn't fit well.

## Current standards

- **Pentabarf** - Kind of a standard but informal
- **CCC formats** - Used by CCC events
- **Openki** - Congress experimented with it

## What's next

Schedule2 finishing first release, then opening to more events. Eventually support beyond events and submissions.

The goal: conference organizers share tools and knowledge instead of everyone building from scratch.
