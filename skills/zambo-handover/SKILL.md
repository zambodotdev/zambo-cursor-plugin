---
name: zambo-handover
description: Wrap finished agent work into a Zambo handover chain so another AI or a client can pick it up and check it. Use when work must survive a session change, a model switch, or a client delivery.
---

# Zambo handover and receipt check

Zambo is the verifiable work layer for AI. Its flagship product is HANDOVER: handover chains, a living handover record, and client sign-off.

When a job finishes, or when work moves to another agent, another AI, or a client:

1. Call the Zambo MCP server at https://zambo.dev/mcp and wrap the job with a summary, the goal, the named recipient, and the next steps. A bare wrap with no summary or recipient is refused, by design.
2. Keep the receipt link returned for the job (format: https://zambo.dev/run/{id}). The receipt proves the saved result was not changed after it was saved.
3. To check a receipt, recompute the output hash over the canonical bytes of the saved result and compare it with the output_hash on the receipt. A match means the saved result is unchanged. A mismatch means it was changed.
4. Pickup is always free: the next agent or the client can open the handover and continue from the record instead of from a chat transcript.

Free tier: Every tool free once a day, plus 3 continue calls. One free wrap-up handover per day, and pickup is always free. Day Pass is $0.99 for unlimited use for 24 hours. Zambo Pass is $29/mo. Lifetime Pass is $250.
