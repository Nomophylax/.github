# Nomophylax (n8x)

Nomophylax is a neuro-symbolic, architecture-aware pull-request reviewer for CI: a deterministic core checks pull requests against ADRs and static-analysis output, with LLMs bounded to perception and presentation.

It is a master's project at the University of St. Gallen (HSG) by Ioannis Theodosiadis and Tilman Haferbeck.

Website: [nomophylax.com](https://nomophylax.com) (coming soon)

## Repositories

| Repository | What it is for | Important directories |
|---|---|---|
| [nomophylax](https://github.com/nomophylax/nomophylax) | The product: source, rule artefacts, architecture docs and ADRs. Iterations are Git tags `v0.x`. | `core/` deterministic reasoning (no LLM, no network) · `perception/` ADR text → rules (LLM) · `presentation/` findings → review (LLM) · `adapters/` GitHub, SonarQube, ArchUnit · `rules/` ratified rule artefacts · `cli/`, `action/` entry points · `docs/adr/` decisions · `docs/requirements.md`, `docs/verification.md`, `docs/iterations.md` |
| [project](https://github.com/nomophylax/project) | The master's project *about* n8x: meetings, roadmap, decisions on scope and method, report and slide sources, course notes. No product code. | `CONTEXT.md`, `ROADMAP.md` · `meetings/` · `decisions/` · `retrospectives/` one per iteration · `report/`, `slides/` sources · `wiki/` advisor course notes · `artifacts/` generated Markdown mirror of SharePoint · `ai/` prompts and outputs |
| [evaluation](https://github.com/nomophylax/evaluation) | Benchmark corpus, experiment runs, metrics and figures. Consumes n8x releases; frozen per iteration tag. | (set up with v0.1) |
| [site](https://github.com/nomophylax/site) | Public website nomophylax.com, built from `nomophylax/docs`. | (later) |
| [.github](https://github.com/nomophylax/.github) | This org profile and the shared issue and PR templates. | `profile/`, `.github/ISSUE_TEMPLATE/`, `.github/PULL_REQUEST_TEMPLATE.md` |

Dependency direction is one-way: `evaluation` → `nomophylax` release; `site` → `nomophylax/docs`; `project` links to both; nothing depends on `project`.

Tasks are GitHub issues in the repository they concern, tracked on the org [project board](https://github.com/orgs/nomophylax/projects/1). Architecture decisions are ADRs in `nomophylax/docs/adr/`; decisions about scope, method or evaluation design live in `project/decisions/`.
