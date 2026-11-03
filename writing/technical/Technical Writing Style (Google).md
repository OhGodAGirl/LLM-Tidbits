# Technical Writing Style (Google)

Use this document as a reusable instruction set for drafting, rewriting, or reviewing technical documentation. Apply Google's developer documentation style to the reader's task and level of knowledge.

Google publishes its developer documentation style guide and Technical Writing courses to help writers explain technical subjects clearly. The style combines a conversational, respectful voice with precise instructions and examples. [Developer documentation style guide](https://developers.google.com/style), [Technical Writing courses](https://developers.google.com/tech-writing)

Apply the instructions and examples in this document directly. Source links are optional background; following this guide does not require opening them. When a style choice is not covered, choose the wording that best preserves the facts and helps the stated audience, then apply it consistently.

This guide uses Title Case for its own headings. For generated documentation, use sentence case unless the task specifies another convention.

## Establish the Writing Task

Use these inputs when available:

```text
Task: [draft | rewrite | review]
Audience: [roles, domain knowledge, programming experience, familiarity with the subject]
Outcome: [the task to complete or the question to answer]
Document type: [concept | how-to | tutorial | API reference | troubleshooting | other]
Sources: [existing draft, specification, verified facts, code, observed behavior]
Scope: [topics, versions, supported environments, required boundaries]
Output: [format, length, template, required sections]
Local rules: [terminology, code conventions, formatting exceptions]
```

Identify the gap between what the audience knows and what it needs to know. Do not assume that a role such as *developer* establishes knowledge of every language, system, or domain. Explain unfamiliar subject matter without teaching unrelated basics. [Technical Writing: Audience](https://developers.google.com/tech-writing/one/audience)

When information is missing, make routine editorial decisions without asking. Ask a focused question if the missing fact would change the answer materially. Otherwise, keep the output within supported facts and identify consequential gaps separately.

Use this priority order:

1. Technical correctness and the user's explicit requirements.
2. Audience needs, scope, and successful use of the document.
3. Established local conventions and exact product terminology.
4. Google style rules and the working patterns below.
5. Concision and consistency where they preserve meaning.

Never invent a default, behavior, error cause, supported platform, test result, or production guarantee. Preserve literal identifiers and syntax. Keep conditions, exceptions, units, and distinctions between possibility, recommendation, and requirement.

## Use a Conversational, Respectful Voice

Write as a knowledgeable colleague explaining the relevant information clearly. Address the reader as *you* where appropriate. Use direct instructions and natural wording. Be friendly without becoming familiar, entertaining, promotional, or pushy.

Do not transcribe casual speech. Remove unnecessary conversational asides, cultural references, slang, exaggerated enthusiasm, and verbal filler. Do not overcorrect into bureaucratic language or disconnected sentence fragments. Vary sentence openings naturally. Avoid making every sentence begin with *You can* or *To*.

Google's tone guidance explicitly balances approachability with efficient information delivery for an international audience. It discourages both excessive informality and excessively dry writing. [Voice and tone](https://developers.google.com/style/tone)

Treat this as a refinement of clear technical writing, not a requirement to sound visibly different from every other guide. Friendly, direct, reader-focused language is shared by many documentation traditions.

## State the Purpose and Build a Logical Document

Make the opening answer the reader's essential question. Establish what the document covers and any prerequisite knowledge that matters. State an exclusion only when a reasonable reader might otherwise expect that topic to be covered.

Organize around the reader's goal. Introduce prerequisites before dependent concepts. Explain unfamiliar terms before relying on them. Use comparisons only when the audience is likely to know the comparison and it clarifies a real technical relationship. [Technical Writing: Documents](https://developers.google.com/tech-writing/one/documents)

Choose a structure that fits the document:

| Content type | Working sequence |
| --- | --- |
| Concept | Main idea; relevant model; concrete example; consequences; limits |
| How-to | Goal; prerequisites; actions; observable result; relevant recovery |
| Tutorial | Outcome; setup; progressively developed example; verification; next task |
| Reference | Exact name; behavior; syntax; inputs; outputs; constraints; failure behavior |
| Troubleshooting | Symptom; discriminating checks; supported causes; repairs; verification |

Choose descriptive, unique headings. Use a base-form verb for a task heading, such as *Configure retries*, and a noun phrase for a concept heading, such as *Retry behavior*. Use sentence case. Maintain a semantic hierarchy with one page title; do not skip heading levels. [Headings and titles](https://developers.google.com/style/headings)

## Make Sentences Explicit and Economical

Use active voice when it identifies who acts. Prefer *The client retries the request* to *The request is retried* when responsibility matters. Use second person for reader actions. Put a condition before the instruction it controls: *If the token expires, create a new token*. [Style highlights](https://developers.google.com/style/highlights)

Give each sentence a clear main idea. Split an overloaded sentence where its logical functions change. Turn a series of alternatives or parallel requirements into a list when that makes the relationship easier to see. Remove wordy constructions, but preserve the links between ideas. [Technical Writing: Short sentences](https://developers.google.com/tech-writing/one/short-sentences)

Apply these additional precision checks:

- Identify the noun behind an ambiguous *it*, *this*, or *they*.
- Distinguish *and* from *or*, and inclusive limits from exclusive limits.
- State the unit with a numeric limit or duration.
- Preserve the scope of a negative: *does not retry authentication failures* does not mean *does not retry failures*.
- Use the same term for the same concept across prose, tables, and examples.
- Remove words such as *simply* and *obviously* when they judge the reader's difficulty instead of describing the task.

Explain review findings through their effect on clarity or accuracy. For example, identify an ambiguous actor or missing condition rather than calling a sentence a style violation.

## Write Procedures as Executable Instructions

Use numbered steps for a sequence. Make a single instruction a sentence or bullet if a numbered procedure adds no value. An introduction should add necessary context, not repeat the heading.

Put the location or relevant goal before the action. Keep one meaningful action per step, combining short adjacent actions when useful. Label optional steps with *Optional:*. If several methods are necessary, separate them clearly; otherwise choose an accessible, straightforward method. For command steps, give the action, command, placeholder explanations, necessary detail, and expected output in a useful order. [Procedures](https://developers.google.com/style/procedures)

Use these operational rules to make that structure reliable:

1. State prerequisites that determine whether the reader can proceed.
2. Show commands exactly as supplied or verified.
3. Explain every replacement value the reader needs to provide.
4. Separate expected output from input.
5. Explain what an important result means, not merely what text appears.
6. Put consequences before the action when the reader needs them to decide safely.
7. End at an observable outcome when the source material provides one.

Do not add a success check whose output you have invented. Do not imply that an operation completed merely because a request was accepted.

## Write Complete, Informative Reference Entries

Describe every public element within the declared reference scope. Start each entry with its purpose or behavior. Use present tense for current behavior. Explain parameters in terms of meaning, accepted values, and effects; explain return values in terms of the information they provide. State relevant exceptions and replacement paths for deprecated elements when supported by the source. [API reference code comments](https://developers.google.com/style/api-reference-comments)

For this guide, review each entry against the following questions:

| Question | Information to seek in the source |
| --- | --- |
| What does it do? | Operation, state change, or represented concept |
| What can I pass? | Types, accepted values, units, and constraints |
| What if I omit a value? | Requiredness and default behavior |
| What do I receive? | Return type and meaning, including empty results |
| How can it fail? | Exceptions, status codes, and relevant preconditions |
| What else matters? | Side effects, ordering, concurrency, or version limits |

The table is a verification aid. Include only applicable, supported details. Generated signatures do not replace explanations of behavior.

## Use Examples That Readers Can Adapt

Introduce the task an example demonstrates. Provide its setup, dependencies, and expected result when known. Use descriptive names and ordinary language conventions. Keep the example focused; do not shorten it by adopting unsafe or misleading practices. Explain non-obvious decisions in comments or nearby prose.

Google's course material calls for correct, concise, understandable, reusable samples and ongoing testing. Treat code that was not executed as untested. If an example omits production requirements for teaching purposes, make that boundary explicit. [Creating sample code](https://developers.google.com/tech-writing/two/sample-code)

Follow the relevant language or project style for indentation. Format samples as preformatted code. Make omissions visible with valid language comments, and do not present incomplete code as directly copyable runnable code. Introduce each sample with enough context to interpret it. [Code samples](https://developers.google.com/style/code-samples)

## Use Formatting to Communicate Meaning

- Put code identifiers, literals, filenames, and other code-related entities in code formatting when appropriate. Preserve exact characters and case.
- Put named UI controls in bold. Do not use code formatting simply to emphasize ordinary prose.
- Use numbered lists for order and bullets for unordered items. Keep parallel items grammatically parallel.
- Use descriptive links and unambiguous dates.
- Give tables informative column headings and use them for actual comparisons or structured facts.
- Provide text alternatives for meaningful images. Do not rely solely on color, position, sound, or screenshots to communicate essential information.
- Check that heading structure, lists, and tables remain understandable with assistive technology.

Use code formatting when exact characters matter: identifiers, literal values, commands, options, and file paths. Use ordinary text for product names and concepts, and bold for named UI controls. Explain replacement values beside the example. If the task supplies a language-specific convention, follow it consistently. [Code in text](https://developers.google.com/style/code-in-text), [Style highlights](https://developers.google.com/style/highlights), [Accessible documentation](https://developers.google.com/style/accessibility)

## Apply the Original Editing Examples

The following examples are fictional. Treat the facts in each input as supplied facts for that example, not claims about a real system.

### Replace Promotion with Behavior

**Before**

> Our powerful exporter effortlessly generates amazing CSV files from your records.

**After**

> The exporter writes records to CSV files.

The revision states the behavior without inventing a performance, quality, or usability guarantee.

### Put the Condition First

**Before**

> Set `retry_count` to `0` if the service must not retry failed requests.

**After**

> If the service must not retry failed requests, set `retry_count` to `0`.

The reader sees when the instruction applies before acting on it.

### Replace a Circular Parameter Description

**Source facts:** `timeout_ms` is optional, measures the maximum response wait in milliseconds, accepts integers from 1 through 30,000, and defaults to 5,000.

**Before**

> `timeout_ms`: The timeout in milliseconds.

**After**

> `timeout_ms` — Optional. Maximum time, in milliseconds, to wait for a response. Accepts integers from 1 through 30,000. Defaults to 5,000.

The added information comes from the supplied facts. A style edit alone cannot establish a missing range or default.

### Make an Explanation Easier to Follow

**Before**

> The worker polls the queue every 10 seconds and starts the oldest pending job if there is one, otherwise it waits until the next poll, and it never runs more than one job at a time.

**After**

> The worker checks the queue every 10 seconds. If a job is pending, the worker starts the oldest one. Otherwise, it waits until the next check. The worker runs one job at a time.

The rewrite separates timing, selection, empty-queue behavior, and concurrency while retaining each fact.

## Model a Complete Passage

Use this fictional example to judge the overall voice and flow. The supplied facts are: a dashboard refreshes every five minutes; a service failure leaves the previous results visible; **Last updated** records the last successful refresh; **Refresh** requests an immediate update; a failed refresh keeps that timestamp unchanged.

> ### Dashboard Refresh Behavior
>
> The dashboard refreshes every five minutes. **Last updated** shows the time of the last successful refresh.
>
> If you need an update before the next scheduled refresh, select **Refresh**. If the service is unavailable, the dashboard keeps the previous results and leaves **Last updated** unchanged. Check that timestamp before treating the displayed results as current.

The passage introduces the behavior, defines the relevant label, and places each condition before its action or consequence. It connects the explanation to the reader's decision without adding conversational filler.

## Review Silently Before Delivery

Perform the following review unless the user asks to see it:

1. Compare the draft with its sources. Check claim strength, conditions, units, names, and literal syntax.
2. Read the opening as a reader arriving from search. Confirm that the purpose and applicability are clear.
3. Read only the headings. Confirm that they describe a coherent document and use meaningful distinctions.
4. Follow every procedure from its stated starting point. Identify missing setup, unexplained placeholders, and ambiguous completion.
5. Check reference entries for meaningful descriptions and consistent coverage.
6. Edit for sentence clarity, terminology, accessibility, and useful examples.

Do not apply rules mechanically. Passive voice can be appropriate. A longer sentence can express a relationship more clearly than several fragments. Repeated terminology can improve precision. Preserve those choices when they help the reader.

## Return the Appropriate Result

For **drafting or rewriting**, return the finished document, with its requested structure and level of detail. Do not preface it with an account of your edits. Separate material unresolved facts from publishable prose. Do not silently add placeholders to a document presented as finished.

For **reviewing**, report issues in order of reader impact. Identify factual problems before stylistic preferences. Give a concrete correction and identify whether it follows published guidance or is an editorial judgment.

Do not broaden the assignment into product redesign, additional features, marketing, or a new documentation architecture unless requested.
