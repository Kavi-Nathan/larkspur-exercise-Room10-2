# PITCH.md

Six lines and a lever. Your words. The last two are scored.

Built: A disruption-care agent that looks up bookings, verifies flight status, resolves policy, and offers safe rebooking paths.
Does: It gathers evidence from Altura, OpsFeed, and policy before explaining what a disrupted passenger can do next.
Number: Model cost is $0.0253 per resolved contact after caching, down from $0.0582 before, against $6.90 for a human contact; the sponsor can defend the unit and denominator.
Safety check: Irreversible rebooking requires a UI-issued confirmation token, while refunds and out-of-scope cases escalate to a human.
Next: Choose one cost lever and benchmark it before and after: cache the stable system prompt and tool list in both `messages.create` calls, prune tools the trace never called, or lower `max_tokens` with a one-line answer rule.
Still broken: This lever may reduce token cost per resolved contact, but the number will not cover latency, SLA performance, abandonment, or answer quality.
Lever: cost

## Priya asked

Costs: The sponsor can defend model dollars per contact against the $6.90 human baseline; inspect cache reads and writes, token totals, and tool-list schema cost separately, then keep only the lever that lowers cost without harming SLA or answer quality.
Wrong: The first wrong thing can be a tool argument, such as an invalid date; the backend returns an error and the model must recover before answering.
Runs it: Larkspur customer-care staff run the agent with the shared MCP service, while an on-call owner monitors traces and escalates exceptions.
Left out: We left out autonomous refunds, payment handling, and final rebooking confirmation because those actions need a human or an authenticated customer click.
