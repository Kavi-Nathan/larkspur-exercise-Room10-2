# PITCH.md

Six lines and a lever. Your words. The last two are scored.

Built: A disruption-care agent that looks up bookings, verifies flight status, resolves policy, and offers safe rebooking paths.
Does: It gathers evidence from Altura, OpsFeed, and policy before explaining what a disrupted passenger can do next.
Number: 4 API turns per resolved ticket, n=1 on the K7PQ2M trace, with 11 tools offered on each turn.
Safety check: Irreversible rebooking requires a UI-issued confirmation token, while refunds and out-of-scope cases escalate to a human.
Next: Run the full five-ticket sweep and benchmark the before-and-after lever with recorded traces and token counts.
Still broken: The agent can still make an untrue claim if a tool returns misleading data or the model accepts an unchecked result.
Lever: <cost | speed | intelligence>

## Priya asked

Costs: Dollar cost is not measured yet; the latest resolved trace used 19,924 input and 721 output tokens, against $6.90 for a human contact.
Wrong: The first wrong thing can be a tool argument, such as an invalid date; the backend returns an error and the model must recover before answering.
Runs it: Larkspur customer-care staff run the agent with the shared MCP service, while an on-call owner monitors traces and escalates exceptions.
Left out: We left out autonomous refunds, payment handling, and final rebooking confirmation because those actions need a human or an authenticated customer click.
