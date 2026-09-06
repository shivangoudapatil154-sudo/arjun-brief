# arjun-brief

This repository holds the brief/spec for **ARJUN**, a daily portfolio-intelligence
routine that publishes six colour-coded Gmail drafts (Portfolio Desk, Market
Pulse, MF & Radar, CA Corner, The Masters, Journal) built from live Tapetide
market data and a Notion knowledge base.

The full specification lives at
[`.claude/skills/arjun-portfolio-advisor/SKILL.md`](.claude/skills/arjun-portfolio-advisor/SKILL.md)
as a Claude Code skill: invoke it with a session that has the Groww,
Tapetide, Notion, Gmail, and Google Calendar MCP servers connected to run
the daily publication routine end to end. As of v6.3, Groww holds the
portfolio truth and all routine market data (unlimited calls); Tapetide's
50-call daily budget is spent entirely on institutional-grade deep-dive
analysis.

**Note:** this repo stores the specification only. It does not itself send
email, write to Notion, or touch a calendar — running the routine requires an
authenticated session with the MCP tools listed above, and each run drafts
(never sends) email for the reader to review before anything goes out.
