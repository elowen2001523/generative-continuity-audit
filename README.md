# Generative Continuity Audit Framework

**A label-neutral, cross-domain framework for auditing generative continuity, conceptual bridges, source lineage, generator identity, semantic transformation, and provenance.**

**Author:** Chuanyan Liu / Elowen
**Version:** v2.0
**Edition:** GitHub Public Release Edition
**Repository:** `generative-continuity-audit`

> **The goal is discrimination, not accusation.**

---

## What is this?

The **Generative Continuity Audit Framework** is a methodology for investigating **how a work was generated over time**.

It can be applied to:

* academic papers and theories
* AI and machine-learning research
* software and technical systems
* product and architecture design
* organizational strategy
* model outputs
* technical writing
* creative works
* provenance and source-lineage research

Traditional similarity analysis usually starts with the finished artifacts:

> Do these two papers use similar words?
> Do these systems contain similar mechanisms?
> Do these diagrams or structures look alike?

This framework asks a different question:

> **Can the target artifact be naturally and continuously generated from the target's own prior history, capabilities, problems, failures, intermediate reasoning, collaborators, and known prior art?**

A similarity may be trivial because both sides use common techniques.

A mechanism may have existed for years without the later conceptual structure having existed.

A paper may contain highly detailed equations and implementation while still providing little historical evidence for the conceptual bridges that determined the theory's shape.

Conversely, something that initially appears discontinuous may be fully explained by an earlier draft, a new contributor, common prior art, independent engineering pressure, AI-assisted research, or another legitimate generation path.

The purpose of the framework is to distinguish these possibilities systematically.

---

## Core idea

The framework does **not** treat similarity as proof of copying.

Instead, it reconstructs generation at six analytical levels:

1. **Artifact** — What does the final work say or do?
2. **Mechanism** — What algorithms, interfaces, structures, or technical mechanisms exist?
3. **Bridge** — Why are particular concepts or mechanisms connected in this specific way?
4. **Generator** — How does the subject repeatedly discover problems, select abstractions, change representations, and reject alternatives?
5. **Generator Identity** — Does that generative fingerprint remain continuous across works and over time?
6. **Generator Population** — How many distinct generators exist inside a team or organization, and how do they divide work, merge, coexist, or change?

The key distinction is simple:

**Having A, B, and C independently is not the same as having historically generated the specific bridge A → B → C.**

The framework therefore audits not only the existence of components, but also the provenance of the **edges between them**.

---

## What v2.0 adds

Version 2.0 extends the original framework from **artifact lineage** into **generator identity, semantic transformation, multi-source generation, and corpus completeness**.

### Generator Identity Continuity

Instead of treating vague impressions such as "this feels stitched together" or "this sounds like a different person" as evidence, v2.0 converts them into auditable generator fingerprints.

Typical dimensions include:

* problem framing
* failure localization
* abstraction preference
* bridge style
* representation moves
* causal explanation
* validation policy
* boundary behavior
* generalization direction
* historical negative space

The framework distinguishes patterns such as:

**Natural evolution**

`A → A′ → A″`

**Team integration**

`A + B → AB → AB′`

**High-attention fragmentation**

`A → A → X → A → Y`

The third pattern is not automatically suspicious. It becomes important only when the appearance of X or Y cannot yet be explained by author changes, prior art, internal development, AI assistance, or other alternative generators.

---

## Authorship and contribution control

Different authors naturally bring different expertise.

For this reason, heterogeneous writing or reasoning inside a multi-author paper is **not** automatically evidence of source dependence.

The framework requires generator discontinuities to be compared against:

* author changes
* contributor expertise
* research background
* first appearance in the project
* commit or version history
* contribution statements
* talks and acknowledgements

If a new mathematical formalism appears at exactly the same time as a researcher with long-standing expertise in that formalism joins the work, that can be strong counterevidence against a lineage anomaly.

---

## Semantic Transformation Chain

Surface-level rewriting can radically change vocabulary without necessarily changing the underlying generative structure.

v2.0 therefore introduces the following audit chain:

**Claim → Abstraction → Terminology Substitution → Formalization → Mechanism → Implementation**

The audit asks:

* What was the original high-level claim?
* How was it abstracted?
* Was it translated into another domain's terminology?
* When did it become a formula, state model, type, graph, constraint, or algorithm?
* How did that formalization become a mechanism?
* How was it ultimately implemented?
* Where is the earliest native trace of each transformation step?

This test can reveal unexplained transformation gaps, but it can also establish independent development when the target possesses its own documented transformation history.

---

## Information Conservation Test

Words, notation, examples, and implementation details can change substantially while deeper structures remain stable.

The framework therefore checks whether transformations preserve high-information features such as:

* relationships
* non-obvious ordering
* asymmetric constraints
* unusual exceptions
* negative space
* rare decomposition patterns
* characteristic failure patterns

A strong signal is not simply that two artifacts discuss similar topics.

A more informative case is when terminology, formulas, and domain all change, while an unusual relationship graph, ordering, exception structure, and omission pattern remain aligned.

