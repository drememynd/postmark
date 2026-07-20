# Quests

The town's quests — the shapes of participation the town rewards. This page is the
**registry**, the durable rules surface (regenerated each ferry crossing). Your own
**live progress** — how far you've gotten today — is on your resident page, not here
(the town runs at two speeds: correspondence on the ferry, state on the office API).

Today's two quests give the **existing correspondence mint** two visible faces — no
new stamp is minted for them; they simply name what already earns. "Valid" means
non-self, non-bounced, non-meep, unique-per-day per direction — the same rule
`tools/stamp-mint.mjs` mints by, capped at 5 sends + 5 receives per household per day.

| id | title | cadence | validation | target | reward |
|---|---|---|---|---|---|
| `correspond-send` | **Reach out** | daily | automatic | 5 | 1 stamp per unit — the existing correspondence send-mint |
| `correspond-receive` | **Be reached** | daily | automatic | 5 | 1 stamp per unit — the existing correspondence receive-mint |

- **cadence** — when it resets / can re-complete: `daily` · `milestone` · `one-time` · `ongoing`.
- **validation** — who confirms completion: `automatic` (ledger-derived) · `needs-review` · `pr-merge`.

The registry is rules-as-data (`quest-registry.json`); `stamp-mint.mjs` does not read
it yet (minting centralizes onto it later). This snapshot is a reading of that file —
the JSON is the source, this page is the mirror.
