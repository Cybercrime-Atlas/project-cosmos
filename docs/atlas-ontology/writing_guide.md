---
title: Project COSMOS Writing Guide
layout: default
nav_order: 3
description: Writing standards for Project COSMOS ontology labels, aliases, short descriptions, long descriptions, and variants.
---

<a id="top"></a>

# Project COSMOS Writing Guide

This guide defines writing standards for Project COSMOS ontology content.

Use it when creating or reviewing labels, aliases, short descriptions, long descriptions, and variants for ontology classes and individuals.

The guide is designed to grow over time. Start with the shared rules, then apply the class-specific rules for the individual being written.

## Contents

- [How to Use This Guide](#how-to-use-this-guide)
- [Rule Precedence](#rule-precedence)
- [General Writing Rules](#general-writing-rules)
- [Shared Field Rules](#shared-field-rules)
- [Class-Specific Writing Rules](#class-specific-writing-rules)
  - [Pattern](#pattern)
  - [Pattern Phase / Diamond Event](#pattern-phase--diamond-event)
  - [Products and Services / Commodities](#products-and-services--commodities)
  - [Market](#market)
  - [Role Player](#role-player)
  - [Platform](#platform)
  - [Victim](#victim)
  - [Harm](#harm)
  - [Technique](#technique)
- [Reusable Templates](#reusable-templates)
- [Review Checklists](#review-checklists)
- [Editorial Review Notes](#editorial-review-notes)
- [Future Guidance](#future-guidance)
- [Suggested Repository Structure](#suggested-repository-structure)

---

<a id="how-to-use-this-guide"></a>

## How to Use This Guide

Use this guide in order:

1. Identify the ontology class of the entity or individual.
2. Apply the rule for the exact class, if one exists.
3. If no exact class rule exists, apply the nearest parent-class or class-family rule.
4. If no class-family rule exists, apply the shared field rules.
5. Use the relevant checklist before committing content.

The guide separates shared writing conventions from class-specific rules because fields such as `rdfs:label`, `alsoCalled`, `shortDescription`, and `longDescription` may differ by class.

[Back to top](#top)

---

<a id="rule-precedence"></a>

## Rule Precedence

Class-specific field rules override class-family rules.

Class-family rules override shared field rules.

Shared field rules apply only when no more specific rule is available.

```text
Exact class rule
overrides
Class-family rule
overrides
Shared default rule
```

[Back to top](#top)

---

<a id="general-writing-rules"></a>

## General Writing Rules

<a id="american-english"></a>

### American English

Use American English for all descriptions.

<a id="plain-analytic-style"></a>

### Plain Analytic Style

Use clear analytic prose.

Avoid marketing language, sensational wording, and unnecessary jargon.

Avoid time-specific incident detail unless it is essential to the stable definition of the entity.

Avoid operational how-to instructions, command-level procedures, and unnecessary indicators of compromise.

<a id="default-length-limits"></a>

### Default Length Limits

Use these default limits unless a class-specific rule says otherwise.

- `shortDescription`: 40 words or less.
- `longDescription`: 250 words or less.
- `variant`: 40 words or less.

[Back to top](#top)

---

<a id="shared-field-rules"></a>

## Shared Field Rules

These rules apply unless a class-specific section provides different guidance.

<a id="shared-label"></a>

### `rdfs:label`

The label is the preferred human-readable name for the entity.

The label should be concise, recognizable, and suitable for display in lists, diagrams, and ontology browsers.

<a id="shared-also-called"></a>

### `alsoCalled`

The `alsoCalled` field captures common aliases, alternative names, abbreviations, or ecosystem terms.

Use aliases that are common enough to help readers recognize the entity.

Do not include one-off references, incident-specific names, or speculative aliases.

<a id="shared-short-description"></a>

### `shortDescription`

The `shortDescription` provides a concise summary of the entity.

It should usually be one sentence.

The default maximum length is 40 words.

The purpose is to help a reader quickly decide whether the entity is relevant.

<a id="shared-long-description"></a>

### `longDescription`

The `longDescription` provides the fuller analytic explanation of the entity.

The default maximum length is 250 words.

Use paragraph breaks where they improve readability.

Do not add operational instructions, command-level procedures, indicators of compromise, or unnecessary implementation detail.

<a id="shared-variant"></a>

### `variant`

A `variant` captures a noteworthy variation on a general entity description.

A variant should describe a recurring variation that is important enough to record, but not common enough to change the core description.

A variant is description text, not a separate entity.

A variant should read like an additional paragraph appended to the end of the `longDescription`.

Rules for `variant`:

- Unlimited variants may be used.
- A variant is not an entity.
- Each variant should be 40 words or less.
- A variant should describe a recurring variation, not a one-off case.

[Back to top](#top)

---

<a id="class-specific-writing-rules"></a>

## Class-Specific Writing Rules

This section provides class-specific field rules. Add new classes here as the ontology expands.

---

<a id="pattern"></a>

## Pattern

<a id="pattern-purpose"></a>

### Purpose

A Pattern is a structured model representing a recurrent, recognizable manifestation of illicit, adverse, or exploitative cyber-dependent or cyber-enabled activity.

A Pattern encompasses multiple Diamond Events that collectively express a coherent operational or business model.

<a id="pattern-criteria"></a>

### Criteria

A Pattern should meet all of the following criteria:

- **Recognizable:** the activity has been observed, noted, and described.
- **Recurrent:** the activity happens often enough, and consistently enough, to be modeled as a Pattern.
- **Cyber-dependent or cyber-enabled:** the activity has a significant cyber component.
- **Illicit, adverse, or exploitative:** the activity is forbidden by law, rules, or customs; causes negative impact; or produces advantage or gain for the perpetrator.
- **Complex business or operational model:** the activity cannot be simplified to a single TTP or Diamond Event.

<a id="pattern-field-rules"></a>

### Field Rules

#### `rdfs:label`

Name the recurring cybercrime pattern or operational model.

Use a concise label that is recognizable outside a single incident or campaign.

#### `alsoCalled`

Include widely used alternative names for the Pattern.

Do not include one-off campaign names unless they are commonly used to refer to the Pattern itself.

#### `shortDescription`

Summarize the illicit activity, major operational model, and primary victim impact.

Use one clear sentence where possible.

#### `longDescription`

Describe the illicit activity, the Diamond Event flow, the role players and ecosystem elements, and the victims and impacts.

Maximum length: 250 words.

#### `variant`

Capture common Pattern variations that do not justify a separate Pattern.

Maximum length: 40 words per variant.

<a id="pattern-long-description-guidance"></a>

### Pattern `longDescription` Guidance

A Pattern `longDescription` should include three major parts:

1. Description of the illicit activity, including a concise summary of the Diamond Event flow.
2. Description of the threat actors, role players, and ecosystem elements.
3. Summary of victims and victim impacts.

<a id="pattern-template"></a>

### Pattern Template

```text
Label:
[Recognizable Pattern name]

alsoCalled:
[Common aliases or alternative names, if any]

shortDescription:
[One-sentence description of the recurring illicit activity and primary victim impact.]

longDescription:
[Paragraph 1: Describe the illicit, adverse, or exploitative activity and the overall operational model.]

[Paragraph 2: Summarize the Diamond Event flow, role players, and ecosystem elements.]

[Paragraph 3: Summarize victim groups and primary harms or impacts.]

variant:
[Optional recurring variation, 40 words or less.]
```

[Back to top](#top)

---

<a id="pattern-phase--diamond-event"></a>

## Pattern Phase / Diamond Event

<a id="diamond-event-purpose"></a>

### Purpose

A Pattern Phase, also described as a Diamond Event, represents a single, recognizable, illicit, adverse, or exploitative cyber-dependent or cyber-enabled activity.

A Diamond Event describes a complete phase in a Pattern.

A Threat Action is a specific technical action that a role player performs during that phase.

<a id="diamond-event-core-elements"></a>

### Core Diamond Model Elements

A Diamond Event should describe a unique set of four interconnected core elements:

- **Adversary:** Role Player.
- **Capability:** Threat Action.
- **Infrastructure:** Platform or Commodity.
- **Victim:** Victim and Impact.

<a id="diamond-event-modeling-rules"></a>

### Modeling Rules

A Diamond Event can describe a distinct phase within a Pattern.

Diamond Events represent the phases or steps taken by an actor to form a Pattern.

One Diamond Event may be associated with one or more Patterns.

A Diamond Event may also be linked to a Market when that Market trades the activity.

Diamond Events may be chained together in sequences when one Diamond Event includes or depends on another Event.

Some Diamond Events, especially technical Events, occur commonly across diverse Patterns. These should be labeled and modeled as reusable Common Events when appropriate.

<a id="diamond-event-field-rules"></a>

### Field Rules

#### `rdfs:label`

Use a short, action-oriented phase name.

Aim for 5 to 12 words.

Name the phase of activity, not a single technical action.

#### `alsoCalled`

Include common alternative names for the phase only.

Do not use tool names, campaign names, or overly narrow incident names as aliases.

#### `shortDescription`

Use one sentence.

Maximum length: 40 words.

Make the four core Diamond Model elements explicit at a high level.

#### `longDescription`

Use up to 250 words.

Explain the phase role, the four Diamond Model elements, and relationships to Patterns, Markets, and chained Events.

#### `variant`

Capture recurring variations in how the Event is performed, without creating a separate Event.

Maximum length: 40 words per variant.

<a id="diamond-event-label-guidance"></a>

### Label Guidance

#### Intent

The label should provide a compact, human-readable name for the phase of activity.

It should be recognizable in lists and diagrams without requiring the reader to open the full description.

It should emphasize the illicit or adverse cyber activity and the role of the adversary.

#### Content Rules

A good Diamond Event label should:

- Capture the phase-level outcome or purpose.
- Focus on what is happening in that step.
- Implicitly reflect the four core elements without listing them explicitly.
- Convey the illicit or exploitative nature of the activity.
- Avoid neutral wording such as `Email campaign`.
- Avoid proper campaign names.
- Avoid overly technical jargon or long enumerations.

If the Event is reusable across diverse Patterns, make the label generic but specific enough to be useful.

Use the schema to mark or classify Common Events where possible, rather than forcing the word `Common` into the label unless the data model requires it.

#### Suggested Label Structure

```text
[Pattern or Common] + [adversary action] + [target or goal] + [key vector]
```

#### Example Label Patterns

```text
Credential harvesting via cloned webmail portal
Initial access via commodity ransomware affiliate kit
Account takeover using SIM-swap fraud
```

<a id="diamond-event-short-description-guidance"></a>

### Short Description Guidance

#### Intent

The `shortDescription` should provide a single-sentence summary of the Diamond Event as a complete phase.

It should make the linkage between the four core elements explicit at a high level.

It should allow a reader to quickly decide whether this Event is the one they want.

#### Content Rules

In 40 words or less, the short description should:

- Describe a single, recognizable illicit or adverse activity.
- Make clear that the activity is cyber-dependent or cyber-enabled.
- Reference the adversary or role player.
- Reference the capability or threat action.
- Reference the infrastructure, platform, or commodity.
- Reference the victim or impact.
- Avoid including the name of the Diamond Event.
- Optionally indicate the broader Pattern or Market context.
- Optionally indicate whether the Event is reusable across multiple Patterns.

#### Suggested Short Description Structure

```text
A [role player] uses [capability] via [infrastructure] to [impact on victim] as [phase role] in [Pattern or Market context].
```

<a id="diamond-event-long-description-guidance"></a>

### Long Description Guidance

#### Intent

The `longDescription` should provide a multi-dimensional narrative of the phase.

It should explain:

- Who acts.
- What they do.
- Where or how they do it.
- Against whom they act.
- What effect the activity has.
- How the Event fits into larger Patterns, Markets, and Event chains.

#### Content Rules

Within 250 words, the long description should:

- Characterize the adversary or role player.
- Describe the capability or threat actions at phase level.
- Explain the infrastructure, platform, or commodity.
- Detail the victim and impact.
- Position the Event in larger structures such as Patterns, Markets, and chained Events.
- Explain Common Event status if the Event is reusable across diverse Patterns.
- Avoid full procedural detail, command-level steps, or indicators of compromise.

#### Suggested Long Description Structure

**Paragraph 1: Context and phase role**

Identify the activity as a Diamond Event and summarize its purpose and phase within Patterns.

**Paragraph 2: Four elements**

Describe Adversary, Capability, Infrastructure, Victim, and Impact in an integrated narrative.

**Paragraph 3: Relationships and reuse**

Explain links to Patterns, Markets, common predecessor or successor Events, and whether the Event is reusable.

<a id="diamond-event-template"></a>

### Diamond Event Template

```text
Label:
[Pattern or Common] + [phase-level action] + [target or goal] + [key vector]

alsoCalled:
[Common alternative names for the phase, if any]

shortDescription:
A [role player] uses [capability] via [infrastructure] to [impact on victim] as [phase role] in [Pattern or Market context].

longDescription:
[Paragraph 1: Identify the activity as a Diamond Event and explain its phase role.]

[Paragraph 2: Describe the role player, capability, infrastructure, victim, and impact.]

[Paragraph 3: Explain Pattern, Market, chaining, reuse, or Common Event relationships.]

variant:
[Optional recurring variation, 40 words or less.]
```

[Back to top](#top)

---

<a id="products-and-services--commodities"></a>

## Products and Services / Commodities

<a id="products-and-services-purpose"></a>

### Purpose

A Products and Services entity, also referred to as a commodity, describes a product, service, tool, dataset, credential set, infrastructure service, or other tradable or usable item in the cybercrime ecosystem.

A commodity can be added to any number of Diamond Events for a given Pattern.

A Diamond Event can be linked to any number of commodities.

A commodity can be linked to any number of Diamond Events.

<a id="products-and-services-field-rules"></a>

### Field Rules

#### `rdfs:label`

Name the commodity, product, service, or tradable category.

#### `alsoCalled`

Include common marketplace names, slang, abbreviations, or ecosystem terms.

#### `shortDescription`

Define what is traded or used and why it matters operationally.

#### `longDescription`

Describe the function, buyers and sellers, operational role, and relationship to Patterns, Markets, or Diamond Events.

#### `variant`

Capture common variations in product form, service model, delivery model, or use context.

<a id="products-and-services-template"></a>

### Products and Services Template

```text
Label:
[Product, service, tool, dataset, credential set, or commodity category]

alsoCalled:
[Common marketplace names, slang, or abbreviations]

shortDescription:
[One-sentence explanation of what the commodity is and what it enables.]

longDescription:
[Paragraph 1: Define the commodity and its function.]

[Paragraph 2: Explain how it is obtained, sold, rented, operated, or used.]

[Paragraph 3: Explain its relationship to Patterns, Markets, role players, or Diamond Events.]

variant:
[Optional recurring variation, 40 words or less.]
```

[Back to top](#top)

---

<a id="market"></a>

## Market

<a id="market-purpose"></a>

### Purpose

A Market represents a supply chain, underground service, managed service, or trading context in which products, services, or activities are exchanged.

<a id="market-field-rules"></a>

### Field Rules

#### `rdfs:label`

Name the market, supply chain, or service model.

#### `alsoCalled`

Include common market names, ecosystem terms, or abbreviations.

#### `shortDescription`

Summarize what is traded, who participates, and what the Market enables.

#### `longDescription`

Describe traded commodities, buyers, sellers, platforms, role players, and links to Patterns or Diamond Events.

#### `variant`

Capture recurring market-model variations.

<a id="market-template"></a>

### Market Template

```text
Label:
[Market, supply chain, or service model name]

alsoCalled:
[Common alternative terms]

shortDescription:
[One-sentence summary of what is traded and what the Market enables.]

longDescription:
[Paragraph 1: Define the Market and the activity or service model.]

[Paragraph 2: Describe buyers, sellers, role players, commodities, and platforms.]

[Paragraph 3: Explain links to Patterns, Diamond Events, or other Markets.]

variant:
[Optional recurring variation, 40 words or less.]
```

[Back to top](#top)

---

<a id="role-player"></a>

## Role Player

<a id="role-player-purpose"></a>

### Purpose

A Role Player describes a functional role in the cybercrime ecosystem.

A Role Player is not a named person, organization, campaign, or incident.

<a id="role-player-field-rules"></a>

### Field Rules

#### `rdfs:label`

Name the role, not an individual person, group, or campaign.

#### `alsoCalled`

Include common role aliases, slang, or ecosystem terms.

#### `shortDescription`

State what the role player does and how they contribute to the activity.

#### `longDescription`

Describe responsibilities, capabilities, relationships to other roles, and where the role appears in Patterns, Markets, or Diamond Events.

#### `variant`

Capture recurring variations in role specialization, operating model, or relationship to other roles.

<a id="role-player-template"></a>

### Role Player Template

```text
Label:
[Functional role name]

alsoCalled:
[Common role aliases or ecosystem terms]

shortDescription:
[One-sentence description of what the role player does.]

longDescription:
[Paragraph 1: Define the role and its main responsibilities.]

[Paragraph 2: Describe capabilities, resources, and operating context.]

[Paragraph 3: Explain relationships to other roles, Markets, Patterns, or Diamond Events.]

variant:
[Optional recurring role variation, 40 words or less.]
```

[Back to top](#top)

---

<a id="platform"></a>

## Platform

<a id="platform-purpose"></a>

### Purpose

A Platform describes infrastructure, services, environments, or channels that enable activity in Patterns, Markets, or Diamond Events.

<a id="platform-field-rules"></a>

### Field Rules

#### `rdfs:label`

Name the platform type or infrastructure category.

#### `alsoCalled`

Include common platform labels, ecosystem terms, or slang.

#### `shortDescription`

Explain what the platform enables.

#### `longDescription`

Describe how the platform is used, who uses it, what it supports, and how it relates to Patterns, Markets, or Diamond Events.

#### `variant`

Capture recurring variations in platform type, access model, or abuse context.

<a id="platform-template"></a>

### Platform Template

```text
Label:
[Platform or infrastructure category]

alsoCalled:
[Common alternative terms]

shortDescription:
[One-sentence explanation of what the platform enables.]

longDescription:
[Paragraph 1: Define the platform and its function.]

[Paragraph 2: Explain how it is accessed, operated, or abused.]

[Paragraph 3: Explain links to Patterns, Markets, commodities, or Diamond Events.]

variant:
[Optional recurring platform variation, 40 words or less.]
```

[Back to top](#top)

---

<a id="victim"></a>

## Victim

<a id="victim-purpose"></a>

### Purpose

A Victim entity describes a victim group, target category, or affected population.

<a id="victim-field-rules"></a>

### Field Rules

#### `rdfs:label`

Name the victim group or target category.

#### `alsoCalled`

Include widely used alternative victim-group names.

#### `shortDescription`

Identify who is affected and the relevant exposure or harm context.

#### `longDescription`

Describe why the group is targeted, how it is affected, and which Patterns or Diamond Events commonly involve it.

#### `variant`

Capture recurring variations in victim type, sector, geography, scale, or exposure.

<a id="victim-template"></a>

### Victim Template

```text
Label:
[Victim group or target category]

alsoCalled:
[Common alternative victim-group names]

shortDescription:
[One-sentence explanation of who is affected and why the group matters.]

longDescription:
[Paragraph 1: Define the victim group.]

[Paragraph 2: Explain why the group is targeted or exposed.]

[Paragraph 3: Describe common impacts and links to Patterns or Diamond Events.]

variant:
[Optional recurring victim variation, 40 words or less.]
```

[Back to top](#top)

---

<a id="harm"></a>

## Harm

<a id="harm-purpose"></a>

### Purpose

A Harm entity describes an adverse impact or consequence experienced by a victim.

<a id="harm-field-rules"></a>

### Field Rules

#### `rdfs:label`

Name the harm or impact type.

#### `alsoCalled`

Include recognized alternative terms, not incident-specific phrases.

#### `shortDescription`

Define the harm in plain language.

#### `longDescription`

Explain how the harm arises, who experiences it, and how it differs from related harms.

#### `variant`

Capture recurring variations in how the harm manifests.

<a id="harm-template"></a>

### Harm Template

```text
Label:
[Harm or impact type]

alsoCalled:
[Recognized alternative terms]

shortDescription:
[One-sentence plain-language definition of the harm.]

longDescription:
[Paragraph 1: Define the harm.]

[Paragraph 2: Explain how the harm arises in cybercrime activity.]

[Paragraph 3: Explain who experiences it and how it differs from related harms.]

variant:
[Optional recurring harm variation, 40 words or less.]
```

[Back to top](#top)

---

<a id="technique"></a>

## Technique

<a id="technique-purpose"></a>

### Purpose

A Technique describes a technical or operational action at a level below a Diamond Event.

A Technique should support understanding of what happens within a phase, without replacing the phase-level Diamond Event description.

<a id="technique-field-rules"></a>

### Field Rules

#### `rdfs:label`

Use the recognized technique name where available.

#### `alsoCalled`

Include common aliases, ATT&CK-style names, or recognized alternative labels where applicable.

#### `shortDescription`

Define the technical action at a high level.

#### `longDescription`

Explain the technique purpose, typical use, and relationship to Pattern Phases.

Avoid procedural how-to detail.

#### `variant`

Capture recurring variations in technique use or implementation.

<a id="technique-template"></a>

### Technique Template

```text
Label:
[Recognized technique name]

alsoCalled:
[Common aliases or recognized alternative technique names]

shortDescription:
[One-sentence high-level definition of the technique.]

longDescription:
[Paragraph 1: Define the technique and its purpose.]

[Paragraph 2: Explain typical use at phase level.]

[Paragraph 3: Explain links to Pattern Phases, Tactics, or broader activity.]

variant:
[Optional recurring technique variation, 40 words or less.]
```

[Back to top](#top)

---

<a id="reusable-templates"></a>

## Reusable Templates

<a id="generic-entity-template"></a>

### Generic Entity Template

Use this when no more specific class template exists.

```text
Label:
[Preferred human-readable entity name]

alsoCalled:
[Common aliases, if any]

shortDescription:
[One-sentence concise summary, 40 words or less unless class-specific guidance differs.]

longDescription:
[Full analytic description, 250 words or less unless class-specific guidance differs.]

variant:
[Optional recurring variation, 40 words or less.]
```

<a id="class-guidance-template"></a>

### Class Guidance Template

Use this structure when adding guidance for a new class.

```text
## [Class Name]

### Purpose

[Explain what this class represents.]

### Field Rules

#### `rdfs:label`

[Label rule.]

#### `alsoCalled`

[Alias rule.]

#### `shortDescription`

[Short description rule.]

#### `longDescription`

[Long description rule.]

#### `variant`

[Variant rule.]

### [Class Name] Template

Label:
[...]

alsoCalled:
[...]

shortDescription:
[...]

longDescription:
[...]

variant:
[...]
```

[Back to top](#top)

---

<a id="review-checklists"></a>

## Review Checklists

<a id="general-checklist"></a>

### General Checklist

- [ ] Uses American English.
- [ ] Applies the rule for the entity's class.
- [ ] Uses the shared field rule only when no class-specific rule exists.
- [ ] `shortDescription` follows the relevant class-specific length and content rule.
- [ ] `longDescription` follows the relevant class-specific length and content rule.
- [ ] `alsoCalled` includes only useful, recurring aliases.
- [ ] `variant` describes a recurring variation, not a separate entity.
- [ ] Description avoids unnecessary time-specific or incident-specific detail.
- [ ] Description avoids operational how-to instructions.

<a id="pattern-checklist"></a>

### Pattern Checklist

- [ ] Represents recurrent activity.
- [ ] Represents recognizable activity.
- [ ] Has a significant cyber component.
- [ ] Describes illicit, adverse, or exploitative activity.
- [ ] Cannot be reduced to a single TTP or Diamond Event.
- [ ] `longDescription` covers illicit activity, Diamond Event flow, role players, ecosystem elements, victims, and impacts.

<a id="diamond-event-checklist"></a>

### Pattern Phase / Diamond Event Checklist

- [ ] Describes a single phase of activity.
- [ ] Includes Adversary / Role Player.
- [ ] Includes Capability / Threat Action.
- [ ] Includes Infrastructure / Platform or Commodity.
- [ ] Includes Victim / Impact.
- [ ] Label is short, action-oriented, and typically 5 to 12 words.
- [ ] Label names a phase, not a single technical action.
- [ ] `shortDescription` is one sentence and 40 words or less.
- [ ] `shortDescription` makes the four core elements explicit at a high level.
- [ ] `longDescription` explains phase role, four elements, and relationships.
- [ ] Reuse or Common Event status is explained where relevant.
- [ ] Description avoids full procedural detail and indicators of compromise.

<a id="products-and-services-checklist"></a>

### Products and Services / Commodities Checklist

- [ ] Describes a product, service, tool, dataset, credential set, infrastructure service, or other commodity.
- [ ] Explains what the commodity enables.
- [ ] Describes how it may be bought, sold, rented, operated, or used.
- [ ] Links to relevant Patterns, Markets, or Diamond Events where appropriate.

[Back to top](#top)

---

<a id="editorial-review-notes"></a>

## Editorial Review Notes

The source Word document contains several editorial issues that should be resolved in future revisions.

<a id="pattern-section-formatting-note"></a>

### Pattern Section Formatting

The Pattern section contains a note indicating a formatting mistake.

The substantive Pattern guidance has been preserved, but the formatting issue should be reviewed in the source material before future publication.

<a id="compound-or-composite-events-note"></a>

### Compound or Composite Events

The Diamond Events section notes that compound events should be described.

This guide currently refers to Event chaining and reusable Common Events, but a future section should define Compound or Composite Events explicitly.

Suggested future section:

```text
## Compound or Composite Diamond Events

### Purpose

[Define when a Diamond Event should be modeled as compound or composite.]

### Modeling Rules

[Explain when to chain Events, when to create a CompositePatternPhase, and when to reuse Common Events.]
```

<a id="diamond-event-name-note"></a>

### Diamond Event Name in `longDescription`

The source document contains an unresolved note asking whether a Diamond Event `longDescription` should include the name of the Diamond Event.

Current working rule:

A Diamond Event `shortDescription` should not include the Diamond Event name.

A Diamond Event `longDescription` may include the Diamond Event name when it improves clarity, but should not simply repeat the label without adding analytic value.

[Back to top](#top)

---

<a id="future-guidance"></a>

## Future Guidance

This guide should be extended over time with class-specific rules for additional ontology classes and subclasses.

Recommended future sections include:

- `Market_or_Supply_Chain`
- `Underground_Service`
- `Underground_Managed_Service`
- `Crimeware`
- `Payment_Instruments`
- `Credential_and_Identity_Artifacts`
- `Infrastructure_Services`
- `Specific_Victim_Groups`
- `General_Victim_Groups`
- `Economic_Impact`
- `Psychological_Impact`
- `Operational_Impact`
- `Physical_Impact`
- `Tactic`

[Back to top](#top)

---

<a id="suggested-repository-structure"></a>

## Suggested Repository Structure

A simple initial structure is:

```text
docs/
  index.md
  ontology-reference.md
  writing-guide.md
```

As the writing guidance grows, split the guide into child pages.

```text
docs/
  writing-guide/
    index.md
    shared-rules.md
    class-specific-rules.md
    patterns.md
    pattern-phases.md
    markets.md
    products-and-services.md
    role-players.md
    platforms.md
    victims.md
    harms.md
    techniques.md
    review-checklists.md
```

For GitHub Pages navigation, the parent page can use this front matter:

```yaml
---
title: Writing Guide
layout: default
nav_order: 3
has_children: true
---
```

Child pages can use this front matter:

```yaml
---
title: Pattern Phases
layout: default
parent: Writing Guide
nav_order: 4
---
```

[Back to top](#top)
