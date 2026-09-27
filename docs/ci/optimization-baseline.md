# GitHub Actions optimization baseline

## Status

This document records the live CI architecture at commit
`fcdb095c8f712b7599f31297dc53d3c3783e9849` on 2026-09-27.

This baseline changes no workflow behavior and enables no validation suppression.

## Repository and governance

| Field           | Value                                                                   |
| --------------- | ----------------------------------------------------------------------- |
| Repository      | `Cotsel/Cotsel`                                                         |
| Visibility      | Public                                                                  |
| Default branch  | `main`                                                                  |
| Required check  | `boundaries`                                                            |
| Required review | One code-owner approval, stale-review dismissal, and last-push approval |

## Current workflow

`Repository policy` runs on every PR and every push to `main`. It allocates one
`ubuntu-latest` job and uses read-only contents permission.

The job verifies required repository boundary documents and rejects Agroasys-specific
imports in Cotsel core source. Its concurrency group cancels superseded work.

The workflow has no path filter. This is appropriate because the check is short and protects
the repository boundary itself.

## Observed usage

The workflow ran four times during the 30-day window starting 2026-08-28. One run was a PR
run and three were pushes. All runs succeeded. Average elapsed time was 16 seconds.

September billing through 2026-09-27 records four gross Linux minutes and USD 0 net cost.
Standard public-repository runner usage is not a private Actions billing target.

## Phase 0 findings

1. The one-job policy is proportionate and inexpensive.
2. Concurrency already cancels obsolete PR work.
3. A change classifier would add complexity without meaningful compute reduction.
4. Keep the required `boundaries` check broad because it protects repository independence.
5. This baseline enables no validation suppression.

## Rollback

Revert this documentation commit if the baseline contains an error. No CI behavior rollback
is required.
