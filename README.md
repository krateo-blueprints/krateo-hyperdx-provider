# krateo-hyperdx-provider

The HyperDX OpenAPI spec consumed by [`krateo-hyperdx-provider-chart`](https://github.com/krateo-blueprints/krateo-hyperdx-provider-chart).

> Split out of the former `observability-stack` monorepo to follow the org standard (`krateo-<name>` source repo ↔ `krateo-<name>-chart`). History preserved.

## What it ships

| Path | Purpose |
|------|---------|
| `openapi/hyperdx.yaml` | OpenAPI spec for HyperDX; `krateo-hyperdx-provider-chart`'s `RestDefinition` points its `oasPath` at a **pinned** raw ref of this file, and `krateo-oasgen-provider` generates the managed `hyperdx.krateo.io` CRDs + controllers from it at runtime. |

No image is built here (oasgen-provider does the work). Pin the `oasPath` to a tag of this repo (not `main`) for reproducibility.

Part of [Krateo PlatformOps](https://krateo.io).
