# Purpose — Instruct — throughline source

This document is **generated from the graph** by `tl docs`; `tl docs --check` gates
it in CI. The prose headings are hand-owned — everything between `tl:*` markers is
injected from the YAML items, so the published spec can never drift from the graph.

This source is the **genre / purpose axis** for one purpose: **instruct**. It governs
what the writing is *for* — guiding the reader through the actions needed to reach a
successful outcome — not readability, spelling, punctuation, tone/register, medium or
brand voice, each of which is its own throughline source. Purpose variants are
mutually exclusive: **inform**, **instruct** and **persuade** are sibling sources and
a consumer composes exactly one under the `purpose` namespace. Every principle is a
`user_requirement`; every rule is a `system_requirement` that `implements` its
principle. The throughline UIDs are this source's own and immutable — a consumer cites
a rule as `purpose:SR-0001`.

It carries
<!-- tl:count type == 'user_requirement' -->
5
<!-- tl:end --> principles and
<!-- tl:count type == 'system_requirement' -->
10
<!-- tl:end --> rules.

## Purpose

<!-- tl:item INT-0001 -->
**INT-0001 — Text enables the reader to complete a task correctly** — `intent`, status `approved`

> Instructing means guiding the reader through the actions needed to reach a successful outcome. It suits how-to guides, procedures, setup steps and form help, where the reader needs to do rather than merely to know. This axis governs the communicative purpose — task completeness and sequencing — not readability, spelling, punctuation or register, each of which is a separate source. Purpose variants are mutually exclusive: a consumer composes exactly one of the inform, instruct or persuade sibling sources.

**source_ref**: TBS Purpose — Instruct
<!-- tl:end -->

## 1. Set out the outcome and when the task applies

<!-- tl:item UR-0001 -->
**UR-0001 — Set out the outcome and when the task applies** — `user_requirement`, status `approved`

> Tell the reader what they will achieve and when to use these instructions.

*Derives from:* INT-0001

**source_ref**: TBS Purpose — Instruct — Outcome and scope
<!-- tl:end -->

<!-- tl:table attrs.get('principle') == 'UR-0001' -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0001 | system_requirement | approved | Open by stating what the reader will have achieved |
| SR-0002 | system_requirement | approved | State when the procedure applies and when it does not |
<!-- tl:end -->

## 2. State what the reader needs before starting

<!-- tl:item UR-0002 -->
**UR-0002 — State what the reader needs before starting** — `user_requirement`, status `approved`

> Name the prerequisites so the reader does not stall midway.

*Derives from:* INT-0001

**source_ref**: TBS Purpose — Instruct — Prerequisites
<!-- tl:end -->

<!-- tl:table attrs.get('principle') == 'UR-0002' -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0003 | system_requirement | approved | List what the reader must have or do before starting |
| SR-0004 | system_requirement | approved | Name the permissions, tools or information required |
<!-- tl:end -->

## 3. Sequence the actions the reader must take

<!-- tl:item UR-0003 -->
**UR-0003 — Sequence the actions the reader must take** — `user_requirement`, status `approved`

> Give one performable action at a time, in the order to do them.

*Derives from:* INT-0001

**source_ref**: TBS Purpose — Instruct — Sequencing
<!-- tl:end -->

<!-- tl:table attrs.get('principle') == 'UR-0003' -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0005 | system_requirement | approved | Give the steps in the exact order to perform them |
| SR-0006 | system_requirement | approved | Limit each step to a single action |
<!-- tl:end -->

## 4. Guide the reader through decisions and branches

<!-- tl:item UR-0004 -->
**UR-0004 — Guide the reader through decisions and branches** — `user_requirement`, status `approved`

> Tell the reader how to handle conditions and choices.

*Derives from:* INT-0001

**source_ref**: TBS Purpose — Instruct — Decisions and branches
<!-- tl:end -->

<!-- tl:table attrs.get('principle') == 'UR-0004' -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0007 | system_requirement | approved | State the condition before the action that depends on it |
| SR-0008 | system_requirement | approved | Tell the reader how to decide, not just the options |
<!-- tl:end -->

## 5. Let the reader confirm success and recover from failure

<!-- tl:item UR-0005 -->
**UR-0005 — Let the reader confirm success and recover from failure** — `user_requirement`, status `approved`

> Tell the reader how to check it worked and what to do if it did not.

*Derives from:* INT-0001

**source_ref**: TBS Purpose — Instruct — Verification and recovery
<!-- tl:end -->

<!-- tl:table attrs.get('principle') == 'UR-0005' -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0009 | system_requirement | approved | Tell the reader how to confirm the task succeeded |
| SR-0010 | system_requirement | approved | State what to do if a step fails |
<!-- tl:end -->
