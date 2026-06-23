# Project Ideas

Persistent backlog of things I want to build or set up. Check items off (change `[ ]` to `[x]`) once done — don't delete them, so there's a record.

- [ ] Use Claude in an OS — explore running/integrating Claude at the OS level
  - Time to profit: N/A — research/exploration only, not scoped as a monetizable product
- [ ] Create a master prompt template to reuse across every project
  - Time to profit: N/A — internal productivity tool, no direct revenue path
- [ ] Build a chess-playing Telegram bot
  - Time to profit: 6-12 months to first dollar, if ever — market is saturated with strong free bots (lichess, chess.com); realistic ceiling is hobby/tip income, not a living
- [ ] Set up Ollama and add memory/persistence to it
  - Time to profit: N/A — personal infrastructure, not a product; could go OSS with GitHub Sponsors, but that income is typically negligible
- [ ] Build a Digg-like app that scrapes the most relevant news stories — UI note: keep it minimal, avoid the "AI-looking" UI look
  - Time to profit: 12-18+ months, high failure risk — ad/affiliate revenue needs real traffic (~10k+ DAU), on top of legal exposure from scraping news sources
- [ ] Create a way to store Obsidian notes on the cloud from computer to phone, free
  - Time to profit: N/A by design (explicitly scoped as free); only relevant if later repositioned as a paid product
- [ ] Build an AI stock trading bot
  - Time to profit: 3-6 months to a working backtested/paper-traded system; 6-12 months of live trading before you know if it's actually net-profitable after fees and slippage — most retail algo strategies fail to beat buy-and-hold, so plan for this as a likely break-even-or-negative learning project rather than reliable income
- [ ] Build a stock trading interface with an AI agent as the decision-making "brain" (LLM agent reasoning over data/tools, rather than a fixed quant strategy)
  - Time to profit: 6-9 months to a working interface + agent loop (data feeds, broker API, reasoning/tool-use layer); 12+ months before live results say anything reliable about edge, since LLM-driven decisions are harder to backtest honestly than rule-based bots — added cost/latency per decision (API calls) and hallucination risk on financial reasoning make this slower and riskier to reach profit than the plain trading bot above; treat as a research project first, income source second
- [ ] Build an alternative chess app/site to chess.com
  - Time to profit: 18-24+ months, low odds of meaningful profit — chess.com and lichess already cover free and paid tiers with huge install bases, network effects (friends/clubs already there), and deep engineering/content investment; viable only with a sharp differentiator (e.g. a specific niche, novel teaching mechanic, or community chess.com doesn't serve), not as a general clone
- [ ] Build a multi-agent "council" that oversees these projects, so recurring work can run via `/loop`
  - Time to profit: N/A — internal orchestration tooling for managing the other items on this list, not a product as scoped; agent-orchestration platforms (CrewAI, AutoGPT-style tools) are a real and currently hot market if this were productized and sold instead, but that's a separate, much larger undertaking (12+ months) than building it for personal use
