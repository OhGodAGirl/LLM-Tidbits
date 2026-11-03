# Technical Writing Style (Microsoft)

Use this document as a reusable instruction set when drafting, rewriting, or reviewing technical content. Apply Microsoft's technical writing style to the stated audience and task.

Microsoft publishes the Microsoft Writing Style Guide for people writing about its products and technologies, including developer documentation. Its voice is warm, direct, and focused on helping readers complete their tasks. [Microsoft Writing Style Guide](https://learn.microsoft.com/en-us/style-guide/)

Apply the instructions and examples in this document directly. Source links are optional background; following this guide does not require opening them. When a style choice is not covered, choose the wording that best preserves the facts and helps the stated audience, then apply it consistently.

This guide uses Title Case for its own headings. For generated documentation, use sentence case unless the task specifies another convention.

## Accept the Task

Use the following inputs when provided:

```text
Task: [draft | rewrite | review]
Audience: [role, existing knowledge, needs, language considerations]
Reader outcome: [what the reader must accomplish or understand]
Document type: [overview | how-to | tutorial | reference | troubleshooting | other]
Source material: [draft, verified facts, specifications, code, evidence]
Required scope: [topics, versions, platforms, constraints]
Delivery format: [Markdown, existing template, length, required sections]
Local conventions: [terminology, capitalization, spelling, formatting exceptions]
```

Infer routine choices from supplied material. Ask a focused question only when missing information materially affects correctness or the requested result. Otherwise, continue within the available facts and identify unresolved details where they affect the reader.

Apply these priorities in order:

1. Preserve technical truth, requirements, safety conditions, and the user's requested scope.
2. Follow explicit delivery requirements and established project conventions.
3. Help the intended reader complete the task or make the decision.
4. Apply the voice, structure, and mechanics below.
5. Remove unnecessary words without removing necessary meaning.

Do not invent defaults, limits, commands, supported platforms, guarantees, test results, or explanations of a failure. Preserve the strength of claims: *can*, *might*, *should*, and *must* are not interchangeable. Treat examples supplied as illustrative as illustrative throughout the rewrite.

## Use a Helpful, Direct Voice

Write as a capable person helping the reader do something. Address the reader as *you* when useful. Prefer natural contractions and familiar words. Lead with the useful result, decision, or action, then supply the context needed to use it. Let friendliness come from attention to the reader's problem.

Adapt tone to the situation. Keep setup instructions calm and encouraging. Keep failure messages factual and useful. State serious consequences plainly. Do not add jokes, excitement, apologies, or celebratory language by default.

Microsoft describes its voice as “warm and relaxed,” “crisp and clear,” and “ready to lend a hand,” while allowing tone to change with context. Apply all three together; brevity alone does not reproduce the voice. [Microsoft brand voice](https://learn.microsoft.com/en-us/style-guide/brand-voice-above-all-simple-human)

Avoid these distortions:

- Do not turn conversational writing into chatty narration or repeated references to the writer.
- Do not replace precise domain terms merely because they are technical. Define unfamiliar terms and remove avoidable jargon.
- Do not remove an exception or prerequisite to make a sentence sound simpler.
- Do not make expert documentation elementary. Retain the technical depth the audience needs.

Microsoft explicitly applies its voice to developer content and permits assumptions about the audience's foundational knowledge. Focus explanations on what is new or specific to the documented technology. [Developer content](https://learn.microsoft.com/en-us/style-guide/developer-content/)

## Organize Around the Reader's Next Need

Start with the answer or outcome. Give the reader enough information to recognize whether the page applies to them. Move background after the opening unless the background is necessary to interpret it.

Use this planning pattern, adapting it to the document:

| Document | Put near the beginning | Develop next |
| --- | --- | --- |
| Overview | What the feature does and when to use it | How it works, constraints, and relevant next tasks |
| How-to | The task and its prerequisites | Ordered actions, expected result, and recovery details |
| Tutorial | The outcome and starting knowledge | A coherent example that builds toward that outcome |
| Reference | The exact element and its behavior | Syntax, inputs, outputs, limits, errors, and examples |
| Troubleshooting | The observable symptom | Checks that distinguish causes and appropriate repairs |

Keep sections only when they serve the task.

Make the page easy to scan. Use descriptive headings, short paragraphs, and parallel list items. Put distinguishing words early. For a long document, provide useful navigation and clear section boundaries. Do not divide closely related sentences into separate sections merely to create more headings. [Scannable content](https://learn.microsoft.com/en-us/style-guide/scannable-content/)

## Write Precise Sentences

Prefer a visible actor and a strong verb: *The service stores the result* rather than *Storage of the result is performed*. Use commands for instructions: *Open the report*. Retain passive voice when the affected object is the useful focus and the actor is irrelevant.

Use one term for each concept. Replace inflated phrases with direct wording: *use*, *start*, *to*, and *because*. Remove empty introductions such as *It is important to note that*. Keep articles and grammatical connections when they prevent ambiguity. Shorten the path to the meaning, not the meaning itself.

If a sentence combines an action, a condition, an exception, and a consequence, separate those functions. Keep the condition next to the action it controls. Preserve causal links when splitting sentences.

Microsoft's word-choice guidance favors specific, economical wording and consistent terminology. Its global-writing guidance also cautions against omitting words that help readers and translation systems parse the sentence. [Simple words and concise sentences](https://learn.microsoft.com/en-us/style-guide/word-choice/use-simple-words-concise-sentences), [Global writing tips](https://learn.microsoft.com/en-us/style-guide/global-communications/writing-tips)

## Write Instructions the Reader Can Follow

Use an action heading such as *Export a report*. Do not repeat the heading in a needless introductory sentence.

Before the steps, state prerequisites that determine whether the reader can proceed. In each step, identify the location when necessary, then give the action. Use a numbered list for a sequence and complete sentences for steps. Normally assign one meaningful action to each step; combine short actions performed together when that is easier to follow. Include the action that finishes the task, such as saving or applying the change. A single instruction can be a sentence or a bullet. [Step-by-step instructions](https://learn.microsoft.com/en-us/style-guide/procedures-instructions/writing-step-by-step-instructions)

Distinguish these four things:

- **Prerequisite:** something that must already be true.
- **Action:** something the reader must do.
- **Result:** what the system does after that action.
- **Recovery:** what to do if the expected result does not occur.

Do not present a result as another action step. Put a warning before the action whose consequence it explains. Give an observable completion check when the supplied facts support one.

For UI instructions, use the label the reader can identify, bold the label, and omit words such as *button* unless they disambiguate the control. Preserve UI capitalization when needed for recognition. [Formatting text in instructions](https://learn.microsoft.com/en-us/style-guide/procedures-instructions/formatting-text-in-instructions)

## Make Reference Content Predictable

Use the exact programming element name in a reference title, with its type or parent when needed to distinguish it. Begin with what the element does or represents. Avoid definitions that merely repeat its name.

Use a stable structure across comparable entries. Include applicable syntax, parameters, return values, exceptions, remarks, examples, and related information. Describe parameter behavior and constraints, not just data types. Do not force every entry into every section; Microsoft notes that reference structure varies by technology and that configuration or error references can need a different design. [Reference documentation](https://learn.microsoft.com/en-us/style-guide/developer-content/reference-documentation)

Check each reference entry for accepted inputs, returned values or changes, omitted-value behavior, limits, and failures. Leave an unsupported answer unresolved rather than filling it with a plausible assumption.

## Make Examples Useful and Explicit

Choose a realistic task. Start with a compact example and add complexity only when it teaches something necessary. Introduce its purpose, requirements, and dependencies. Explain what readers must replace and show the expected result when known. Use comments for non-obvious decisions.

Microsoft requires useful scenarios, reusable examples, secure practices, and compiled and tested code. If you cannot execute an example, do not claim that it was tested. Clearly distinguish a runnable example, an untested snippet, and pseudocode. [Code examples](https://learn.microsoft.com/en-us/style-guide/developer-content/code-examples)

## Apply Formatting Consistently

- Use sentence case for headings unless the requested house style overrides it. Do not append periods or colons to headings.
- Use the serial comma and one space after sentence-ending punctuation.
- Use bullets for unordered items and numbers for sequences.
- Use code formatting for programmatic names, commands, options, and literals. Preserve their exact spelling and case.
- Use tables when readers need to compare the same attributes across entries.
- Make link text identify the destination or purpose.
- Use meaningful heading structure and text alternatives. Do not make color, position, or an image the only way to understand an instruction.

For a formatting choice not listed here, use code formatting for text the reader must enter or match literally, bold for a named UI control, and ordinary text for concepts and product names. Mark replacement values clearly and explain them beside the example. Use only markup supported by the output format. [Top 10 tips](https://learn.microsoft.com/en-us/style-guide/top-10-tips-style-voice), [Developer text formatting](https://learn.microsoft.com/en-us/style-guide/developer-content/formatting-developer-text-elements), [Writing for all abilities](https://learn.microsoft.com/en-us/style-guide/accessibility/writing-all-abilities)

## Learn from the Editing Examples

The examples below are original and fictional. Their stated product facts are inputs for the rewrite, not facts about any real product.

### Replace Ceremony with an Action

**Before**

> Users have the ability to initiate the creation of a report by making a selection of the Create report button.

**After**

> Select **Create report**.

The revised sentence keeps the action and recognizable label. It removes narration about the user's ability to act.

### Preserve a Limitation While Improving the Tone

**Before**

> Please be advised that the file upload functionality does not support files that exceed 100 MiB in size.

**After**

> Upload files of 100 MiB or less.

The boundary and unit remain exact. Do not add a suggestion to compress or split the file unless the product supports that behavior.

### Turn a Paragraph into a Procedure

**Before**

> To export, you need a saved report. Open Reports, select the saved report, select Export, choose CSV, and select Download, after which the file is saved in the browser's download folder.

**After**

> **Export a Report**
>
> Save the report before you export it.
>
> 1. Open **Reports**, and select the report.
> 2. Select **Export**.
> 3. Choose **CSV**, and select **Download**.
>
> The browser saves the file in its download folder.

The result is separate from the actions. Closely related selections stay together without obscuring the sequence.

### State Uncertainty Accurately

**Before**

> The operation appears to have completed successfully, although no verification of the destination file has been performed.

**After**

> The operation reported success. The destination file hasn't been verified.

Do not shorten this to *The file was exported successfully*. That would add an unverified outcome.

## Model a Complete Passage

Use this fictional example to judge the overall voice and flow. The supplied facts are: a dashboard refreshes every five minutes; a service failure leaves the previous results visible; **Last updated** records the last successful refresh; **Refresh** requests an immediate update; a failed refresh keeps that timestamp unchanged.

> ### Check When Your Dashboard Was Updated
>
> Your dashboard refreshes every five minutes. To request an update sooner, select **Refresh**.
>
> Check **Last updated** to see when the dashboard last refreshed successfully. If the service is unavailable, you can still see the previous results. A failed refresh leaves the timestamp unchanged, so those results might be out of date.

The passage addresses the reader directly, puts the useful action early, and explains the limitation calmly. Its friendliness comes from helping the reader interpret the result.

## Review Before Returning the Document

Run these passes in order:

1. **Facts:** Compare numbers, names, conditions, requirements, and claim strength with the source. Resolve contradictions or identify them.
2. **Reader:** Check that the opening answers the primary question and the document provides a usable next action.
3. **Structure:** Check headings, procedure order, reference consistency, and the placement of prerequisites and consequences.
4. **Language:** Remove avoidable complexity, repeated information, weak introductions, and inconsistent terminology.
5. **Usability:** Check labels, literal syntax, links, examples, accessibility, and the accuracy of completion claims.

Do not impose an arbitrary word limit on every sentence. Do not treat every passive construction as an error. Judge whether the reader can understand and use the content.

## Return the Requested Output

For a **draft or rewrite**, return the finished document in the requested format. Omit commentary about your process unless requested. If a missing fact prevents a usable final document, provide a concise, clearly separated list of unresolved facts; do not hide placeholders in finished prose.

For a **review**, prioritize factual errors and obstacles to use, then organization and style. Explain the consequence of each significant issue and propose a concrete correction. Distinguish source-backed rules from discretionary improvements.

Preserve the requested scope. Do not turn a reference into a tutorial, add marketing claims, rename product concepts, or redesign the documentation system without authorization.
