# Project Cosmos

**White Paper**

---

## Table of Contents

1. [Introduction: Why the Cybercrime Ecosystem Ontology and Graph?](#1-introduction)
2. [The Structure and Terminology of the Ontology](#2-structure-and-terminology)
3. [Methodology](#3-methodology)
4. [Use Cases](#4-use-cases)
5. [Future Development](#5-future-development)
6. [References](#references)

---

## 1. Introduction

Cybercrimes are not single isolated events, but complex processes involving multiple phases, actors, actions, and tools. As a result, the cybercrime ecosystem is expansive, incorporating a myriad of online and offline settings where malicious actors interact to exchange goods, services, or knowledge, and where they employ their tools and skills to attack potential victims.

The complexity of cybercrimes has led to numerous frameworks aimed at breaking them down into understandable events. For instance, academic and non-academic sources have developed typologies and taxonomies [1], ontologies have been proposed across the social sciences [2], crime scripts have been frequently used in criminology [3], and cyber kill chain models are applied in cybersecurity to analyse advanced persistent threats [4]. In parallel, the vast, diverse structures of the cybercrime ecosystem have been analysed using social network analysis [5] or with a variety of machine learning approaches [6]. There is, however, no adequate framework that allows the individual cybercrime processes to be comprehensively understood within the broader, networked cybercrime ecosystem in a manner that is both integrated and practically usable.

Furthermore, disruption of cybercrime on a large scale involves collaboration between multiple organizations, yet different organizations often use different terms to describe the same concepts, making communication difficult. A shared classification system to understand the cybercrime ecosystem can bridge this gap, thereby facilitating multi-agency transnational collaboration across public and private institutions and academia. [7]

For these reasons, **Project Cosmos** was created. It provides an ontology, a graph, and a powerful visual tool that maps actors, activities, commodities, and relationships across the digital criminal ecosystem. The three components of Project Cosmos are intended to be used by both specialist and non-specialist researchers, journalists, and practitioners from a wide variety of organizations, offering a comprehensive, coherent, and accessible representation of the actors and their intricate interrelationships within the dynamic cybercriminal ecosystem.

Thus, the project helps The World Economic Forum's Cybercrime Atlas progress towards its goals. The Cybercrime Atlas is a collaborative, cross-sector research initiative hosted by the WEF Centre for Cybersecurity that brings together private-sector cybersecurity firms, financial institutions, technology companies, investigators, and law-enforcement stakeholders to develop a shared knowledge base of the cybercriminal ecosystem. A central element of the initiative is its effort to "map" cybercrime: community members use open-source research and publicly available materials to identify relationships among criminal operations, threat actors, networks, infrastructure, and enabling services. This mapping function is intended not merely as a descriptive exercise, but as a basis for pooled analysis, operational collaboration, and coordinated disruption of cybercriminal activity.

This white paper introduces potential users to the components of Project Cosmos by describing the structure and terminology of the ontology, outlining the methodology used to develop it and the graph, providing details regarding the related deliverables such as the visual app, and discussing use cases and possibilities for how the project will be expanded in the future.

---

## 2. Structure and Terminology

In order to accurately represent the complexity of the cybercrime ecosystem, the ontology is divided into hierarchically and horizontally interconnected classes known as *Patterns*, *Pattern Phases*, *Role Players*, *Techniques*, *Platforms*, *Products and Services*, *Markets*, *Victims*, and *Harms*. This ontology is then mapped onto the graph that represents the interconnected nature of real-world entities.

The ontology defines the conceptual structure of the domain by specifying the types of entities that can exist and the relationships that may hold between them, effectively providing a shared vocabulary and set of rules for representing knowledge. In contrast, the graph consists of concrete statements that use this vocabulary to describe specific instances and their relationships, forming a network of interconnected data. Although both the ontology and the graph may be encoded together in a single OWL/RDF document, they represent distinct components: the ontology establishes the framework for meaning, while the graph captures the actual information expressed within that framework.

The characteristics of each of the interconnected classes in the cybercrime cosmos ontology that are subsequently mapped to the graph are detailed below.

### Pattern

The largest class in a hierarchical sense is made up of **Patterns**, which are structured models representing a recurrent, recognizable manifestation of illicit, harmful cyber-dependent or cyber-enabled activity. The sample of Patterns currently available in the ontology are: Cyber Extortion, Business Email Compromise, Romance Scam, Initial Access Broker Operation, and Carding; however, this is an initial sample that will be updated.

Given that criminal activity can be known by different names in different institutions or contexts, the ontology allows for an `alsoCalled` property to be attributed to all elements that make up the ecosystem. In the case of Cyber Extortion, for example, the ontology captures that this can also be called "Ransomware", "CyX", or "Double Extortion".

Patterns encompass multiple, diverse Pattern Phases that collectively express a coherent operational or business model, without implying criminality or attribution.

### Pattern Phase

**Pattern Phases** describe a single, recognizable, illicit, adverse, or exploitative cyber-dependent or cyber-enabled activity. They collectively constitute a Pattern and are chained together in the sequential order they typically occur within the Pattern, although in practice some may take place simultaneously. In the ontology, the phases are linked to the Pattern through the `involvesPatternPhase` property and the order is set by assigning a number to `PatternPhaseSequence`.

For example, as can be observed in Figure 1, the Cyber Extortion Pattern consists of 8 Pattern Phases in the following order: Recon, Initial Access, Lateral Movement, Preparation, Exfiltration, Encryption, Extortion, and Monetization.

![Figure 1: Cyber Extortion Pattern — 8 sequential Pattern Phases (involvesPatternPhase relationship)](cyber_extortion_pattern_phases.png)

*Figure 1. Cyber Extortion Pattern — 8 sequential Pattern Phases (involvesPatternPhase relationship)*

Each of these Pattern Phases is made up of four interconnected core elements: Role Player, Technique, Platform or Product and Service, and Victim. This structure is conceptually based on the Diamond Model of Intrusion Analysis [7], which conceives malicious events as containing four core interrelated features arranged in a diamond — that is, they are not ordered hierarchically but as interconnected elements.

### Role Player

Roles performed within the cybercrime ecosystem are referred to as **Role Players**. As the ontology is a conceptual model, a Role Player is understood as a function that someone or something can perform, rather than a specific actor who might perform one or more roles. In the Cyber Extortion example, some Role Players are present across all phases of that Pattern (e.g., Ransomware Affiliates), while others are only relevant to specific phases (e.g., Data Broker Services or Money Mules). These latter examples also demonstrate the horizontal, interconnected nature of the ecosystem, as Data Broker Services and Money Mules can be Role Players in phases of multiple cybercrime Patterns — such as CyX Monetization, BEC Post-Fraud Laundering, or Carding Monetization.

### Technique

This class describes specific MITRE ATT&CK or CAPEC threat action techniques used during an illicit cyber-dependent or cyber-enabled activity. It is more granular than a Pattern Phase and refers to a specific illicit action a Role Player would or could perform during that phase. Similarly to Role Players, Techniques can be linked to one or more phases present in multiple Patterns.

As can be observed in Figure 2, the Monetization phase of Cyber Extortion involves Financial Theft, which is a Technique that can also be found in phases of other Patterns — such as Romance Victim Exploitation or BEC Fraud Transaction. Figure 2 also shows that these relationships are expressed as `patternPhaseInvolveThreat` or `patternPhaseCouldInvolvesThreat` in the ontology.

![Figure 2: The Pattern Phase CyX Monetization as displayed in the ecosystem map](cyx_monetization_hub_updated.png)

*Figure 2. The Pattern Phase CyX Monetization as displayed in the ecosystem map.*

Techniques are directly based on MITRE ATT&CK techniques or the Common Attack Pattern Enumeration and Classification (CAPEC) and are linked to these where possible. For instance, Financial Theft corresponds to MITRE ATT&CK technique T1657. As in the MITRE knowledge base, Techniques are linked to a broader Tactic via a relationship property.

### Platform

**Platforms** are generally-described technology services, applications, or platforms used to facilitate a Pattern Phase, transaction, exchange of value, or communication between Role Players — in other words, the technical venue (website, forum, app, hosting) where activity or trade takes place. Cryptocurrency exchanges are an example of a Platform type connected to many forms of cybercrime activity.

### Product and Service

**Products and Services** (also known as commodities) refer to specific products or services that criminals trade or deploy, such as a phishing kit, zero-day exploit, or escrow service.

Platforms and Products and Services can be linked to both Markets and Pattern Phases, thereby mapping the interconnected nature of the cybercrime ecosystem and facilitating the identification of transversal entities. For instance, cryptocurrency mixers are a service related to Cyber Extortion, Business Email Compromise, and Romance Scamming. In contrast, dating websites are central to Romance Scamming but are not related to the other Patterns in the current sample.

### Market

**Markets** are not one of the four core elements of Pattern Phases, but they are central to the cybercrime ecosystem. The term refers to a structured system where buyers and sellers interact to exchange specific types of products and services via different platforms. A Market entity is linked to an arbitrary number of Role Players, Platforms, and Products and Services, and is designed to be linked to other Markets or Pattern Phases to indicate how it contributes to the creation of a given pattern.

The Infrastructure Market provides a good example of how ontology properties capture commercial dynamics within the cybercrime ecosystem. As shown in Figure 3, the `IsBoughtByRole` property connects the Infrastructure Market with Ransomware Operators, Ransomware Affiliates, RaaS Operators, and Payment Platform Exploiters, while the `IsSoldByRole` property relates it to Proxy Providers, Bulletproof Hosting Providers, VPN Service Providers, and Botnet Operators.

![Figure 3: Infrastructure Market and related buyers, sellers, and platforms](infrastructure_market_hub.png)

*Figure 3. Infrastructure Market and related buyers, sellers, and platforms.*

### Victim

**Victims** are entities that can be targeted or affected in a Pattern Phase. Instances represent individuals, organizations, systems, or groups that suffer harm or attacks. Subclasses specify whether they are general victim groups, or specific types of victims. This class has not been fully developed in the current version of the ontology, but it constitutes a key area for future development.

### Harm

The **Harm** class captures all types of negative consequences that victims can suffer during or after a Pattern Phase. It includes concrete harms (such as financial losses or operational disruptions) as well as broader effects (business or societal impacts). Each subclass of Harm (such as Economic Impact or Psychological Impact) represents a specific dimension of harm, allowing the model to capture both immediate and downstream damages associated with cyber events. As with Victims, this class is not fully developed in the current version of the ontology.

---

## 3. Methodology

The ontology has been developed by a multidisciplinary team with members from the public and private sectors and academia. It is hosted by the Cybercrime Atlas at the World Economic Forum, and the development process has been coordinated by Orange Cyberdefense Security Intelligence & Research. Other collaborators on the ontology are affiliated with Santander, Scitum | TELMEX, Trend Micro, and the Universitat de Girona.

The process began with extensive literature review and an examination of existing ontologies, frameworks, and taxonomies within the domain. Having identified the requirement for a public-domain data structure, taxonomy, and dictionary that allows individual cybercrime processes to be understood within the broader cybercrime ecosystem, a diverse set of stakeholders was identified, including law enforcement agencies, legislators, academia, researchers, students, journalists, and cybersecurity professionals.

A dedicated work stream was created within the Atlas community, staffed and led by Atlas volunteers. Work commenced mid-2024 with the following defined goals:

- **Design the ontology itself**, identifying the objects, relationships, and attributes required.
- **Populate the ontology** by identifying and using open-source information to describe the entities in the ecosystem. A collaborative and democratic process was used within the working group to achieve consensus on definitions and relationships. The Stanford University WebProtégé platform was used for data capture and management, while common project management approaches and tools were leveraged to track inputs, decisions, and outputs.
- **Design and develop a specialized visualization platform** to allow investigation, interrogation, and exploration of the resulting knowledge graph. A lightweight JavaScript application for the web was sponsored by Orange Cyberdefense, developed and tested in parallel with the data population process.
- **Identify and implement an appropriate data structure.** RDF was selected to provide the graph-based structure, OWL to add ontology meaning and reasoning rules, and XML as the preferred output format. Graph data is converted into a proprietary JSON structure for use within the visualization application.
- **Identify and implement appropriate communication platforms.** Filtered data download was implemented within the web application, and GitHub was selected as a repository for data sharing, documentation, and (future) collaboration. Any information generated by the project is made available under the [Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International Public License](https://creativecommons.org/licenses/by-nc-nd/4.0/).

A **victim-centric approach** was adopted to define the scope of the taxonomy, beginning with the experiences of individuals or businesses directly affected by illicit cyber activities, then identifying the primary perpetrators and mapping outward to related actors, services, and networks. This approach also bypassed difficult questions regarding definitions of legality and law, and potentially weighted terminology such as "criminal".

An ontology-based modelling approach was followed to define the relevant domain concepts and the relationships between them. Content was represented as a graph in which object instances formed nodes and explicitly defined relationships formed edges. Data properties were used to add richer information where appropriate. Vocabularies of standard objects, attributes, and relationship types were developed iteratively to guide consistent adoption while allowing new values to be added when needed. Later in the process, detailed writing and style guides were developed — also iteratively — to improve efficiency while providing consistency.

The resulting structures and knowledge graph were occasionally tested with other experts, but no systematic review has been conducted outside of the core development team as yet.

### Deliverables

The deliverables produced by the project thus far are:

- **The ontology itself.** The theoretical structure described above and in the onboarding document.
- **Supporting documents**, such as writing guides for each class and an onboarding document. These support future expansion of the graph and the necessary adaptations to the ever-evolving cybercrime landscape.
- **Graph v1.** The first attempt to map out a sample set of patterns using the ontology, shared as an RDF/XML file. Development of the graph was guided by the need to be sufficiently detailed to provide useful insights but parsimonious enough to allow for swift navigation in the associated app.
- **The visual app.** A tool for the stakeholders mentioned in the introduction to this white paper and a proof of concept for the application of the ontology to a broad audience.

---

## 4. Use Cases

The main objective of the ontology is to provide a comprehensive but understandable overview of the cybercrime ecosystem. Beyond visualization, it functions as a shared analytical backbone through which diverse stakeholders can structure, interpret, and act upon complex cybercrime data. Its utility can be understood through five potential use cases:

### Training, Education, and Capacity Building

The ontology and visual application enable law enforcement agencies, judicial institutions, and other stakeholders to build a structured understanding of cybercrime processes. Police academies and specialist units can train officers on the full operational lifecycle and context of cybercrimes — tracing, for example, how a ransomware attack progresses sequentially from Recon through to Monetization — without requiring deep prior technical knowledge. Figure 4 displays a screenshot of the Cyber Extortion Pattern within the visual app.

![Figure 4: Screenshot of the Cyber Extortion Pattern and its related phases in the application](Screenshot_2026-05-06_115506.png)

*Figure 4. Screenshot of the Cyber Extortion Pattern and its related phases in the application.* The shared vocabulary also supports communication between general investigators and specialist cybercrime units collaborating across borders. Equally, judges and prosecutors can use the graph to understand the functional distinctions between Role Players, such as the difference between a Ransomware Affiliate and a RaaS Operator, or the relative position of a Money Mule within an operation, with direct implications for assessments of culpability and sentencing.

### Academic and Policy Research

Researchers and policymakers can use the ontology as a structured framework for analysing the cybercrime ecosystem. Scholars can systematically examine relationships between actors, markets, and activities across Patterns, while policy analysts can trace how specific platforms or services enable multiple forms of cybercrime. This supports more rigorous evaluation of proposed interventions by revealing their potential systemic impact, as well as their limitations.

### Operational Analysis, Threat Intelligence, and Disruption Planning

Investigators and cybersecurity professionals can use the ontology as a unified framework to integrate, structure, and act upon threat intelligence. By mapping actors, infrastructure, and techniques — including those aligned with MITRE ATT&CK or CAPEC — analysts can link related cases, identify shared Role Players, Platforms, and Products and Services, and detect patterns across incidents. This enables the identification of upstream suppliers, intermediary services, and downstream monetization channels. Elements that recur across multiple Patterns, such as cryptocurrency mixers or infrastructure providers, can be prioritized as high-leverage targets for coordinated disruption, supporting a shift from incident-level response to ecosystem-level intervention.

### Cross-Sector and Transnational Collaboration

The ontology establishes a shared operational language for joint investigations and collaborative analysis involving law enforcement, financial institutions, technology companies, and other stakeholders across jurisdictions. By anchoring reporting and intelligence to a common set of nodes and relationships, organizations can reduce translation overhead and improve interoperability. The `alsoCalled` property further enables alignment across differing terminologies and institutional perspectives, facilitating more efficient information sharing and coordinated action at scale.

### Journalism and Public Communication

The visual application makes the cybercrime cosmos more accessible to non-specialist audiences. Journalists and other communicators can use the ontology to contextualize individual incidents within broader operational structures, improving both the accuracy and explanatory depth of reporting. By showing how actors, services, and markets interconnect across multiple crime types — illustrating, for example, how a single enabling service such as a cryptocurrency mixer connects to ransomware, business email compromise, and romance scamming simultaneously — the tool supports more informed public discourse and helps move coverage beyond isolated events toward a clearer understanding of systemic cybercriminal activity.

---

## 5. Future Development

The current version of the ontology covers a limited sample set of Patterns, but as highlighted above, the cybercrime ecosystem is vast and in constant evolution. Several future initiatives are planned, including:

- **Ongoing expansion** — supported by the broader cybersecurity community — to identify new entities and curate relationships as new knowledge regarding the cybercrime ecosystem emerges.

- **A full academic treatment** of the ontology and the graph. This will further contextualize and expand on the descriptions provided herein. It will also help disseminate the ontology within the academic community and allow for peer-reviewed feedback.

- **Structures and processes to support broader collaboration** with external contributors. For the first release, GitHub will be used for pull requests only; other proposed changes should be submitted by email or through the working group. Over time, the goal is to build a broader contributor community in which participants can submit changes directly through GitHub pull requests.

- **A more sophisticated treatment of Victims and Harms.** As noted above, these classes have not been fully developed in the present version of the ontology. The current treatment links naive descriptions of Harms and Victims directly and independently to Pattern Phases. This approach fails to fully capture the victim's perspective or to illustrate the complex chain of cause and effect. Future releases aim to model this area more completely.

- **A complementary ontology** that allows for the mapping of concrete threat intelligence to the theoretical graph. The ontology as it stands aims to model the cybercrime ecosystem at a theoretical level — using, for example, the concept of a "Role Player" rather than the more concrete "Threat Actor" deployed for intelligence and investigations. By creating mappings from real-world intelligence artefacts (such as a Threat Actor's *nom de guerre*) to a theoretical Role Player as a concept in the ontology, the graph can be used to enrich intelligence outputs and construct a "shadow graph" predicting how two real-world entities might be connected in theory.

- **AI-enabled platforms** that make the knowledge graph easier to query, enrich, and maintain. Because the knowledge graph is a formal, structured, and partly self-describing representation of entities and relationships, it can be combined with a graph database and large language model–based interfaces to support more intuitive analysis. Such a platform would allow users to ask questions about the graph using natural-language prompts, while the system translates those prompts into appropriate graph queries and returns explainable, source-linked results. This would provide a powerful capability for law enforcement and other stakeholders who may not be specialists in cybersecurity, especially where real-world threat intelligence is integrated as described above. When connected to the web and other trusted data sources, carefully governed LLM-based tools could also help accelerate the proposal of new entities and the identification of potential new relationships, subject to careful human review and validation.

---

## References

[1] Phillips, K., Davidson, J. C., Farr, R. R., Burkhardt, C., Caneppele, S., & Aiken, M. P. (2022). Conceptualizing Cybercrime: Definitions, Typologies and Taxonomies. *Forensic Sciences, 2*(2), 379–398. https://doi.org/10.3390/forensicsci2020028

[2] Donalds, C., & Osei-Bryson, K. M. (2019). Toward a cybercrime classification ontology: A knowledge-based approach. *Computers in Human Behavior, 92*, 403–418. https://doi.org/10.1016/j.chb.2018.11.039

[3] For a ransomware example, see: Matthijsse, S. R., van 't Hoff-de Goede, M. S., & Leukfeldt, E. R. (2023). Your files have been encrypted: A crime script analysis of ransomware attacks. *Trends in Organized Crime*, 1–27. https://doi.org/10.1007/s12117-023-09496-z. For a phishing example, see: Loggen, J., & Leukfeldt, R. (2022). Unraveling the crime scripts of phishing networks: an analysis of 45 court cases in the Netherlands. *Trends in Organized Crime, 25*, 205–225. https://doi.org/10.1007/s12117-022-09448-z

[4] Lockheed Martin Cyber Kill Chain. https://www.lockheedmartin.com/en-us/capabilities/cyber/cyber-kill-chain.html

[5] Pastrana, S., Hutchings, A., Caines, A., & Buttery, P. (2018). Characterizing Eve: Analysing Cybercrime Actors in a Large Underground Forum. In Bailey, M., Holz, T., Stamatogiannakis, M., & Ioannidis, S. (Eds.), *Research in Attacks, Intrusions, and Defenses*. RAID 2018. Lecture Notes in Computer Science, vol 11050. Springer, Cham. https://doi.org/10.1007/978-3-030-00470-5_10

[6] Hughes, J., Pastrana, S., Hutchings, A., Afroz, S., Samtani, S., Li, W., & Santana Marin, E. (2024). The Art of Cybercrime Community Research. *ACM Computing Surveys, 56*(6), Article 155, 1–26. https://doi.org/10.1145/3639362

[7] Caltagirone, S., Pendergast, A., & Betz, C. (2013). The diamond model of intrusion analysis. *ThreatConnect, 298*(0704), 1–61.
