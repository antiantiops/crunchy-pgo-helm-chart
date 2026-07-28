# Crunchy PGO Helm Chart

[![Lint and Test](https://github.com/antiantiops/crunchy-pgo-helm-chart/actions/workflows/ci.yaml/badge.svg)](https://github.com/antiantiops/crunchy-pgo-helm-chart/actions/workflows/ci.yaml)
[![Release](https://github.com/antiantiops/crunchy-pgo-helm-chart/actions/workflows/release-chart.yaml/badge.svg)](https://github.com/antiantiops/crunchy-pgo-helm-chart/actions/workflows/release-chart.yaml)

A public Helm chart mirror for [PGO](https://github.com/CrunchyData/postgres-operator) — the open source Postgres Operator from Crunchy Data.

## Usage

```bash
helm repo add crunchy-pgo https://antiantiops.github.io/crunchy-pgo-helm-chart/
helm repo update
helm install pgo crunchy-pgo/pgo --namespace postgres-operator --create-namespace
```

## Why?

Crunchy distributes PGO only through their OCI registry. This repo re-publishes the chart as a standard Helm HTTP repository so it can be consumed by ArgoCD, Flux, Rancher, and other tools that don't support OCI yet.

## Upstream Watch

A GitHub Actions workflow checks the Crunchy OCI registry every 6 hours and auto-bumps the chart when a new PGO version is released.
