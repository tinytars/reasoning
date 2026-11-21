# Finding an answer in this repository

**Where an answer is, as opposed to what this repository is or how to edit it.** Forty-four
documents hold about 85,000 B here, and the shape is lopsided on purpose: eight documents at the
root specify and teach, and thirty-six under [`finding-dag/`](finding-dag/) are the content itself,
one note per node of the graph. The expensive mistake is not a slow search but an unaimed one — the
node documents are deliberately uniform, every one of them carrying a `## Inputs` and a
`## Reasoning` section, so a heading search over them returns thirty-six equally plausible hits and
tells a reader nothing. [`README.md`](README.md) says what this repository is and who it is for,
[`START-HERE.md`](START-HERE.md) is the tutorial and [`ARCHITECTURE.md`](ARCHITECTURE.md) is the
exact contract; this file says which document holds a given answer, and restates none of them.

It is also what an agent reads first. The shape is the estate's shared retrieval contract —
`promontory-studio/plover-context`'s `infra/retrieval/CONTRACT.md` — which asks for an entry point
short enough to be read whole, an alias table written by hand, and a generated projection of every
heading beside it.

**On the words below.** [`CLAUDE.md`](CLAUDE.md) bans two words from this repository's framing copy,
and the prose here keeps that rule. The right-hand column does not, and cannot: a node is addressed
by the identifier the graph is wired with, several of which carry one of those words, and `CLAUDE.md`
puts node content and filenames out of its own scope as data-model identifiers. A row naming
`patientPlan.md` is quoting an identifier; the question beside it is written the way this repository
writes.

## Three ways in, in this order

1. **The alias table below**, where the subject is known. It maps the words a question arrives in
   onto the document that answers it, and it is one hop: a row is written only where the document is
   certain, because a missing row is recovered from by the commands below while a wrong row sends a
   question somewhere plausible and empty.

2. **Three ranked commands**, where the table has no row. The third is this repository's own, and it
   is the one to reach for first on a node question — every node declares its label and what it
   reads in frontmatter, so the graph is greppable without opening anything:

   | To find | Command |
   |---|---|
   | the section holding it | `git grep -nE '^#{2,3} .*<word>' -- '*.md'` |
   | the document about it | `git grep -ci <word> -- '*.md' \| sort -t: -k2 -rn \| head` |
   | the node that holds it, by label or by what it reads | `git grep -nE '^(label\|basis\|inputs):.*<word>' -- 'finding-dag/*.md'` |

3. **[`HEADINGS.md`](HEADINGS.md)**, where the subject itself is unknown — every `##` and `###`
   heading in the corpus on one page, 87 of them across 29 documents, generated rather than
   maintained. It indexes the root documents usefully and the nodes barely, for the reason stated
   above and in its own prose.

### The words a question uses

