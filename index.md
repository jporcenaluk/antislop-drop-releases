# The Antislop Drop - Release Notes

Release notes and changelog for [The Antislop Drop](https://github.com/jporcenaluk/automations), a weekly AI-in-software newsletter for software leaders.

_Release notes are published automatically on each release._

---

## v0.0.1-omega.14 (2026-05-06)

Fixed newsletter theme selection so per-domain article caps are applied before theme eligibility, preventing daily issues from reusing source URLs when a theme has too few usable samples.

---

## v0.0.1-omega.13 (2026-05-06)

Fixes production backfill retries by adding the required BigQuery partition filter to the enrichment completeness check.

---

## v0.0.1-omega.12 (2026-05-05)

This is a big one! This release introduces a database store rather than file-based store for articles, meaning it is possible to create smarter retrieval and synthesis of information.

It also uses AI to categorize and add metadata to articles on write, rather than on read. This leads to less token-heavy processes when composing the newsletter.

---

## v0.0.1-omega.11 (2026-04-17)

Reduce token usage (and failures due to that).

---

## v0.0.1-omega.10 (2026-04-16)

Moving to a more stable model (Gemini 2.5). Also removed “team nudge.”

---

## v0.0.1-omega.9 (2026-04-15)

More internal improvements? YES! Sorry, sometimes the structure needs set before the content can improve. In this case, internal improvements to help with verification during automation were included. This includes *integration tests*!

Also, the 'scout' agent that goes and gathers industry whitepapers was *expensive* and also flaky. I'll need to rethink the approach there!

---

## v0.0.1-omega.8 (2026-04-08)

Refactoring and simplifying.

---

## v0.0.1-omega.7 (2026-04-03)

Reliability.

---

## v0.0.1-omega.6 (2026-04-03)

Making fallbacks more reliable.

---

## v0.0.1-omega.5 (2026-04-03)

Test fixes, refactors, chores, ci updates, fixes, fixes, fixes, oh my! Do you like chores and fixes? Because I have chores and fixes for YOU!

---

## v0.0.1-omega.4 (2026-03-24)

Omega 4 is not a real vitamin (I don't think) but it doesn't matter. In this release a lot happened behind the scenes but I'll keep the release notes to what may actually matter to you: a better newsletter.

- Moved up to the big leagues by going from Gemini 3 Flash to Gemini 3.1 Pro. What this means for you is 'more intelligent' insights into the state of the world when it comes to what's important to pay attention to in AI news.
- Started ingesting new pieces of information (e.g. whitepapers) in addition to news to get a solid grounding for what the news may mean for the long-term
- 3 fixes to add in stability
- 2 refactors

---

## v0.0.1-omega.3 (2026-03-21)

I hope everyone is getting their OMEGA 3 in! Wow, we had to wait three releases four our first *really lame* release joke. Yes, this is v0.0.1-omega.3, and it is a **doozy** of an update. Now:

* you won't keep getting the same lame sources across daily newsletters! The variety of sources should be improved greatly.
* stories should not be random scattershots every day, but follow trends over time to see what is important.
* daily, weekly (on Mondays), and monthly newsletters offer differing levels of detail and scope so you can keep up on what's going on daily, but also have time to reflect on the overall trends at cadences that make sense.
* some HUGE internal re-structuring that allows for further 'smarts' to be built-in

---

## v0.0.1-omega.2 (2026-03-16)

The most notable improvement is a big switch to Google’s ADK (Agent Development Kit) framework from simply calling LLM APIs.

This lays the foundations for neat (and useful) ways to gather information and make sense of it.

Other improvements:

* daily emails use daily information rather than gathering weekly information and summarising (which led to repeated email content)
* internal security improvements
* email version added to footer
* added cohesion pass to allow for holistic email tone

---

## v0.0.1-omega.1 (2026-03-08)

## Release notes

This is the first version (v0.0.1-omega.1) of The Antislop Drop. You may be asking yourself: What the heck is this? Well. It's a newsletter for tech leaders to help turn the Firehose of AI information into a daily Drop.

I've got *big plans* for what is deployed in future releases but the long and short of it is that this is going to not only be a newsletter, but a fun testbed for how I develop things using agentic AI.

In this first release you get:

* Weekly emails (soon to be daily; although I may trigger them manually daily for the time being)
* Gemini 3.1 Flash as the model that summarises information
* 100s of sources for news condensed into a single email (weekly! but soon daily)

> A note about the versioning. We're in the `omega` era until this newsletter hits 10 subscribers, at which time we'll hit the `psi` era. And we'll keep working our way _up_ the Greek alphabet while we hit subscriber milestones up to Alpha when we hit 1,000,000 subscribers. And then Version 1 (imagine a lot of music and fireworks and cheering) gets released.

---

## v0.0.1-omega (2026-03-08)

## 0.0.1-omega (2026-03-08)

### Added

* add .github/copilot-instructions.md with project, tooling, and coding conventions ([ca21ad4](https://github.com/jporcenaluk/automations/commit/ca21ad49661bfeaabaeb1f7fa01106f4fd42b5c3))
* add 7 validated RSS feeds from issue [#71](https://github.com/jporcenaluk/automations/issues/71) ([#92](https://github.com/jporcenaluk/automations/issues/92)) ([3f4ce65](https://github.com/jporcenaluk/automations/commit/3f4ce6528c171dc7ecd835bfc53a6665e1a6e12e))
* add FastAPI response models ([478ab22](https://github.com/jporcenaluk/automations/commit/478ab224cd4d9762ccfb5fad5fbaac71fd21d894))
* add Gemini Pro summariser with Pydantic models and retry logic (US-004) ([b87fae0](https://github.com/jporcenaluk/automations/commit/b87fae0f31853d7ab903eb8f5aa2e6abaa14c37d))
* add unsubscribe link and HTML email support for CAN-SPAM compliance ([#96](https://github.com/jporcenaluk/automations/issues/96)) ([b6091ca](https://github.com/jporcenaluk/automations/commit/b6091cab5bf0d596368aff0b3901d9fdf93e7a60)), closes [#83](https://github.com/jporcenaluk/automations/issues/83)
* convert FeedEntry to Pydantic model with built-in normalization (Phase 3) ([fac5fdb](https://github.com/jporcenaluk/automations/commit/fac5fdb2ab183971accbd463fecad4431bdcfbec))
* Gemini 3.1 Pro structured summarisation with Pydantic validation and recursive retry ([a313ee4](https://github.com/jporcenaluk/automations/commit/a313ee4708b244a292d306d881e1d084ee3cf092))
* HTML email template, Resend broadcast draft integration, and tests ([747a1ea](https://github.com/jporcenaluk/automations/commit/747a1eab204ef872115455615f7dea7410ba5b1e))
* migrate Flask web layer to FastAPI (Phase 1) ([73971fb](https://github.com/jporcenaluk/automations/commit/73971fbc332bcd140eb96da13a3ca521fc010a63))
* orchestrate newsletter pipeline with LangGraph StateGraph (US-005) ([7781125](https://github.com/jporcenaluk/automations/commit/7781125822fdbfc98ffccb4ad15e864a51cb91a9))
* **US-007:** add Dockerfile, Pulumi IaC, GitHub Actions deploy workflow, and tests ([f3294a6](https://github.com/jporcenaluk/automations/commit/f3294a659b141a428d636e170e985e6e78ced849))
* **US-007:** Cloud Run deployment with Cloud Scheduler trigger ([4ba6001](https://github.com/jporcenaluk/automations/commit/4ba60019a53bbf20d7efa93b13b5440c1fdc9198))
* versioning, release-please, dual-env deploys, and public release notes ([#108](https://github.com/jporcenaluk/automations/issues/108)) ([ebeda71](https://github.com/jporcenaluk/automations/commit/ebeda7122b298760158581dcc66a05af8a044645))

### Fixed

* address code review feedback - validate draft_id, fix type annotations ([d99c6b3](https://github.com/jporcenaluk/automations/commit/d99c6b3b7b344dd7bf429a335c4fcf82b96404ec))
* clarify comment on Pydantic validation vs Gemini schema enforcement ([427570e](https://github.com/jporcenaluk/automations/commit/427570ec87d4784e47f719dc1ef0d2251c439bd8))
* replace StackReference with direct config reads in Pulumi main stack ([#95](https://github.com/jporcenaluk/automations/issues/95)) ([ded8aab](https://github.com/jporcenaluk/automations/commit/ded8aabd71bd8a44015cec89ddd67fc6ef3f02d8)), closes [#94](https://github.com/jporcenaluk/automations/issues/94)
* resolve all pre-commit hook failures ([#69](https://github.com/jporcenaluk/automations/issues/69)) ([218369d](https://github.com/jporcenaluk/automations/commit/218369d676ad4dc549b4882415548072f355a770))
* update Gemini model ID from gemini-3-flash-preview to gemini-3-flash ([#66](https://github.com/jporcenaluk/automations/issues/66)) ([44599dd](https://github.com/jporcenaluk/automations/commit/44599ddedd1420966f596ff502b620072acd8e2e)), closes [#65](https://github.com/jporcenaluk/automations/issues/65)
* update web framework from Flask to FastAPI in copilot-instructions.md ([911d51d](https://github.com/jporcenaluk/automations/commit/911d51d71fb0864882d0be56a94192775c85799b))
* use gemini-3-flash-preview in global region ([#106](https://github.com/jporcenaluk/automations/issues/106)) ([4e109ac](https://github.com/jporcenaluk/automations/commit/4e109ac97fe019b63b9a4f6b550bff15052a3dcc))
* use language: python with additional_dependencies for pytest-fast hook ([14b77f6](https://github.com/jporcenaluk/automations/commit/14b77f68e55b31b0e365c2f265fa13ee146d168c))

### Changed

* enforce JSON schema via Gemini response_json_schema config ([2bc56b6](https://github.com/jporcenaluk/automations/commit/2bc56b603159ff6e7c8195930eba4636bc054f5d))
* extract infra/stack.py for clean imports, address code review ([4e9bb66](https://github.com/jporcenaluk/automations/commit/4e9bb663d7caf7ba107d57e6096943cac8120f95))
* move newsletter formatting from cloud_task.py to newsletter.j2 template ([34e8a28](https://github.com/jporcenaluk/automations/commit/34e8a28f60a22de46bdcfc740e70d33d2b5f5930))
* remove `from __future__ import annotations` from pipeline.py and revert __init__.py re-exports ([1bc6c32](https://github.com/jporcenaluk/automations/commit/1bc6c3234096b1ae74c8646858c6f185007cde83))
* use Gemini 3.1 Pro, recursive retry, Jinja prompt template ([50eae95](https://github.com/jporcenaluk/automations/commit/50eae95291645fe7ca6967f145aadf1192cedd83))

---
