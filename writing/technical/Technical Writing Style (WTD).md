# Technical Writing Style (WTD)

Use this document as a reusable instruction set for drafting, rewriting, or reviewing technical documentation. Apply the documentation practices described here and, unless the task supplies another voice, use the neutral, friendly tone specified for the Write the Docs website.

Write the Docs is a community whose software documentation guide collects practices from many contributors. It does not prescribe one universal house voice for every organization's documentation. Its website style guide has a narrower scope: writing on its own websites. Keep those two sources of guidance distinct. [Software documentation guide](https://www.writethedocs.org/guide/), [Website style guide](https://www.writethedocs.org/style-guide/)

Apply the instructions and examples in this document directly. Source links are optional background; following this guide does not require opening them. When a style choice is not covered, choose the wording that best preserves the facts and helps the stated audience, then apply it consistently.

This guide uses Title Case for its own headings. For generated documentation, use sentence case unless the task specifies another convention.

## Identify the Reader and the Deliverable

Use these inputs when supplied:

```text
Task: [draft | rewrite | review | plan a documentation set]
Audience: [users, administrators, contributors, developers, or other readers]
Reader need: [the real task, question, difficulty, or decision]
Starting knowledge: [what readers know and what they need explained]
Content type: [overview | tutorial | how-to | reference | troubleshooting | other]
Evidence: [draft, verified behavior, specifications, code, support findings]
Scope: [supported versions, environments, topics, and required boundaries]
Output: [format, template, length, destination requirements]
Local conventions: [terminology, baseline style, known exceptions]
Maintenance context, if relevant: [owner, source of truth, update process]
```

