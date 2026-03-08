# Changelog

## [0.1.0-omega](https://github.com/jporcenaluk/automations/compare/v0.0.1-omega...v0.1.0-omega) (2026-03-08)


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
