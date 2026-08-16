---
title: "The 3 SQL Antipatterns I See Most Often (And How to Fix Them)"
description: "Three recurring SQL mistakes that quietly inflate cost and slow queries down — and the fixes I reach for every time."
pubDate: "Aug 15 2026"
---

Most slow, expensive queries aren't broken because of one dramatic mistake. They're slow because of a handful of small, repeatable patterns that show up in almost every codebase — mine included, early on. Here are the three I run into most often, and what I do instead.

## 1. `SELECT *` on wide tables

It's the fastest way to write a query and the fastest way to make it expensive. On a warehouse like BigQuery or Snowflake, you're billed by data scanned — pulling every column when you need three of them means paying for columns nobody's using.

**Fix:** explicit column projection. List exactly what you need. On genuinely wide tables (50+ columns), this alone can cut scan cost dramatically, no other optimization required.

## 2. Correlated subqueries where a JOIN would do

A correlated subquery re-runs once per row of the outer query — on a small table that's invisible, on a few million rows it becomes the query that never finishes. I still see this most often in "just get me a count for each X" queries that grew organically over time.

**Fix:** rewrite as a JOIN with a GROUP BY, or a window function if you need row-level context alongside an aggregate. Same result, usually an order of magnitude faster.

## 3. Filtering after aggregating instead of before

Running a `GROUP BY` across an entire table and only filtering the result down afterward means your warehouse did all that aggregation work for rows you were going to throw away anyway.

**Fix:** push filters as early as possible — filter in the `WHERE` clause before aggregation, not just in a `HAVING` clause after. On partitioned tables, this also means partition pruning actually kicks in, which by itself can eliminate scanning most of the table.

## Why this matters beyond query speed

None of these are exotic problems. They're the kind of thing that creeps in gradually — a query written under deadline pressure, copied and extended six times, never revisited. The cost shows up quietly, in a warehouse bill or a dashboard that takes 40 seconds to load instead of 4.

I built these exact checks into the [AI SQL Optimizer](/tool) on this site — paste in a query and it'll flag these patterns (and a few others) automatically, entirely in your browser. If you want to see what it catches in your own queries, it's free to try.