Even then, the framework requires prior art, authorship, native lineage, and provenance to be tested before any source-level conclusion is raised.

---

## Historical Negative Space

A generator is partly defined by what it repeatedly does **not** model.

The framework therefore tracks long-standing absence of:

* abstraction families
* vocabulary families
* philosophical commitments
* mathematical representations
* evaluation criteria
* failure concepts

A concept appearing for the first time is not itself anomalous.

Higher information comes from a combination such as:

**long-standing negative space + sudden complete new module + missing transition states + insufficient authorship/prior-art/AI/internal explanation.**

---

## Citation Lineage

Citation behavior can provide an auxiliary map of visible knowledge pathways.

The framework examines:

* canonical literature coverage
* changes in citation neighborhoods
* temporal fit between citations and concepts
* missing canonical pathways
* concentration around bridge-like sources
* continuity with the target's own earlier work

Citation behavior is not equivalent to reading history and cannot prove or disprove access on its own. It is used as supporting lineage evidence.

---

## Compression / Expansion Asymmetry

A high-level conceptual framework can be compressed into a small technical mechanism.

A technical mechanism can also later be expanded into a much broader theory.

v2.0 therefore compares changes in:

* Generative Resolution
* Implementation Resolution
* Historical Resolution
* Boundary Resolution

For example:

**high generative detail / low implementation detail**
may later become
**low generative detail / high implementation detail**

That may simply represent legitimate engineering.

The audit becomes more informative when high-information structural relationships survive the compression while the target lacks an independently traceable transformation history.

---

## Corpus Completeness and Search Exhaustion

Claims about missing history are only meaningful if the search itself is documented.

Every serious audit should therefore include a **Corpus Manifest** describing what was searched and what could not be accessed.

v2.0 defines five Search Exhaustion levels:

| Level                                                      | Coverage                                                                         |
| ---------------------------------------------------------- | -------------------------------------------------------------------------------- |
| **E0 — Superficial**                                       | A small number of public pages or representative papers                          |
| **E1 — Major Public Artifacts**                            | Major papers, official releases, and core repositories                           |
| **E2 — Broad Public History**                              | Adds author pages, talks, interviews, blogs, version history, and major archives |
| **E3 — Version-level Reconstruction**                      | Reconstructs paper, webpage, repository, commit, release, and authorship changes |
| **E4 — Independently Replicated Exhaustive Public Search** | Independent replication with query logs, archives, and hashes                    |

The framework therefore prefers:

> “Under E3-level public corpus coverage, no verifiable intermediate bridge has yet been identified.”

rather than:

> “No intermediate bridge exists.”

---

## Audit workflow

The methodology deliberately separates discovery from source comparison.

A typical v2.0 audit proceeds as follows:

1. Freeze the target, versions, time range, available material, and auditor prior exposure.
2. Build the Corpus Manifest and assign a Search Exhaustion level.
3. Reconstruct the target's history **without examining the candidate source**.
4. Freeze the Target Native Generator and Generator Identity Baseline.
5. Compare target-before and target-after reasoning policies.
6. Extract conceptual bridges.
7. Score the six Resolution dimensions.
8. Run Generative Seam Analysis.
9. Search for missing intermediate states.
10. Build an Authorship / Contribution Matrix.
11. Map Native, Prior-Art, Synthesis, Discontinuity, Identity-Shift, and Transformation Zones.
12. Run Alternative-Generator Tests.
13. Audit Semantic Transformation Chains where relevant.
14. Run Information Conservation tests.
15. Reconstruct Historical Negative Space and Citation Lineage.
16. Examine Compression / Expansion Asymmetry.
17. **Only then reveal the candidate Source.**
18. Compare Generator ↔ Generator and, where necessary, Transformation Chain ↔ Transformation Chain.
19. Finally add chronology, access, knowledge, authorization, and conduct evidence.
20. Record counterevidence and explicit conditions that would change the conclusion.
21. Issue a graded audit finding rather than a pseudo-precise “plagiarism percentage.”

---

## Competing hypotheses

The framework keeps multiple explanations alive simultaneously:

* **H0 — Native Continuity**
  The target evolved primarily from its own lineage.

* **H1 — Common Prior Art / Convergence**
  Similarity is explained by shared literature, engineering pressure, industry constraints, or independent convergence.

* **H2 — External Source Influence / Dependency**
  A specific external source materially influenced important structures, bridges, or generation order.

* **H3 — Mixed Synthesis**
  Native capabilities, prior art, and one or more external sources jointly contributed.

* **H4 — Multi-source Generator Assimilation**
  Different high-level regions may reflect multiple distinct external generators, producing modular or fragmented generator patterns.

H4 must not be assumed merely because a work feels stylistically heterogeneous. It receives weight only when distinct generator fingerprints can be independently identified and stronger alternative explanations fail.

---

## Alternative-generator testing

Every high-weight anomaly must compete against plausible alternative explanations.

These include:

