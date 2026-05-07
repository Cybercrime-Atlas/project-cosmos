<p align="center">
  <a href="">
    <img src="https://github.com/Cybercrime-Atlas/project-cosmos/blob/main/.github/images/CA_Colour.png" alt="Atlas logo" width="400" height="165">
  </a>
</p>

# Project Cosmos

> Ontology project for Cybercrime Atlas mapping — Powered by the World Economic Forum

Project Cosmos is an open ontology for representing and mapping cybercriminal ecosystems. It is developed under the **Cybercrime Atlas** initiative, hosted by the World Economic Forum, and provides a shared vocabulary and structural framework for describing threat actors, infrastructure, tools, tactics, financial flows, and the relationships between them.

The goal is a common reference framework that researchers, analysts, vendors, academics, and law enforcement can use to share, integrate, and compare findings across organisations — without prescribing how anyone runs their own internal analysis.

## Repository structure

The repository will grow as the ontology develops. Initial planned structure:

- **`ontology/source/`** — canonical editable ontology source
- **`ontology/derived/`** — generated serializations
- **`ontology/releases/`** — version snapshots
- **`docs/`** — GitHub Pages content

## Why an ontology

Cybercrime research is fragmented across vendors, agencies, and academic disciplines, each using their own terminology and data models. The same threat actor is described differently by every organisation looking at it; the same infrastructure is named differently in different feeds; the same financial flow is modelled differently in different reports.

Project Cosmos doesn't try to replace those internal models. It provides a shared layer above them — a way for findings to be translated, compared, and combined when organisations choose to collaborate.

## Using Project Cosmos

The ontology and schemas are released under permissive licences (see below) so they can be adopted in any setting — academic research, vendor tooling, internal analyst workflows, or law-enforcement engagement.

When using or referencing Project Cosmos in derivative work, please attribute as:

> "Project Cosmos — Cybercrime Atlas, Powered by the World Economic Forum"

## Contributing

We welcome contributions from the community. Researchers, analysts, vendors, academics, and law-enforcement partners are all invited to file issues, propose changes to the ontology, and submit pull requests.

See [CONTRIBUTING.md](CONTRIBUTING.md) for how to get involved, and [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md) for the standards we expect of all participants.

## Licensing

This repository uses dual licensing:

- **Code** (scripts, tooling, automation) — [Apache License 2.0](LICENSE)
- **Content** (ontology definitions, documentation, examples, data) — [Creative Commons Attribution 4.0 International](LICENSE-CONTENT)

## Security

To report a security issue or vulnerability, please email [info@cybercrime-atlas.org](mailto:info@cybercrime-atlas.org). See [SECURITY.md](SECURITY.md) for our responsible-disclosure policy.

## About Cybercrime Atlas

The Cybercrime Atlas is a global initiative hosted by the World Economic Forum that brings together cybersecurity investigators from the private sector and law-enforcement agencies to map, investigate, and disrupt cybercriminal ecosystems.

Learn more at [cybercrime-atlas.org](https://cybercrime-atlas.org).
