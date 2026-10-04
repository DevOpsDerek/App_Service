# App_Service

A repository containing Azure ARM infrastructure as code files

## Automation validation

`.github/workflows/validate-agentic-workflows.yml` calls the centrally
maintained GitHub automation validator from
[`DevOpsDerek/workflows`](https://github.com/DevOpsDerek/workflows), pinned to
immutable commit `dac4b81c298cb3ea6821ea312efa5375f42d5ccb`. It runs on pull
requests and pushes to `main`, with `contents: read`, and validates GitHub
Actions and any gh-aw sources. This repository currently has no gh-aw sources,
so the central validator skips gh-aw compilation.

This workflow does **not** validate ARM template semantics. The ARM files are
JSON syntax-checked with `python3 -m json.tool`; that check alone is not ARM
validation. No deployment or infrastructure-apply automation is configured.
