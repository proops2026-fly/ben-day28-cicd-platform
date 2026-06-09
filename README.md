# ben-day28-cicd-platform

Shared CI/CD platform workflows for proops2026-fly services.

## Reusable Workflows

| Workflow | Purpose |
|----------|---------|
| `reusable-build.yml` | Go vet, test, docker build and push to ghcr.io |
| `reusable-deploy.yml` | Deploy image to a target environment |

## Usage

Reference workflows with the `v2` tag:

```yaml
jobs:
  build:
    uses: proops2026-fly/ben-day28-cicd-platform/.github/workflows/reusable-build.yml@v2
    with:
      project-name: "proops2026-fly"
      service-name: "your-service"
    secrets: inherit
```

## Tags

| Tag | Points to |
|-----|-----------|
| `v2` | Current stable — run: only steps, no marketplace actions |
