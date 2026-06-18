# HeyGen Video Script — PHANTOM-MNQ: AI Quorum Execution on Apex Eval

**Speaker:** Vincent Casella — CEO, S3 Development / ESS Division
**Audience:** Dual — retail traders (prop firm context) + S3 developer team
**Estimated Duration:** ~2 minutes (~290 words)
**model_id:** TRNQL_8AMsweep.v3
**System:** PHANTOM-MNQ
**Status:** LIVE — Apex Trader Funding Eval ($50K)

---

### Script

**(Confident, measured. Direct to camera. Opens with a trader-facing hook, builds to the system reveal.)**

"Let me show you what we built.

Every morning — right at 8AM Eastern — the New York futures market sets a trap. Market makers push price into a liquidity zone, sweep the stops, then reverse hard. That move — traders call it the 8AM range sweep — is one of the most consistent setups on Micro Nasdaq futures.

We built a system called PHANTOM-MNQ to trade it autonomously on an Apex Trader Funding evaluation account.

Here's how it works.

Our Pine Script strategy, Iron Sight, runs live on MNQ on TradingView. When the sweep fires, it sends a signal to our server stack running on Google Cloud. No human intervention — the signal hits the moment the bar closes.

That signal then goes to PHANTOM — our 10-agent AI council. Ten independent AI pipelines evaluate the setup simultaneously. Each one scores the trade using an LSTM model and runs it through a Claude language model for a final verdict. The options are CONFIRM, HOLD, or OVERRIDE.

If six or more agents return CONFIRM — quorum is met. Execution fires.

At that point, a bracket order is sent to NinjaTrader 8 via the ATI interface — market entry, stop loss, and take profit as a linked OCO pair. The order routes through Tradovate directly to the Apex eval account.

Every signal — traded or skipped — is logged to our Sentinel database. Full audit trail.

This is what institutional-grade automation looks like at the retail level. And it is live.

Full architecture documentation is on the S3 Iron Sight developer site. Links in the description."

---

### Production Notes for HeyGen

- **Avatar:** Vincent Casella persona. Professional attire — dark blazer or button-down. Clean executive presence.
- **Background:** Dark tech / trading floor aesthetic. If using a scene background, something with monitors showing chart data works well — matches the Iron Sight brand.
- **Pacing:** Open with a slightly faster, punchy delivery on the hook ("Let me show you what we built"). Slow down and emphasize each system layer — Iron Sight, GCP, PHANTOM, NinjaTrader. Pause after "quorum is met" for effect.
- **Emphasis words:** "8AM range sweep," "ten independent AI pipelines," "six or more agents," "quorum is met," "live"
- **Tone:** Confident and credible — not hype. This is a technical team showing real work. Traders should feel confidence; developers should feel precision.
- **Slides / B-roll (optional — HeyGen screen overlay or split):**
  - At "Iron Sight runs live on MNQ" → show the TradingView chart with TRNQL_8AMsweep.v3 loaded on MNQ1! 5-minute
  - At "ten independent AI pipelines" → show the quorum visualiser from the architecture page
  - At "bracket order is sent to NinjaTrader 8" → show the NT8 ATI command block or NT8 bracket order confirmation
  - At "Full architecture documentation" → show the iron-sight-docs PHANTOM-MNQ architecture page
- **Closing frame:** S3 Development logo + `phantom-bridge.S-3.us` or `S-3.us` URL on screen
- **CTA text on screen:** "PHANTOM-MNQ Architecture — S3 Iron Sight Developer Docs"
