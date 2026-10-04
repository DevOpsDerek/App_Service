# App_Service

A repository containing Azure ARM infrastructure as code files

## Automation validation

This repository currently has no GitHub Actions workflows or test/toolchain
configuration. The central
[`DevOpsDerek/workflows`](https://github.com/DevOpsDerek/workflows) catalog at
`57da3f99768c3403cb688b1729d3dfc146c7cd4b` provides validation for GitHub
Actions and gh-aw sources, plus a checked-script runner for Go, Python,
Node.js, .NET, and Terraform. None of these interfaces validates ARM templates,
so this repository does not add a CI workflow or treat them as ARM validation.
Revisit central adoption if an ARM-specific validation interface is published;
do not add deployment or infrastructure-apply automation.
