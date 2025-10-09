# Architecture

This document describes the high‑level architecture of the AI App Generator.

* `apps/studio` – User‑facing Next.js 14 App Router application.
* `packages/engine` – Orchestrates spec → code generation.
* `packages/templates` – Template registry and learning system.
* `packages/quality` – Quality gates: lint, typecheck, unit tests, build.
* `packages/shared` – Shared types and utilities.
* `prisma/schema.prisma` – Database schema for users, projects, and generations.
