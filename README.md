# example-go

[![view-action-graph](https://img.shields.io/github/actions/workflow/status/actionforge/example-go/workflow.yml?label=View%20build.act)](https://app.actionforge.dev/github/actionforge/example-go/main/.github/workflows/graphs/build.act)

A simple Hello World app in Go, built using an [Actionforge](https://actionforge.dev) graph as the CI/CD pipeline.

## Build

```bash
go build -o hello-world .
```

## Graph

The build pipeline is defined as an Actionforge graph in [`.github/workflows/graphs/build.act`](.github/workflows/graphs/build.act):

```
checkout -> setup-go -> build -> upload-artifact
```

It runs on every push to `main`, on pull requests, and on manual dispatch.
