# Contributing user stories and use cases

Start with a need, not a preferred architecture. Contributions from participants, facilitators, community organizers, researchers, and builders are welcome.

- A **user story** briefly describes who needs to do what and why. Use the [user-story form](https://github.com/dds-wg/dds/issues/new?template=user-story.yml).
- A **use case** describes a concrete situation around a need: who is involved, what happens, the relevant conditions, and what success or failure means. Use the [use-case form](https://github.com/dds-wg/dds/issues/new?template=use-case.yml).

Either can come first. You do not need to write a user story before submitting a use case. Multiple cases may explore the same story under different conditions, and one case may relate to several stories. Shared possible solutions do not make distinct needs identical.

Only the first question in either form is required. A rough paragraph is enough to start; we can refine the rest together. Say whether your example is observed, reported by users, or hypothetical. Do not treat a hypothetical example as evidence of real-world demand.

**The format is not important.** A short message, rough notes, a sketch, or an existing public document can all help. Put everything in the first box if that is easiest, or share it through another community channel. There is no need to rewrite material to match the prompts, and missing details should invite follow-up questions rather than block a contribution. The priority is to gather as many needs, experiences, and useful details as possible; we can structure them together later.

## Six prompts for a use case

1. **Situation and goal:** what is the problem, who needs an outcome, and why does it matter?
2. **People and starting conditions:** who is involved or affected, what is already true, and what starts the scenario?
3. **Steps:** what happens from the starting event to the outcome? A short narrative or numbered list is enough.
4. **Conditions and success:** what is required, optional, or prohibited in this case, and how could someone check the outcome?
5. **Variations and risks:** what could differ, fail, or be misused? What must never happen, including when the goal cannot be achieved?
6. **Connections and questions:** which stories, cases, public examples, or unresolved questions help explain it?

Describe roles and intentions rather than screen layouts or implementation details. If a process already depends on a particular technology or rule, identify it as an existing constraint and explain why it matters. Separate that from proposing a technology for DDS to adopt.

For requirements, distinguish **required**, **optional**, **prohibited**, and **unknown** where useful. An unanswered field does not mean that a capability is permitted or that a risk is absent. Requirements apply to the described case, not automatically to every deliberative process.

## Worked example: continue an anonymous workshop in another tool

This is a hypothetical illustration, not an adopted DDS requirement or a claim that any product supports it. It develops one possible context for [the provider-change user story](https://github.com/dds-wg/dds/issues/22).

### 1. Situation and goal

A neighborhood workshop has collected anonymous proposals and reactions. The organizer wants to continue the same process in another tool without asking people to submit everything again or exposing who wrote what.

### 2. People and starting conditions

The organizer coordinates the move, participants contribute, and the old and new services handle the process information. The original participation terms allow this transfer while requiring contributions to remain anonymous. The old service is available. The scenario starts when the organizer requests the move.

### 3. Steps

1. The organizer identifies the process and information needed to continue it.
2. The receiving service checks which contributions, relationships, and process rules it can preserve.
3. The organizer reviews any incompatibilities before authorizing the move.
4. If the essential conditions can be met, participants continue in the new tool with the earlier proposals and reactions available.

### 4. Conditions and success

- **Required:** proposals, reactions, and the relationships between them remain usable. The organizer can compare the transferred material with the source.
- **Required:** the process's anonymity and access rules remain in force after the move.
- **Prohibited:** adding identifying or linkable information that breaks the anonymity promised in this process.
- **Optional:** copying nonessential visual presentation settings.
- **Unknown:** whether participants need to edit their own earlier contributions after the move. This needs clarification before that capability can be assumed.

### 5. Variations and risks

The receiving tool may not support an essential rule. In that case the move must pause rather than silently weaken protection. A bridge might import identifying metadata that was not visible in the original interface. Review must consider the transferred information, not just what appears on screen. If the transfer fails, the original process should remain available in this example, and the organizer should know that the move did not complete.

These are constraints to investigate, not a claim that anonymization or safe transfer is technically solved. Recovery when the old provider is already unavailable is a different case.

### 6. Connections and questions

Related story: [continue a deliberation after changing providers](https://github.com/dds-wg/dds/issues/22). What information is necessary to continue this particular workshop? Who can authorize the transfer? How can participants understand the move? No particular transport, identity scheme, or ontology is prescribed by this example.

## Other ways to contribute

If GitHub is not convenient, share a description in the [DDS Matrix room](https://matrix.to/#/#dds-wg:matrix.org), send it to the [public DDS mailing list](mailto:public-dds@w3.org), or bring it to an [open call](https://www.w3.org/groups/cg/dds/calendar/). Ask for help turning it into a GitHub entry if useful. The prompts above work in any of these channels; using the form is not a condition of participation.

These are public community channels, and mailing-list messages are permanently archived. Use roles rather than personal identities where possible. Do not include private contact details, identifiable participant datasets, sensitive disclosures, or restricted access links. Public submission is not permission to disclose someone else's information.

## How the collection will be used

The immediate priority is to gather needs broadly, not perfect the template or finish documenting every case. Collection and clarification can continue as the work progresses.

As contributions accumulate, we can identify scope, shared capabilities, and conflicting assumptions, then use those requirements to inform a layered system-design proposal. Keep links from proposed building blocks back to the stories and cases that motivate them, including their risks and constraints. Community review and revision of that proposal can then guide focused subgroup and implementation work. This is a proposed sequence, not an adopted architecture or an allocation of work.

A lightweight requirements matrix may become useful as cases accumulate; contributors do not need to prepare one. Submitting a case does not mean DDS has adopted its requirements, endorsed a solution, or committed to implement it. A template, matrix, or polished specification is not a prerequisite for sharing a need.

A longer-term aim is to recommend suitable implementation patterns and make it easier to assess whether an implementation follows the DDS recommendations relevant to its use case. Explicit process properties, capabilities, constraints, and trade-offs can help communities judge whether a tool fits their needs, understand where it differs from the recommendations, and help builders choose approaches. Over time, reference implementations, SDKs, or an agent skill could help people apply these recommendations and check whether an implementation follows them.

## Sources and design rationale

This DDS form was prepared as follow-up to the November 5, 2026 plenary. It is a lightweight synthesis, not a universal W3C template or a W3C Recommendation. The wording and illustrative example are written for DDS rather than copied from these sources.

The following models were reviewed on November 11, 2026:

- [W3C Linked Web Storage use-case template](https://github.com/w3c/lws-ucs/blob/main/.github/ISSUE_TEMPLATE/use-case.md): actors, preconditions, trigger, scenario, alternatives, errors, and acceptance criteria. DDS combines these into everyday-language prompts rather than requiring a long specification.
- [W3C Web of Things use-case template](https://github.com/w3c/wot-usecases/blob/main/CONTRIBUTIONS/use-case-template.md) and [issue form](https://github.com/w3c/wot-usecases/blob/main/.github/ISSUE_TEMPLATE/use-case-template.yml): motivation, context, variants, security, privacy, accessibility, and internationalization. DDS keeps relevant constraints but omits mandatory contact information, taxonomy, and specification-gap analysis.
- [W3C Credentials Community Group education use-case template](https://github.com/w3c-ccg/vc-ed-use-cases/blob/main/.github/ISSUE_TEMPLATE/use-case-template.md): a connection to the user story, data concepts, restrictions, and incomplete contributions welcome. DDS makes related stories optional and does not require domain-specific tags or a chosen standard.
- [Alistair Cockburn, Basic Use Case Template, TR.96.03a, 1998](https://cis.bentley.edu/lwaguespack/CS360_Site/Downloads_files/Use%20Case%20Template%20%28Cockburn%29.pdf): goal in context, actors, trigger, success and failure conditions, main scenario, extensions, and progressive refinement. DDS invites a short initial contribution, with detail added over several passes, and omits scheduling and project-management fields.
- [Washingtonwei, Practical Style Guide and Templates for Writing Effective Use Cases](https://github.com/Washingtonwei/use-case-style-guide): clear goals and actor actions, assumptions, business rules, and alternative paths. DDS keeps steps readable without imposing the full specification format or interface-oriented examples.

The [W3C DID use-case requirements matrix](https://www.w3.org/TR/did-use-cases/#requirements), shared during the call, informs possible later comparison of cases. It is not a submission form. Explicit prompts for prohibited combinations, misuse, and safeguards reflect the DDS call's discussion of negative requirements and unhappy paths.
