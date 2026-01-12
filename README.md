# IdeaMiner

IdeaMiner is a read-only research script that analyzes public Reddit discussions to identify recurring pain points and trending themes (“branches”), with a focus on:
- “hair-on-fire” problems (blocked, urgent, high frustration)
- tool-seeking intent (“any tool”, “template”, “alternatives”, “how do I…”)
- repeated manual workflows (spreadsheets, copy/paste, reporting, reconciliation)

## What it does
1. Fetches a small number of public posts from selected subreddits (hot/new/top).
2. Scores threads for pain + demand + manual-work signals.
3. For shortlisted threads only, fetches a limited number of top comments for context.
4. Produces aggregated outputs: ranked threads, clustered themes, suggested micro-SaaS wedges.

## Compliance / data handling
- Uses the official Reddit Data API via OAuth (when approved).
- Read-only: no posting, commenting, voting, messaging, or moderation actions.
- Stores minimal metadata (IDs, timestamps, subreddit, score/comments, URL) and derived tags/summaries.
- Raw content is not stored long-term; routine deletion/purging is performed and deletions are respected.
- Reddit data is **not** used to train any ML/LLM models; LLMs (if used) are for summarization/classification only.

## Status
Early prototype / scaffolding.
