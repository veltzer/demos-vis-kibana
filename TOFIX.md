# TOFIX

Findings from a code scan on 2026-10-04.

## Medium

- `README.md:3` - the repo says "Demos for the Kibana system" but holds no demo at all: the only tracked files are fleet boilerplate, `config/project.lua` and two READMEs. Add the demos (saved-object exports, a docker-compose for ES+Kibana, sample dashboards), or describe the repo as a placeholder.
- `rsconstruct.toml:1` - `README.md` is not checked by rumdl, and the repo has no `.rumdl.toml`, unlike its siblings (demos-db-redis, demos-db-mysql). Add the fleet `.rumdl.toml`, a `[processor.rumdl]` with `src_files = ["README.md"]`, and `.rumdl.toml` in the taplo `src_files`.

## Low

- `README.txt:1` - a one-line "These are my kibana demos" duplicate of `README.md`. Delete it.
