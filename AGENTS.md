# mulesoft-error-handler-plugin: project context

## Purpose

Reusable MuleSoft error-handling strategies and mappings.

## Technology declarations

- `mule.version = 4.9.1` — [pom.xml](pom.xml).
- `mule.extensions.maven.plugin.version = 1.9.0` — [pom.xml](pom.xml).
- `exchange.mule.maven.plugin.version = 0.0.23` — [pom.xml](pom.xml).
- `java.version = 17` — [pom.xml](pom.xml).
- `Maven parent mule-modules-parent 1.9.0` — [pom.xml](pom.xml).
- `Declared minimum Mule runtime 4.3.0` — [mule-artifact.json](mule-artifact.json).

These are source declarations, not evidence of installed runtimes. Maven properties may describe build/test dependencies rather than supported runtime minima; unresolved expressions remain inherited until verified.

## Layout and operation sources

Top-level source/documentation directories: `docs`, `examples`, `exchange-docs`, `src`.

- [README.md](README.md).
- [mule-artifact.json](mule-artifact.json).
- [pom.xml](pom.xml).
- [azure-pipelines.yml](azure-pipelines.yml).
- [docs/ARCHITECTURE.md](docs/ARCHITECTURE.md).

GitHub default branch inspected on 2026-10-06: `main`. This context is prepared against develop, the integration line selected from the project pipeline/release sources. The GitHub default is separately main. Build/publish commands mentioned by those sources are context, not authorization.

## Project rules

Before planning, reviewing or changing this project, read [the applicable project rules](rules/README.md).
