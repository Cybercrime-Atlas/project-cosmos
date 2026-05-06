# Contributing to Project Cosmos

Thank you for your interest in contributing. Project Cosmos is an open ontology, and we welcome contributions from researchers, analysts, vendors, academics, and law-enforcement partners.

This guide explains how to file issues, propose changes, and submit pull requests.

## Code of Conduct

All participants are expected to follow our [Code of Conduct](CODE_OF_CONDUCT.md). Report concerns to `info@cybercrime-atlas.org`.

## Ways to contribute

There are several ways to contribute, in roughly increasing order of effort:

1. **Open an issue** — flag a bug, ask a question, propose a small change
2. **Propose an ontology change** — suggest a new entity type, a new relationship, or a refinement to an existing definition
3. **Submit a pull request** — fix a bug, add an example, improve documentation, or implement an accepted proposal
4. **Contribute a worked example** — show how Project Cosmos can be used to map a real (publicly known) cybercriminal ecosystem

## Filing an issue

Before opening an issue, please search existing issues to see if your topic has already been raised.

Use the relevant template:

- **Bug report** — for problems with the ontology, schemas, documentation, or examples
- **Proposal** — for changes or additions to the ontology

Please include enough context that someone unfamiliar with your specific use case can understand what you're proposing and why.

## Proposing an ontology change

Ontology changes have downstream effects for everyone who has adopted Project Cosmos. We treat them as design decisions and follow a lightweight RFC-style process:

1. Open a **Proposal** issue describing the change, the motivation, and any alternatives you considered
2. The maintainers and community discuss the proposal in the issue thread
3. Once there is rough consensus, a maintainer (or you, if you'd like) opens a pull request implementing the change
4. The pull request is reviewed against the agreed proposal and merged

Larger or more contentious changes may be left open longer to gather wider input. Please be patient — careful change management is part of why an ontology is useful.

## Submitting a pull request

1. **Fork** the repository to your own account (or create a feature branch if you have direct access)
2. **Branch naming** — use a short, descriptive name with a prefix:
   - `feat/` for new features or additions
   - `fix/` for bug fixes
   - `docs/` for documentation-only changes
   - `chore/` for housekeeping
   - For example: `feat/add-financial-flow-entity`, `fix/typo-in-actor-definition`
3. **Commit messages** — please write clear, descriptive messages. We loosely follow [Conventional Commits](https://www.conventionalcommits.org/):
   - `feat: add Financial Flow entity type`
   - `fix: correct typo in Actor description`
   - `docs: clarify usage example for Infrastructure mapping`
4. **Open the pull request** — fill in the PR template; reference any related issues
5. **Wait for review** — at least one maintainer must approve. Code-owners review is required for changes to the core ontology
6. **Address feedback** — push additional commits to the same branch; we'll squash on merge

## Style and conventions

- Markdown files should use sentence-case headings
- File and directory names should use lowercase with hyphens (e.g. `threat-actor-attributes.md`)
- Schemas should validate against the relevant standard (JSON-LD, RDF/Turtle, etc.) before submission
- Examples should reference only publicly known threat actors, infrastructure, or events — do not include sensitive or unattributed intelligence

## Sensitive content

Project Cosmos is a **public** repository. Do not include:

- Information about active investigations
- Identities of confidential sources
- Non-public threat-actor identifying information
- Closed-source intelligence (e.g., from paid platforms)
- Anything classified TLP:AMBER or TLP:RED

If a worked example would require sensitive material, either omit those details or anchor the example on a publicly disclosed case (indictments, vendor reports, court filings, press releases).

## Questions

For general questions, open a [Discussion](../../discussions). For private or sensitive questions, email `info@cybercrime-atlas.org`.
