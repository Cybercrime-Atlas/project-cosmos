# Contributing to Project Cosmos

Thank you for your interest in contributing. Project Cosmos is an open ontology, and we welcome contributions from researchers, analysts, vendors, academics, and law-enforcement partners.

## Code of Conduct

All participants are expected to follow our [Code of Conduct](CODE_OF_CONDUCT.md). Report concerns to `github@cybercrime-atlas.org`.

## What you can contribute

You may propose:

- new ontology terms
- improved shortDescription or longDescription values
- relationship corrections
- identifier corrections
- documentation improvements
- release and publication fixes

## Before you contribute

1. Check whether an existing issue already covers the change.
2. Open an issue first for major structural changes.
3. Keep one logical change per pull request.

## Repository rules

- The canonical ontology source is `ontology/source/atlas-ontology.owl`.
- Do not edit generated files manually unless the change specifically concerns publication output.
- Do not change public IRIs casually. Treat them as stable identifiers.

## Pull request expectations

Each pull request should explain:

- what changed
- why it changed
- whether any IRI changed
- whether any descriptions, relationships, or documentation also need updating

## Description standards

### shortDescription
- concise and standalone
- usually about 20–40 words
- should identify the essence of the concept
- should not simply repeat the label

### longDescription
- fuller explanatory treatment
- should add context, scope, function, and boundaries
- should remain stable and reusable
- should not drift into incident-specific reporting unless that is intentional

## Structural changes requiring extra care

Raise an issue before submitting a PR if you want to:

- rename classes, properties, or individuals
- change namespace or versioning behavior
- delete public terms
- alter major relationship patterns
- change release or publication workflows

## Review process

Typical review checks include:

- ontology validity
- IRI stability
- naming consistency
- description quality
- relationship correctness
- publication impact

## Security

Do not publish secrets, credentials, tokens, internal system details, or unpublished sensitive data.

For security issues, see [SECURITY.md](SECURITY.md).

## Questions

For general questions, open a [Discussion](../../discussions). For private or sensitive questions, email `info@cybercrime-atlas.org`.
