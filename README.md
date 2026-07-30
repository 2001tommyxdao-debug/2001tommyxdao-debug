## Tommy Dao

Business Systems Analyst II at Origami Risk. Four years building configuration, reporting and internal tooling for insurance clients, most of it in the gap between what a customer asks for and what the system can actually be made to do.

I am an analyst who builds. Not a software engineer, and the distinction is the point: I spend my day in requirements, data models and client calls, and I write the code when the thing that would solve the problem does not exist yet.

**What I care about right now:** making AI systems provably safe to hand to a non-technical user. Refusal behaviour, tenant isolation, and evaluation that fails loudly instead of degrading into plausible filler.

### Start here

**[rag-eval-harness](https://github.com/2001tommyxdao-debug/rag-eval-harness)** is the repo I would want you to read. A severity-tiered eval harness for multi-tenant RAG, where correctness is tested last and a cross-tenant leak is a P0 that blocks the release. Runs in two commands with no API key.

It exists because I built the internal version at work and cannot show you that one, so I rebuilt the architecture on original content. Clone it and run the failing case yourself.

The bug it caught that I could not have caught by hand: a query returned section 3.1 instead of 3.4, because the search term appeared once in passing earlier in the document and the matcher took first hit instead of best hit. It surfaced as WRONG-SECTION rather than a silent pass. Fixed by ranking on term-occurrence density. A spot check would have missed it, because the wrong section still read plausibly.

### Other builds

- **[checkpoint](https://github.com/2001tommyxdao-debug/checkpoint)** - planning tools that turn a short brief into a calendar. The governing rule is that it never states a number it has not verified, which cost more features than it saved.
- **[leadharvest](https://github.com/2001tommyxdao-debug/leadharvest)** - prospecting tool with an AI audit pipeline, a two-tier scoring gate, and an outreach queue built on FOR UPDATE SKIP LOCKED so a cron tick and a manual click cannot send the same cold email twice.
- **[award-atlas](https://github.com/2001tommyxdao-debug/award-atlas)** - an interactive globe of airline and hotel award pricing. One HTML file, no build step, works offline.

All four are personal projects, built outside of work, on my own time and my own data.

B.S. Business, Management Information Systems, University of Minnesota Carlson School. Minneapolis, Central time.
