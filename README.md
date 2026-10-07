# mulesoft-error-handler-plugin

> Canonical API error responses for Mule 4 — consistent error body, status codes, and logging integration.

Mule plugin that standardises error handling across API-led applications. Uses app-local `customErrors.dwl` for domain-specific error mappings (same pattern as `auditCustom.dwl` for audit logging).

## Table of Contents

- [About](#about)
- [Features](#features)
- [Prerequisites](#prerequisites)
- [Getting Started](#getting-started)
- [Usage](#usage)
- [CI/CD](#cicd)
- [Documentation](#documentation)
- [Related Projects](#related-projects)
- [License](#license)

## About

Platform error-handling plugin published to Anypoint Exchange. Default dependency in `maven-parent-pom` and the utility application template.

## Features

- Standard API error response structure
- HTTP status mapping from Mule errors
- Integration with `json-logger` for exception events
- Customisable via `dwl/error/customErrors.dwl`

## Prerequisites

| Requirement | Version / notes |
|-------------|-----------------|
| Mule Runtime | 4.9.x |
| Maven | 3.9+ |
| Exchange org | `8d624bf1-5cd5-455e-94ea-6f2ba716a0ed` |

## Getting Started

```bash
mvn clean test package
```

| Field | Value |
|-------|-------|
| `artifactId` | `api-error-handler` |
| `version` | `1.1.0-SNAPSHOT` |
| `classifier` | `mule-plugin` |

## Usage

```xml
<dependency>
  <groupId>8d624bf1-5cd5-455e-94ea-6f2ba716a0ed</groupId>
  <artifactId>api-error-handler</artifactId>
  <version>1.1.0-SNAPSHOT</version>
  <classifier>mule-plugin</classifier>
</dependency>
```

Reference: `common-error.xml` in `mulesoft-utility-template-app`.

## CI/CD

| Trigger | Branch | Action |
|---------|--------|--------|
| PR → `develop` | SNAPSHOT |
| Merge `main` | Release + tag `v*` |

**Pipeline:** `publish-exchange.yml`

## Documentation

Detailed runbooks, architecture, and troubleshooting are maintained in the **Obsidian vault** (not in this repository).

| Topic | Obsidian path |
|-------|---------------|
| Repository card | `GitHub/repos/mulesoft-error-handler-plugin.md` |
| Documentation standard | `GitHub/readme-standard.md` |

## Related Projects

| Project | Relationship |
|---------|--------------|
| [mulesoft-json-logger-plugin](https://github.com/brunosouzas/mulesoft-json-logger-plugin) | Exception logging |
| [raml-utility-core-library](https://github.com/brunosouzas/raml-utility-core-library) | Error types in RAML |
| [maven-parent-pom](https://github.com/brunosouzas/maven-parent-pom) | Default dependency |

## License

See [LICENSE](LICENSE).