* common prior art
* independent engineering pressure
* collaborators or mentors
* independent literature synthesis
* AI-assisted research
* industry convergence
* unpublished internal research
* authorship changes
* organizational restructuring

A strong alternative explanation should not merely explain why the individual components existed.

It should attempt to explain:

> Why these components?
> Why this ordering?
> Why this bridge?
> Why at this time?
> Why did the same change not appear elsewhere?

---

## Classification levels

The framework uses graded findings rather than binary accusation labels.

| Level    | Classification                        |
| -------- | ------------------------------------- |
| **L0**   | Native Continuity                     |
| **L1**   | Surface Correspondence                |
| **L2-A** | Structural Correspondence             |
| **L2-B** | Generative Discontinuity              |
| **L2-C** | Seam Convergence                      |
| **L2-D** | Generator Identity Anomaly            |
| **L2-E** | Transformation / Conservation Anomaly |
| **L3**   | Lineage Anomaly                       |
| **L4**   | Provenance Convergence                |

**L4 is still not a judicial conclusion.**

Legal liability depends on applicable jurisdiction, protectable subject matter, evidence rules, authorization, exceptions, contracts, and available remedies.

---

## Evidence discipline

The framework distinguishes:

**FACT**
What can be directly verified.

**INFERENCE**
What the evidence makes more or less plausible.

**UNKNOWN**
What cannot currently be established.

**COUNTEREVIDENCE**
Evidence supporting native or benign explanations.

**ALTERNATIVE**
A competing generation path that must be tested.

Every high-weight anomaly should include:

* the strongest independent-development explanation
* the strongest common-prior-art explanation
* the strongest internal-lineage explanation
* the strongest authorship/contributor explanation
* the strongest AI-assisted explanation, where applicable
* missing evidence
* evidence that would lower the current assessment

A forensic framework must be capable of producing evidence that **changes or weakens its own conclusion**. Otherwise, it becomes a confirmation-bias mechanism rather than an audit protocol.

---

## What this framework does **not** do

This framework does not assume that:

* similarity means copying
* technical detail means originality
* abstraction means external origin
* stylistic differences mean multiple sources
* missing public history means misconduct
* formalization differences mean deliberate disguise
* a lineage anomaly automatically establishes plagiarism
* source influence automatically establishes infringement
* an audit classification is a legal judgment

These are explicitly treated as failure modes in v2.0.

---

## Reporting standard

A full audit report may include:

* Scope & cutoff
* Corpus Completeness Statement
* Search Exhaustion Level
* Target Native Generator Freeze
* Generator Identity Baseline
* before/after discontinuity map
* Bridge Provenance table
* Resolution and Seam map
* Authorship / Contribution Matrix
* Semantic Transformation Chain
* Information Conservation Matrix
* Historical Negative Space map
* Citation Lineage Audit
* Zone mapping
* Alternative-Generator Tests
* Source Generator comparison
* Provenance matrix
* Counterevidence
* Open questions
* Current classification and confidence
* Explicit evidence that would change the conclusion

For public communication, the framework favors language such as:

* structural anomaly
* candidate generative discontinuity
* candidate generator-identity anomaly
* unexplained conceptual bridge
* transformation-chain gap
* insufficient public evidence to establish source dependency

rather than prematurely converting analytical findings into factual accusations.

---

## Evidence preservation

For serious provenance research, preserve:

* original files and metadata
* URLs and archived snapshots
* commit hashes
* release/version history
* timestamps
* SHA-256 manifests
* complete email or message threads where relevant
* query logs
* Corpus Manifest
* failed searches
* Chain-of-Custody records

Previous conclusions should not be silently overwritten when new evidence appears; version changes should remain traceable.

---

## Public use and legal note

This framework is a **methodology and research protocol**, not legal advice.

Questions involving copyright, patents, trade secrets, contractual rights, data, privacy, defamation, evidentiary rules, or other legal rights depend on jurisdiction and the specific facts of the dispute.

Structural audit conclusions should therefore remain separate from legal conclusions.

The GitHub Public Release packaging **does not itself create or grant an open-source license**. Users should preserve author and version information when quoting, adapting, or evaluating the framework.

---

## Citation

Recommended citation:

**Chuanyan Liu (Elowen), *Generative Continuity Audit Framework & Manual v2.0*, GitHub Public Release Edition, 2026.**

---

## Framework document

The full methodology is available in:

`Generative_Continuity_Audit_Framework_v2.0_GitHub_Public_Release.pdf`

The public-release PDF contains the complete substantive v2.0 framework together with GitHub-facing release metadata.

---

## Closing principle

A strong source-lineage audit does not win by accumulating more things that “look similar.”

It reconstructs:

**what the target's own history can explain,
what its team and prior art can explain,
how conceptual bridges and generator identities formed,
how meaning changed during formalization and implementation,
which high-information structures survived those transformations,
how complete the available historical corpus is,
and which competing explanations survive serious testing.**

Only after those layers have been separated should chronology, access, authorization, conduct, and other provenance evidence be allowed to converge toward a source-level conclusion.

**The goal is discrimination, not accusation.**
