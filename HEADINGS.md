# HEADINGS.md

**Every `##` and `###` heading in this repository, grouped by document — the fallback for a
question whose subject is unknown.** 87 headings across 29 documents, written whole by
`plover-context`'s `infra/retrieval/gen_headings.py` and edited by hand nowhere. It is a projection
and not a source: a figure read here carries the date the projection was generated, which
`git log -1 --format='%h %ad' HEADINGS.md` answers off the tree rather than out of the text.

[`AGENTS.md`](AGENTS.md) beside it is the entry point, and its three ranked commands come first —
they answer a word that appears in no heading at all, which this cannot.

**The headings sort into two kinds, and the second kind is why the document names below matter more
than the headings under them.** A heading in a root document — `ARCHITECTURE.md`,
`START-HERE.md`, `CONTRIBUTING.md` — names a specification, a lint rule or a tutorial step, and
scanning it works the way scanning any index works. A heading in a `finding-dag/` node does not:
every node carries the same two, `## Inputs` and `## Reasoning`, because
`ARCHITECTURE.md`'s section-presence convention requires them. So for a node the signal is the
**document name and the `#` label above those two** — the node identifier the graph is wired with —
and the way to the right node is `AGENTS.md`'s alias table or the node's own `## Inputs` links,
never a heading search.

