# Technical decisions

## ADR 001 — transparent rule-based baseline

**Status:** accepted

**Context:** the initial version needs recommendations that can be inspected and evaluated without relying on a labeled match dataset.

**Decision:** use explicit matchup rules and a deterministic heuristic score to rank candidate items. Each recommendation should include the rule or item signal that contributed to it.

**Benefits:**
- The behavior is inspectable and reproducible.
- Recommendations can be explained to users.
- Scenarios can evaluate the expected behavior without external services.

**Trade-offs:**
- The rules do not learn from match outcomes.
- Coverage is limited to the authored catalog and rules.
- The score must not be interpreted as win probability or statistically measured item quality.

**Future consideration:** compare the baseline with a learned ranking approach only when suitable, permitted data and an evaluation method are available.

## ADR 002 — versioned local catalog

**Status:** accepted

**Decision:** keep the initial champion and item catalog in local JSON files and record the patch and source.

**Trade-off:** data refresh is explicit; the catalog does not update itself.

## ADR 003 — no automated OP.GG dependency

**Status:** accepted

**Decision:** do not make the initial application depend on OP.GG scraping. Use Riot's Data Dragon for static metadata and document the source of any additional data introduced later.

**Reason:** keep the prototype reproducible and avoid presenting third-party statistics as an official public API.
