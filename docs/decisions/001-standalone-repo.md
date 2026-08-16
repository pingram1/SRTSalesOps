# ADR-001: SRTSalesOps is a standalone repo

## Status

Accepted

## Date

2026-08-16

## Context

The internal quoting and pipeline app was first planned as `apps/ops` inside the public website monorepo, then as a Remy-hosted app. Remy needs a credit top-up. The website repo must stay a static marketing SPA. Pierre already keeps products as siblings under `StartRightTutoringLocal`.

## Decision

Build **SRTSalesOps** at `/Users/pierrei/StartRightTutoringLocal/SRTSalesOps` as its own git repo and private GitHub remote. Open it in a separate Cursor window. Keep `WebsiteNewLocal` untouched.

## Consequences

- Sales-only prices live only in this private repo
- Website conventions no longer fight Ops work
- Sales docs are copied here; if they change in the website repo, copy them again or treat this copy as canonical for Ops
- Gmail / deploy / auth can be added here without risking the public site
