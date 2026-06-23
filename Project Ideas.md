# Project Ideas

Persistent backlog of things I want to build or set up. Check items off (change `[ ]` to `[x]`) once done — don't delete them, so there's a record.

- [ ] Create a dashboard to handle multiple agents at once, heavy on customization
  - Time to profit: 9-15 months — buildable MVP in 3-5 months, but the agent-orchestration space (LangGraph Studio, CrewAI, Relevance AI, etc.) is crowded and well-funded; realistic path to profit is a narrow, "heavy customization for power users" wedge rather than competing head-on, similar risk profile to the multi-agent council idea below but framed as a sellable product instead of personal tooling
- [ ] Create personality prompts for local agents
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
  - Time to profit: 12-18 months if positioned specifically as the clean/ad-light mobile alternative — there's a real, documented wedge here (chess.com forum threads show paying Diamond members complaining about heavy ads, including ads injected into premium features, with some letting memberships lapse over it); still requires beating lichess on mobile polish (lichess is already free and ad-free) and clearing the same network-effects/install-base gap as a general clone, so treat the timeline as optimistic-but-plausible rather than likely
- [ ] Run several local agents simultaneously as separate advisors (each with its own personality/angle) plus one "head" agent that coordinates them, so a problem gets analyzed from multiple perspectives and the agents cross-check each other to catch hallucinations; explicitly prompt against being a "yes man" — agents should be willing to tell me no, not just agree; also the basis for overseeing the other projects on this list via `/loop`
  - Time to profit: N/A — personal tooling, not scoped as a product; the cross-checking approach is a real, validated technique ("multi-agent debate"), with published results showing a ~36% relative reduction in hallucination rate (HaluEval) and a 7.8-point gain on TruthfulQA — but it's a reduction, not elimination, so don't treat consensus among the agents as proof of correctness; the anti-yes-man requirement is fighting a real, separately-documented failure mode (sycophancy bias from RLHF tuning, where models default to agreeing with the user even when wrong) — needs deliberate prompting (e.g. explicitly rewarding disagreement when warranted) since it won't happen by default; depends on the Ollama setup (for local model hosting) and personality prompts (for the distinct advisor angles) above
