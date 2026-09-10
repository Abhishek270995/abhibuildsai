---
title: "I Stopped Writing Every Query Myself — Here's What That Taught Me About Where Analytics Is Headed"
description: "Agentic AI, conversational BI, and automated data prep are changing what 'core analytics' actually means. A practical look at what's shifting, and why beginner analysts especially can't afford to wait to learn it."
pubDate: "Sep 10 2026"
---

A year ago, "AI in analytics" mostly meant a chatbot bolted onto a dashboard — ask it a question, it summarizes a table, everyone moves on with their day.

That phase is over.

The tools I'm working with now don't just answer questions about data. They plan a workflow, pull the numbers, run checks, and hand back something close to a finished analysis. Not something I'd ship without looking at it first — but close enough that it's genuinely changed what I spend my time on day to day.

I don't think that's a small shift. I think it's the biggest change to this job since dashboards replaced static reports, and I wanted to write down what I'm actually seeing — not the vendor-deck version, the working-analyst version.

## What's Actually Different This Time

It's easy to be numb to "AI is changing analytics" as a headline at this point. So here's what's concretely different from even a year ago.

**Writing SQL isn't the moat it used to be.** A stakeholder can describe what they want in plain English and get a workable query back without ever pinging an analyst. That used to be a good chunk of the value an analyst brought to a team on an average week.

**Data cleaning is getting automated in chunks.** Error detection, standardizing formats, flagging weird values — the unglamorous 60–70% of the job that nobody puts on their resume — is increasingly something a tool does first, and a human checks second, rather than the other way around.

**Analysis is starting to run ahead of us instead of waiting for us.** Instead of someone opening a dashboard on Monday and noticing a metric dropped on Thursday, systems are watching continuously and flagging it the moment it happens — fraud detection, demand shifts, operational anomalies, all surfaced in real time instead of at the next scheduled review.

**Single-tool workflows are becoming multi-agent workflows.** One agent handles data quality, another builds the metric, another drafts the narrative — which is honestly just how a good human analytics team already worked, except now it doesn't stop for lunch.

None of this is speculative. It's the direction every major analytics and enterprise-tech report has converged on for this year, and it matches what I'm seeing hands-on with client work.

## So What Does "Core Analytics" Even Mean Now

Here's the part that matters more than any individual tool: none of this makes the analyst role obsolete. Every credible piece of research on this says the same thing — the job isn't disappearing, it's relocating.

It's moving away from *"can you write the query"* toward *"did you ask the right question in the first place."* Away from *"can you build the dashboard"* toward *"can you tell me when the AI-generated number is wrong."* Away from reporting what happened toward explaining why it matters and what to actually do about it.

That second one — catching a confidently wrong AI output before it reaches a decision-maker — might be the single most underrated skill in analytics right now. Nobody teaches it in a course. Most people learn it by getting burned once, presenting a number that looked right and wasn't.

The tools changed. The judgment required to use them well didn't get automated — if anything, it got more valuable, because now it's the only thing standing between a fast answer and a *correct* one.

## Why This Matters More If You're Just Starting Out

I want to be direct about this part, because I think it gets soft-pedaled a lot in career advice: the tasks getting automated first are exactly the tasks that used to be someone's first job. Routine reporting. Basic cleaning. Repetitive dashboard refreshes. That was the on-ramp for a lot of analysts, myself included.

That on-ramp isn't gone. But it's thinner than it used to be, and it's thinning faster than most degree programs and bootcamp curricula are adjusting for. A few things worth sitting with if you're early career:

- Job postings mentioning AI/ML familiarity for analyst roles have roughly doubled year over year.
- Analysts actively using AI tools in their day-to-day work are reporting meaningfully higher effectiveness — and, increasingly, a real pay difference versus peers who aren't.
- Employers aren't saying entry-level roles are vanishing. They're saying entry-level roles are evolving toward AI-assisted analysis and stronger business reasoning — which is a very different hiring bar than the one most people are studying for.

If your plan is "I'll learn the AI stuff once I'm a bit more senior," I'd push back on that directly. The junior role you're trying to grow into is the one being redefined right now. Waiting doesn't keep the door open — it just means you show up later to compete for a version of the job that's already moved on.

## Where I'd Actually Tell Someone to Start

Not "go learn machine learning." That's overkill for most analyst roles and, honestly, a bit of a distraction from what actually matters right now.

Instead, start treating AI as part of your daily toolkit this week, not eventually:

1. **Use AI to interrogate your own SQL, not just to write it for you.** Ask it to poke holes in your query logic before you run it. You'll learn faster this way than from another course module.
2. **Automate one boring, recurring task.** Pick something you do manually every week and hand it to an AI workflow instead. See exactly where it breaks — that's more instructive than it sounds.
3. **Build the habit of validating before repeating.** When a tool hands you a summary or a trend, check it against the raw data before you say it out loud in a meeting.
4. **Treat prompting like querying.** Precision matters. A vague prompt gets you a vague insight, the same way a poorly written `WHERE` clause gets you a wrong table.
5. **Never skip the "so what."** Pair every AI-generated insight with a business implication. That layer isn't getting automated any time soon, and it's the layer that actually gets you noticed.

## Where I Land On This

The tools got faster. The bar for judgment didn't drop — it went up, because now you're not just doing the analysis, you're the last line of defense on whether it's right.

Analysts who'll do well over the next few years won't be the ones who resisted AI, and they won't be the ones who blindly trusted it either. They'll be the ones who learned to direct it with the same rigor they'd apply to a query or a model — and who never stopped asking the smarter question underneath the fast answer.

*If you're early in your analytics career and want a starting point for building AI into your daily workflow, that's exactly what I'll be writing more about here — practical, no-hype, from someone doing this work day to day.*