Do not assume that people using a system need the same information as people contributing to it. Determine which reader the document serves. Use a known user problem or task to choose content. Avoid creating a miscellaneous FAQ as a substitute for an organized explanation or task guide. [How to write software documentation](https://www.writethedocs.org/guide/writing/beginners-guide-to-docs/)

Resolve ordinary editorial choices yourself. Ask a focused question only if missing information materially changes the result. Otherwise, keep unsupported details out of the finished prose and identify significant unresolved facts separately.

## Follow the Priority Rules

Apply these priorities in order:

1. Preserve factual accuracy, explicit user requirements, and the requested scope.
2. Help the identified reader understand or complete the intended task.
3. Follow established terminology, templates, and local conventions.
4. Apply the selected voice and documentation practices in this guide.
5. Improve consistency and concision without weakening completeness.

Do not invent defaults, behavior, commands, limits, test results, guarantees, or reasons for a failure. Preserve exact names, syntax, conditions, units, and version applicability. Distinguish documented behavior, observation, inference, and an unresolved question.

When sources conflict, identify the conflict rather than silently choosing the most convenient claim. A polished sentence must not imply stronger evidence than the source provides.

## Use the Selected Voice Deliberately

For this instruction set, use a measured, welcoming voice. Explain the subject without promotional enthusiasm, personal advocacy, or unnecessary commentary about the writer. Present alternatives through their relevant advantages, limitations, and conditions of use.

Do not equate neutral tone with passive voice or emotional distance. Give direct instructions when the reader needs to act. Address the reader naturally. Avoid language that treats a difficulty as a personal failure.

The Write the Docs website guide calls for neutral, friendly, inclusive writing, limited jargon, defined abbreviations, and sentence-case headings. It also discourages presenting personal preferences as rules or promoting a particular tool. These are website conventions adopted here by choice, not requirements imposed on every community member's documentation. [Website style guide](https://www.writethedocs.org/style-guide/)

Use an established domain term when it improves precision. Explain it at the point where an unfamiliar reader needs it. Do not define widely understood terms merely to make the document look comprehensive.

## Apply the Community Practices

Use these as goals for documentation quality:

- Make the content easy to locate, skim, and reference directly.
- Include useful examples without burying reference information in tutorials.
- Keep terminology and structure consistent.
- Keep documentation aligned with supported behavior and versions.
- Cover the declared subject adequately; do not imply that a partial reference is complete.
- Make contributions and feedback possible.
- Keep maintenance close to the relevant development work and avoid competing copies of the same facts.

The principles allow useful repetition in reader-facing material while discouraging duplicated sources that must be maintained independently. Choose repetition when it gives the reader necessary context; use a canonical source or shared content mechanism to control drift. [Documentation principles](https://www.writethedocs.org/guide/writing/docs-principles/)

Apply these principles proportionately. A small task page does not need a new publishing system. An editorial rewrite does not authorize changing repositories, installing tools, or reorganizing a documentation collection.

## Organize Around Questions Readers Actually Have

Before drafting, write a brief internal statement of the page's purpose: *After reading this, the reader can...* or *This page answers...*. Use that statement to exclude unrelated material.

Choose a page structure according to the reader's need:

| Page type | Primary reader need | Useful content sequence |
| --- | --- | --- |
| Overview | Decide whether the subject is relevant | Purpose, use cases, important limits, next steps |
| Tutorial | Learn through a coherent experience | Outcome, setup, guided example, result, reflection |
| How-to | Complete a known task | Prerequisites, actions, verification, relevant recovery |
| Reference | Find an exact fact | Named element, behavior, fields or syntax, constraints |
| Explanation | Understand a model or decision | Central idea, relationships, examples, tradeoffs |
| Troubleshooting | Diagnose and resolve a symptom | Evidence, distinguishing checks, repair, verification |

Choose the dominant purpose of the requested page. Link or briefly explain related material when needed. Do not force all six functions into every document.

If the task concerns a whole documentation set, give each page a clear place and purpose. A shared hierarchy and starter templates can reduce uncertainty for contributors and readers. Do not add a complicated taxonomy merely because the collection has several files. [Building documentation mindshare](https://www.writethedocs.org/guide/writing/mindshare/)

## Make Sentences and Paragraphs Usable

Use these conventions when editing:

- Give each paragraph a clear purpose and put its controlling idea near the start.
- Use a visible actor when the reader needs to know who performs an action.
- Prefer concrete verbs to phrases such as *perform the implementation of*.
- Put a condition near the statement or action it controls.
- Keep an exception attached to the rule it qualifies.
- Replace ambiguous pronouns with the relevant noun.
- Keep logical relationships explicit when splitting a long sentence.
- Use consistent names even when literary variation would sound less repetitive.

Do not turn these conventions into an inflexible sentence formula. A sentence can contain a necessary qualification. A paragraph can explain more than one closely connected detail. Judge whether the reader can reconstruct the intended meaning accurately.

Keep explanations specific. Replace *This approach is better* with the actual criterion, such as *This approach lets contributors propose changes without publishing them immediately*. If the source does not establish that benefit, do not assert it.

## Write a Complete Task Path

When the requested content is procedural, use these working rules:

1. State the outcome and the starting conditions.
2. Identify necessary permissions, inputs, or dependencies from the supplied facts.
3. Present dependent actions in order.
4. Explain replacement values next to the command or field that uses them.
5. Separate a system response from an action the reader performs.
6. State how to recognize success when the evidence supports it.
7. Include the most relevant failure or recovery information without burying the primary path.

Use numbered steps for a sequence and bullets for independent choices. Keep a single action as a sentence when a list adds no value. If the source is incomplete, identify the missing prerequisite or verification detail rather than inventing it.

## Make Reference Material Answer Exact Questions

Use a consistent entry structure appropriate to the subject. For an operation, describe inputs, outputs, side effects, and failure conditions. For a setting, describe its meaning, accepted values, default behavior, and when it takes effect. For an error, describe the observable condition and supported response.

Do not repeat a name as its definition. *Batch size: the batch size* adds no useful information. Do not imply completeness if important entries or supported cases are missing.

Keep extended teaching examples separate when they interrupt lookup. Give short examples at the point where they remove ambiguity.

## Make Examples and Formatting Accessible

Use original examples that demonstrate the reader's likely task. Label fictional values and replacement values clearly. Avoid examples that assume a narrow cultural background or assign stereotyped roles. Consider how word choices and example names may be understood by different readers. [Reducing bias in your writing](https://www.writethedocs.org/guide/writing/reducing-bias/)

Use meaningful headings, readable emphasis, and understandable text alternatives. Keep essential instructions available as text. Do not rely exclusively on a screenshot, color, or visual location. Review the rendered result as well as the source when that capability is available. The community accessibility guide treats content organization and screen-reader compatibility as part of documentation quality. [Accessibility guidelines](https://www.writethedocs.org/guide/writing/accessibility/)

Use code formatting for exact identifiers, commands, options, values, and file paths; bold for named UI controls; and ordinary text for concepts and product names. Explain replacement values beside their examples. Use descriptive link text and tables for structured comparisons. Keep spelling and punctuation consistent, using the serial comma where it prevents ambiguity. Apply any house conventions supplied with the task and record recurring exceptions so comparable pages make the same choices. [Style guides](https://www.writethedocs.org/guide/writing/style-guides/)

## Use Feedback and Maintenance Evidence

When supplied, use support questions to identify unclear terminology, missing prerequisites, and unaddressed failure cases. A repeated question may reveal a missing explanation or a page readers cannot find. Do not assume that a single support report proves a universal product defect. Collaboration between support and documentation can expose everyday use cases and improve review. [Documentation inside a support team](https://www.writethedocs.org/guide/writing/support-team/)

When asked to propose a maintenance workflow, make updates reviewable and connect documentation changes to the behavior they describe. Version control, plain-text sources, review, and automated checks are a documented approach. They are not proof that the content is correct and are not a requirement to impose a particular tool on every team. [Docs as code](https://www.writethedocs.org/guide/docs-as-code/)

For ordinary drafting and rewriting, apply this as a source check: identify which supplied facts could become stale, preserve version qualifications, and avoid creating another authoritative copy of material that already has a maintained home.

## Apply the Original Editing Examples

The following examples are fictional. Treat their supplied facts as inputs for editing, not verified claims about a real system.

### Replace Personal Advocacy with a Decision Criterion

**Source facts:** Both workflows are supported. Review mode requires approval before publication; direct mode publishes immediately.

**Before**

> You should definitely use review mode because it is the best workflow.

**After**

> Use review mode when changes require approval before publication. Direct mode publishes changes immediately.

The revision gives the reader a basis for choosing without inventing a universal preference.

### Replace Blame with Observable Behavior

**Source facts:** The importer requires a `record_id` column and rejects files without it.

**Before**

> If you forgot the required column, the importer won't work properly.

**After**

> The importer rejects files that do not contain a `record_id` column. Add the column before importing the file.

The rewrite names the requirement and action. It does not speculate about why the reader's file lacks the column.

### Make a Reference Entry Informative

**Source facts:** `batch_size` sets records per batch, defaults to 100, accepts integers from 1 through 1,000, and applies to new jobs.

**Before**

> `batch_size`: Sets the batch size.

**After**

> `batch_size` sets the number of records in each batch. It accepts integers from 1 through 1,000 and defaults to 100. Changes apply to new jobs.

The description supplies the information a reader needs to configure the setting and understand when a change takes effect.

### Preserve the Boundary of Available Evidence

**Before**

> The service returned an accepted response, so the migration is finished.

**Source clarification:** Acceptance starts an asynchronous migration; no completion result is available.

**After**

> The service accepted the migration request. Completion has not been confirmed.

Do not invent a status endpoint or a verification command to make the example seem more complete.

## Model a Complete Passage

Use this fictional example to judge the overall voice and flow. The supplied facts are: a dashboard refreshes every five minutes; a service failure leaves the previous results visible; **Last updated** records the last successful refresh; **Refresh** requests an immediate update; a failed refresh keeps that timestamp unchanged.

> ### Understanding the Age of Dashboard Results
>
> Dashboard results reflect the last successful refresh. The dashboard refreshes every five minutes, and **Last updated** records when that refresh succeeded. Selecting **Refresh** requests an immediate update.
>
> When the service is unavailable, the previous results remain visible and the timestamp stays unchanged. These retained results can still be read, but their age should be checked before they are used as current information.

The passage explains the reader's central question before the controls. It uses a neutral voice and keeps the relationship between visible data, its age, and its limitations explicit.

## Review the Document Before Returning It

Use the following review sequence:

1. **Evidence:** Check names, limits, defaults, behavior, versions, and uncertainty against the supplied sources.
2. **Reader need:** Confirm that the opening and page structure answer the actual question or support the intended task.
3. **Completeness:** Follow the task from its stated starting point; inspect reference coverage within the declared scope.
4. **Findability:** Check titles, headings, links, and the relationship to surrounding content when that context is available.
5. **Accessibility and inclusion:** Check text alternatives, semantic structure, unexplained terminology, and assumptions in examples.
6. **Maintenance:** Identify conflicting duplicates or unstable claims when the requested scope permits that review.
7. **Language:** Remove unnecessary words and personal advocacy while preserving precision and a welcoming tone.

Report only checks actually performed. An editorial review does not establish runtime correctness, successful user testing, or complete accessibility compliance.

## Return the Requested Result

For a **draft or rewrite**, return the finished document in the requested format. Keep editorial explanations out of the document unless asked. Identify material unresolved facts separately and briefly.

For a **review**, prioritize factual problems, missing reader information, and usability obstacles before stylistic preferences. Give concrete corrections. Distinguish an official source rule, a local convention, and your own editorial recommendation.

For a **documentation plan**, connect each proposed page or workflow change to a reader need, identify the supplied evidence, and keep unsupported assumptions visible. Do not recommend a tool merely because it is associated with a documentation community.
