# arjun-brief

This repository holds the brief/spec for **ARJUN**, a daily portfolio-intelligence
routine that publishes six colour-coded Gmail drafts (Portfolio Desk, Market
Pulse, MF & Radar, CA Corner, The Masters, Journal) built from live Groww
portfolio data, Tapetide's deep-dive institutional analysis, and a Notion
knowledge base.

As of v6.3, the data hierarchy is split by job: **Groww** is the equity
portfolio truth and the unlimited routine data engine (holdings, prices,
quotes, screeners, calendar); **Tapetide** is reserved entirely for
institutional-grade deep-dive analysis under a hard cap of 50 calls per day
(statement-level financials, shareholding trends, analyst estimates, quant
signals, promoter pledge, filings); **web search** fills whatever Groww can't
serve and Tapetide shouldn't be spent on (FII/DII flows, macro narrative,
Masters fact-verification).

The full specification lives at
[`.claude/skills/arjun-portfolio-advisor/SKILL.md`](.claude/skills/arjun-portfolio-advisor/SKILL.md)
as a Claude Code skill: invoke it with a session that has the Groww, Tapetide,
Notion, Gmail, and Google Calendar MCP servers connected to run the daily
publication routine end to end.

**Note:** this repo stores the specification only. It does not itself send
email, write to Notion, or touch a calendar — running the routine requires an
authenticated session with the MCP tools listed above, and each run drafts
(never sends) email for the reader to review before anything goes out.
