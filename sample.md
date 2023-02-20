# <Project Title>

:author: Daniel Lindsley <daniel@toastdriven.com>
:created: 2023/02/20

## Summary

A paragraph that describes the rest of the lightweight spec in simple,
general terms. Should be consumable by non-technical users who are familiar
with the processes/logic involved (e.g. project managers, biz folks, maybe
designers).


## Problem

A couple paragraphs describing the existing situation. Talk about the impetus
behind the project, the current shortfalls/issues. Talk about your target
user(s) needs a bit.


## Solution

Again, a couple paragraphs about the solution. Go into more depth than the
summary, and ensure that everything you brought up in the problem section is
addressed here. Mostly avoid jargon, as this needs to be understandable to
non-technical folks.


## High-Level Implementation

Here's where you begin describing the solution to other technical folks (e.g.
fellow programmers, designers, contractors, etc.). No code here yet, but
describe the things to be implemented in detail. Jargon or code *references*
(model names, classes, service names, etc.) are OK, but use sentences here &
try to be complete without necessarily being **exhaustive**.

This tends to be the largest chunk of text in the document. Use it to expose
misunderstandings in the process, data flows, or the changes to be made.

This should be enough that you could hand the document off to someone doing
code review & have them be able to understand the purpose behind your changes.
Or that you can hand it off to another senior engineer for implementation.


## Data Models

Highlight all of the data model changes. A bulleted list-of-lists here, where
the top-level are the classes/tables changing, and the sublists talk about
field-level changes.


## Code Changes

Highlight the important, the complex, or the "high-traffic" files needing
changes. Especially useful for areas you're less familiar/less confident in.
This can help expose where potential file conflicts may occur, or organizational
decisions up-front. Kill this paragraph in favor of the list, unless you need
to talk about something broadly.

### Additions

* `path/to/file.py`: Quick description of rationale.

### Changes

* `path/to/another/thing.js`: What's being touched & why.


## Testing

Talk about the testing approach. Mention testing strategy or strategies
(automated vs. manual, integration vs. unit, who owns the testing/acceptance).
Doesn't have to be exhaustive (like everything else), but should be clear. This
is your chance to plan.


## Migration

Optional, but if needed, talk about what needs to be done to put the change
into production. Are there things that need to be taken offline/made read-only?
What needs to be automated as part of the overall change to make this go? What
needs to happen for a rollback?


## Outstanding Questions

A big-old bulleted checklist of things you don't know or are unsure of. This is
a chance for peers to give immediate input, or to guide future meetings.

* [x] Have we confirmed everything that's needed for migration?
  * Yes, no changes & ops confirms this can be done without taking anything
    down.
* [ ] Is this all the JS changes necessary for the frontend?
  * Perhaps there's a hidden segment in the middleware?
  * More notes here?
* [ ] Who owns the acceptance testing? Product team?