- **[AGENTS.md](AGENTS.md)**
    - [Three ways in, in this order](AGENTS.md#three-ways-in-in-this-order)
        - [The words a question uses](AGENTS.md#the-words-a-question-uses)
        - [What may be read, and how a hit may be quoted](AGENTS.md#what-may-be-read-and-how-a-hit-may-be-quoted)
    - [Known gaps — what this layer does not route](AGENTS.md#known-gaps--what-this-layer-does-not-route)
- **[ARCHITECTURE.md](ARCHITECTURE.md)**
    - [Purpose and scope](ARCHITECTURE.md#purpose-and-scope)
    - [Vault structure](ARCHITECTURE.md#vault-structure)
    - [Frontmatter schema](ARCHITECTURE.md#frontmatter-schema)
    - [Conditional keys](ARCHITECTURE.md#conditional-keys)
    - [Section-presence convention](ARCHITECTURE.md#section-presence-convention)
    - [The PRODUCT_NAME placeholder](ARCHITECTURE.md#the-product_name-placeholder)
    - [Lint rules](ARCHITECTURE.md#lint-rules)
    - [What lint cannot check](ARCHITECTURE.md#what-lint-cannot-check)
    - [Sync hazards](ARCHITECTURE.md#sync-hazards)
    - [Obsidian config contract](ARCHITECTURE.md#obsidian-config-contract)
    - [Out of scope](ARCHITECTURE.md#out-of-scope)
- **[CHANGELOG.md](CHANGELOG.md)**
    - [[0.1.12] - 2026-09-06](CHANGELOG.md#0112---2026-09-06)
- **[CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md)**
    - [Our Pledge](CODE_OF_CONDUCT.md#our-pledge)
    - [Our Standards](CODE_OF_CONDUCT.md#our-standards)
    - [Enforcement Responsibilities](CODE_OF_CONDUCT.md#enforcement-responsibilities)
    - [Scope](CODE_OF_CONDUCT.md#scope)
    - [Enforcement](CODE_OF_CONDUCT.md#enforcement)
    - [Attribution](CODE_OF_CONDUCT.md#attribution)
- **[CONTRIBUTING.md](CONTRIBUTING.md)**
    - [Who edits here](CONTRIBUTING.md#who-edits-here)
    - [Before opening a PR](CONTRIBUTING.md#before-opening-a-pr)
    - [Structural-edit checklist](CONTRIBUTING.md#structural-edit-checklist)
    - [Adding a brain](CONTRIBUTING.md#adding-a-brain)
    - [Review heuristic](CONTRIBUTING.md#review-heuristic)
    - [The two gates, by design](CONTRIBUTING.md#the-two-gates-by-design)
    - [Versioning](CONTRIBUTING.md#versioning)
- **[README.md](README.md)**
    - [Map of the docs](README.md#map-of-the-docs)
    - [Layout: one folder per "brain"](README.md#layout-one-folder-per-brain)
    - [Editing](README.md#editing)
    - [License](README.md#license)
- **[SECURITY.md](SECURITY.md)**
    - [What to report here](SECURITY.md#what-to-report-here)
- **[START-HERE.md](START-HERE.md)**
    - [Track A — editing health reasoning](START-HERE.md#track-a--editing-health-reasoning)
        - [The scenario](START-HERE.md#the-scenario)
        - [What's actually in this repo](START-HERE.md#whats-actually-in-this-repo)
        - [Glossary](START-HERE.md#glossary)
        - [Visualizing the graph in Obsidian](START-HERE.md#visualizing-the-graph-in-obsidian)
        - [Making a structural edit](START-HERE.md#making-a-structural-edit)
        - [Checking your edit](START-HERE.md#checking-your-edit)
    - [Track B — wiring the pipeline, or adding a brain](START-HERE.md#track-b--wiring-the-pipeline-or-adding-a-brain)
        - [Breaking the vault on purpose](START-HERE.md#breaking-the-vault-on-purpose)
        - [Reading order](START-HERE.md#reading-order)
        - [Objection: why prose + a lint script, not real schema validation or types?](START-HERE.md#objection-why-prose--a-lint-script-not-real-schema-validation-or-types)
        - [Adding a brain](START-HERE.md#adding-a-brain)
- **[finding-dag/aiFindings.md](finding-dag/aiFindings.md)**
    - [Inputs](finding-dag/aiFindings.md#inputs)
    - [Reasoning](finding-dag/aiFindings.md#reasoning)
- **[finding-dag/aiHypothesis.md](finding-dag/aiHypothesis.md)**
    - [Inputs](finding-dag/aiHypothesis.md#inputs)
    - [Reasoning](finding-dag/aiHypothesis.md#reasoning)
- **[finding-dag/aiOnPlan.md](finding-dag/aiOnPlan.md)**
    - [Inputs](finding-dag/aiOnPlan.md#inputs)
    - [Reasoning](finding-dag/aiOnPlan.md#reasoning)
- **[finding-dag/allergyResults.md](finding-dag/allergyResults.md)**
    - [Inputs](finding-dag/allergyResults.md#inputs)
    - [Reasoning](finding-dag/allergyResults.md#reasoning)
- **[finding-dag/criticalRatios.md](finding-dag/criticalRatios.md)**
    - [Inputs](finding-dag/criticalRatios.md#inputs)
    - [Reasoning](finding-dag/criticalRatios.md#reasoning)
- **[finding-dag/dataRequisition.md](finding-dag/dataRequisition.md)**
    - [Inputs](finding-dag/dataRequisition.md#inputs)
    - [Reasoning](finding-dag/dataRequisition.md#reasoning)
- **[finding-dag/diseaseResults.md](finding-dag/diseaseResults.md)**
    - [Inputs](finding-dag/diseaseResults.md#inputs)
    - [Reasoning](finding-dag/diseaseResults.md#reasoning)
- **[finding-dag/doctorConversation.md](finding-dag/doctorConversation.md)**
    - [Inputs](finding-dag/doctorConversation.md#inputs)
    - [Reasoning](finding-dag/doctorConversation.md#reasoning)
- **[finding-dag/familyResults.md](finding-dag/familyResults.md)**
    - [Inputs](finding-dag/familyResults.md#inputs)
    - [Reasoning](finding-dag/familyResults.md#reasoning)
- **[finding-dag/finalThoughts.md](finding-dag/finalThoughts.md)**
    - [Inputs](finding-dag/finalThoughts.md#inputs)
    - [Reasoning](finding-dag/finalThoughts.md#reasoning)
- **[finding-dag/healthMarkers.md](finding-dag/healthMarkers.md)**
    - [Inputs](finding-dag/healthMarkers.md#inputs)
    - [Reasoning](finding-dag/healthMarkers.md#reasoning)
- **[finding-dag/healthProgression.md](finding-dag/healthProgression.md)**
    - [Inputs](finding-dag/healthProgression.md#inputs)
    - [Reasoning](finding-dag/healthProgression.md#reasoning)
- **[finding-dag/healthSynthesis.md](finding-dag/healthSynthesis.md)**
    - [Inputs](finding-dag/healthSynthesis.md#inputs)
    - [Reasoning](finding-dag/healthSynthesis.md#reasoning)
- **[finding-dag/hypothesisEvaluation.md](finding-dag/hypothesisEvaluation.md)**
    - [Inputs](finding-dag/hypothesisEvaluation.md#inputs)
    - [Reasoning](finding-dag/hypothesisEvaluation.md#reasoning)
- **[finding-dag/markerGroups.md](finding-dag/markerGroups.md)**
    - [Inputs](finding-dag/markerGroups.md#inputs)
    - [Reasoning](finding-dag/markerGroups.md#reasoning)
- **[finding-dag/markerLevels.md](finding-dag/markerLevels.md)**
    - [Inputs](finding-dag/markerLevels.md#inputs)
- **[finding-dag/noteResults.md](finding-dag/noteResults.md)**
    - [Inputs](finding-dag/noteResults.md#inputs)
    - [Reasoning](finding-dag/noteResults.md#reasoning)
- **[finding-dag/patternAntipattern.md](finding-dag/patternAntipattern.md)**
    - [Inputs](finding-dag/patternAntipattern.md#inputs)
    - [Reasoning](finding-dag/patternAntipattern.md#reasoning)
- **[finding-dag/studyResults.md](finding-dag/studyResults.md)**
    - [Inputs](finding-dag/studyResults.md#inputs)
    - [Reasoning](finding-dag/studyResults.md#reasoning)
- **[finding-dag/treatmentAssessment.md](finding-dag/treatmentAssessment.md)**
    - [Inputs](finding-dag/treatmentAssessment.md#inputs)
    - [Reasoning](finding-dag/treatmentAssessment.md#reasoning)
- **[finding-dag/treatmentGroups.md](finding-dag/treatmentGroups.md)**
    - [Inputs](finding-dag/treatmentGroups.md#inputs)
    - [Reasoning](finding-dag/treatmentGroups.md#reasoning)