<!-- BEGIN ALIASES -->
| A question saying | Folder or file | Then |
|---|---|---|
| the frontmatter schema, a required key, a conditional key, a lint rule, why `validate-vault.sh` failed | `ARCHITECTURE.md` | — |
| the section-presence convention, the PRODUCT_NAME placeholder, what lint cannot check, sync hazards, the Obsidian config contract | `ARCHITECTURE.md` | — |
| making a first edit, opening the vault in Obsidian, colouring the graph by kind, checking an edit | `START-HERE.md` | — |
| breaking the vault on purpose, the reading order, why prose and a lint script rather than a schema | `START-HERE.md` | — |
| who may edit here, the structural-edit checklist, the two gates, adding a second brain, versioning | `CONTRIBUTING.md` | — |
| what this repository is, who it is for, why it carries no app code, the licence, the graph picture | `README.md` | — |
| reporting a content concern or a security issue | `SECURITY.md` | — |
| the two words this repository never uses in its framing copy, and why | `CLAUDE.md` | — |
| what changed in a version | `CHANGELOG.md` | — |
| the central synthesis, the per-system disease finding | `finding-dag` | `aiFindings.md` |
| the proposed intervention set, the alternatives the tool puts forward | `finding-dag` | `aiHypothesis.md` |
| weighing a hypothesis the person brought, pros, cons and a recommendation on one | `finding-dag` | `hypothesisEvaluation.md` |
| the read on a plan the person wrote, per action and as a whole | `finding-dag` | `aiOnPlan.md` |
| which markers to recommend next, why a standard panel is refused | `finding-dag` | `healthMarkers.md` |
| what data to obtain next, by body system and modality, standard-of-care intervals | `finding-dag` | `dataRequisition.md` |
| a reading against a personalized level rather than a lab's range | `finding-dag` | `markerLevels.md` |
| a meaningful ratio between two markers | `finding-dag` | `criticalRatios.md` |
| every marker assigned to a body system, the grouping axis | `finding-dag` | `markerGroups.md` |
| the trajectory — latest, recent, overall | `finding-dag` | `healthProgression.md` |
| adverse against favorable, the two-track synthesis | `finding-dag` | `healthSynthesis.md` |
| questions to raise at a visit, by disease group or decision | `finding-dag` | `doctorConversation.md` |
| assessing each item of a current regimen | `finding-dag` | `treatmentAssessment.md` |
| treatments partitioned by body system then drug class | `finding-dag` | `treatmentGroups.md` |
| patterns that fit, and the reasoning pitfalls that do not | `finding-dag` | `patternAntipattern.md` |
| the closing summary drawing on every section | `finding-dag` | `finalThoughts.md` |
| the response to each known allergy | `finding-dag` | `allergyResults.md` |
| the response to each diagnosis on file | `finding-dag` | `diseaseResults.md` |
| the response to each family-history entry | `finding-dag` | `familyResults.md` |
| the response to each free-text note | `finding-dag` | `noteResults.md` |
| the answer to each study being pursued | `finding-dag` | `studyResults.md` |
| the raw readings a run starts from | `finding-dag` | `labData.md` |
| the markers somebody chose to track, the watchlist | `finding-dag` | `watchlist.md` |
| markers surfaced alongside the watchlist | `finding-dag` | `recommendedMarkers.md` |
| per-marker personalized targets as an input | `finding-dag` | `personalizedRanges.md` |
| what somebody set out to achieve | `finding-dag` | `statedObjective.md` |
| the unified treatment list, ongoing and past | `finding-dag` | `treatmentHistory.md` |
| planned, future-dated treatments as an input | `finding-dag` | `patientPlan.md` |
| interventions being weighed, as an input rather than evaluated | `finding-dag` | `patientHypothesis.md` |
| diagnoses on file as an input | `finding-dag` | `diagnosedDisease.md` |
| known allergies as an input | `finding-dag` | `patientAllergies.md` |
| family history as an input | `finding-dag` | `patientFamilyHistory.md` |
| the self-assessment prose | `finding-dag` | `patientAssessment.md` |
| free-text notes written ahead of a visit | `finding-dag` | `pursuedNotes.md` |
| the studies or questions being pursued | `finding-dag` | `pursuedStudy.md` |
| starred items, areas of query | `finding-dag` | `pinnedQueries.md` |
<!-- END ALIASES -->

### What may be read, and how a hit may be quoted

`.retrieval/config` declares `quote = line`: a matched line may be returned as it stands, not
reduced to its heading. The reason is that a line here is usually the rule itself —
`ARCHITECTURE.md` states its frontmatter keys and lint rules one per line, and a node's
`## Reasoning` block is a sequence of prohibitions where the heading says only "Reasoning" and the
line says what is actually forbidden. A reader handed the heading alone would have to take the rule
on trust, which is the thing the rule is written down to avoid.

There is no exclusion list, and that is a declaration rather than an omission. This repository is
public by design and holds no app code, no credential and no person's record — which, as
[`README.md`](README.md) says, is what lets it be shared with anyone invited to review it. A value
appearing inside a node is an example written to show what a rationale has to name, not a reading
taken from anybody.

## Known gaps — what this layer does not route

- **Fifteen source nodes appear in no heading projection at all**, because a source node is its
  frontmatter plus a one-line basis and carries no `##` heading for the generator to find. The alias
  table above routes them by name and the third command above finds them by label or by what reads
  them; [`HEADINGS.md`](HEADINGS.md) will never list them, and that is a property of the content
  rather than a staleness.
- **It routes documents, not the graph.** Which node feeds which is in the frontmatter and in each
  node's `## Inputs` links, and the picture of it is `docs/graph-view.svg`, regenerated by
  `scripts/gen-graph-view.py`. A question about the *shape* of the graph is answered from those,
  not from this table.
- **The two forge forms are deliberately unrouted** — `.github/PULL_REQUEST_TEMPLATE.md` and
  `.github/ISSUE_TEMPLATE/content-concern.md` are instructions for opening something on GitHub, not
  documents that answer a question about the content.
- **It says nothing about the application that reads this graph.** That is a private repository with
  its own documentation, and the sync direction — it reads from its own checkout, never from here —
  is `README.md`'s to state.
- **A second brain added as a sibling folder is out of scope until this layer is regenerated.**
  `scope` is `[!.]*.md`, so a new folder's notes are in the corpus the moment they are tracked, but
  the alias table is hand-written and will route none of them. `CONTRIBUTING.md § Adding a brain`
  is where that checklist lives, and a row there for this file is the fix.
