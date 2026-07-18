# throughline-purpose-instruct

The **instruct** purpose of the **genre / purpose** content axis, expressed as a
[throughline](https://pypi.org/project/throughline/) **source** — a standalone,
grounded requirements graph that a consuming project composes with
[throughline-compose](https://github.com/timebacksolutions/throughline-compose).

This repository holds no application code. It is a directory of small YAML items with
permanent UIDs, validated by `tl check`. Consumers import it under a namespace and
reference its rules as `purpose:SR-0001` or its principles as `purpose:UR-0001`.

## One orthogonal axis, one purpose

Purpose is *what the writing is for* — its communicative job — distinct from whether
it is *understood* (readability), *correctly spelled* (conventions) or how it *sounds*
(tone). This source is **only** the purpose axis, and **only** the **instruct**
purpose: guiding the reader through the actions needed to reach a successful outcome.
It says nothing about:

- **readability** (word choice, sentence length, active voice) — `throughline-plain-language`
- **conventions** (spelling, punctuation, capitalisation, numbers) — `throughline-conventions-uk`
- **tone / register** (formal, neutral, informal) — `throughline-tone-*`
- **medium / channel** (web page, email, microcopy, slide deck)
- **brand voice** (an organisation's own personality)

In particular, *"put the steps in a numbered list"* is a **readability** move
(`plain`); this source owns the deeper question of whether the instruction is
**complete and correctly ordered** — prerequisites, one action per step, branches, and
how to verify success.

Purposes are **mutually exclusive**: a page has one primary job — to inform *or*
instruct *or* persuade, not several at once. So each purpose is a **sibling** source
(`throughline-purpose-inform`, `throughline-purpose-persuade`) and a consumer composes
exactly one under the `purpose` namespace — swapping purpose is a one-line `url`/`ref`
change. A task like *"a plain, formal, UK-English page that instructs"* becomes a
**compose** of `plain` + `conventions-uk` + `tone-formal` + `purpose-instruct`.

## What's in the graph

<!-- tl:count type == 'user_requirement' -->
5
<!-- tl:end --> principles as `user_requirement`s, each `derives_from` the root
intent, and
<!-- tl:count type == 'system_requirement' -->
10
<!-- tl:end --> rules as `system_requirement`s, each `implements` its principle. The
published spec is generated from the graph at [`docs/spec.md`](docs/spec.md).

## Source & licensing

The rules are Time Back Solutions' own house content guidance, licensed under
Apache-2.0. They reproduce no third-party standard. Each rule records its purpose and
dimension in `attrs.source_ref` and its owning principle in `attrs.principle`. See
[`NOTICE`](NOTICE).

## Extending the source

Items are hand-authored static YAML — one file per item, one permanent UID per file.
To add a rule, create the next `SR-00NN.yml` by hand (never renumber an existing one)
and link it with `implements` to its principle. Then:

```sh
tl check --strict      # the graph must stay sound
tl docs                # regenerate docs/spec.md + README.md
tl docs --check        # CI gate: docs must match the graph
```
