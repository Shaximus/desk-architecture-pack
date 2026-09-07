# Ontario, product limits, and safety

## Jurisdiction

The account that requested this pack resolved to Cornwall, Ontario.

Polymarket's international venue has been the subject of an Ontario Securities Commission action (2025) against the operator group. The practical consequence for an Ontario IP is a geo-block and an advertising ban. This pack does **not** describe VPN circumvention, mirror apps, or "trade through this app" funnels.

If you want live event contracts from Canada, use a venue that is actually available to you after you read *its* terms (examples that exist in the market: licensed forecast/event products at regulated brokers; they are not the same order book as Polymarket 5-minute crypto binaries).

The simulator in this repo is venue-agnostic on purpose.

## Grok Bot product facts that kill the 200-bot video

Official docs (docs.x.ai/grok-bot):

- Every Bot on one account shares **one** persistent cloud computer.
- Files, browser sessions, and logins are shared.
- "Do not use separate Bots as a security boundary."
- Group chats take **2 to 6** Bots.
- Community/docs consensus: on the order of **50 Bots and group chats combined** per account.
- Secrets go through **Take over**, never chat.
- Deleting a Bot does not wipe the shared machine.

So: 200 isolated Grok Bots with separate wallets is not a thing you can buy. 200 *local* inference workers behind a merge graph is a different design, and even then they should be cheap scanners or Monte Carlo particles, not 200 order senders.

## What never goes on the shared Grok Bot computer

- Seed phrases, private keys, API secrets that can withdraw
- The wallet that holds anything you cannot lose
- Client data, extra mailboxes, extra exchange logins
- A Telegram session that can be used to drain a bot

## Live path if you ever leave paper

1. New account at a venue you may legally use.
2. Trade-only credential if the venue supports it.
3. Ticket file written by research agents.
4. Risk veto in code.
5. Human types or clicks the ticket ID.
6. Deterministic executor sends.
7. Daily kill switch.
8. Journal + deflated-Sharpe style review, not vibes.
