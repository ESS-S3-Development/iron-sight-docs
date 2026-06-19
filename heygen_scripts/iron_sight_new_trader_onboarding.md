# HeyGen Video Script
## Iron Sight — New Trader Onboarding
**Production:** S3 Development / Project Black-Box  
**Runtime:** ~5–6 minutes  
**Avatar:** Vincent Casella — Professional Dark Tech  
**Background:** Dark command-center / trading desk aesthetic (deep navy, ambient blue glow)  
**Lower thirds font:** Monospace / tech style, S3 blue (#2962ff)

---

## PRODUCTION NOTES
- Avatar framing: medium shot, centered, confident posture
- Tone: calm, authoritative, welcoming — not salesy
- Pacing: deliberate. Pause 1 second between numbered steps
- Screen overlays: use TradingView UI screenshots where noted
- Logo watermark: Iron Sight / S3 Dev — lower right corner throughout

---

## [SCENE 1 — INTRO HOOK]
*[Avatar on screen. Dark background. S3 logo animates in top-left.]*

---

If you've been invited into the Iron Sight beta program — welcome.

My name is Vincent Casella. I'm the developer behind Project Black-Box and the Iron Sight signal system.

In the next five minutes, I'm going to walk you through exactly how to get set up — from creating your TradingView account to receiving your first live signal.

No coding. No prior experience required. Just follow each step in order, and you'll be ready.

Let's get into it.

---

## [SCENE 2 — WHAT IS IRON SIGHT]
*[Transition: Iron Sight logo card. Brief animated graphic of signal flow: Chart → Signal → Alert → Webhook.]*

---

Iron Sight is a precision signal system that runs inside TradingView.

The scripts watch the market, identify specific setups, and fire alerts that route directly into our execution engine — a system we call NIGHTHAWK.

During the beta phase, you're in **Observation Mode.** That means every signal gets logged, you get an SMS notification, but no orders are placed automatically. You paper trade first. That's intentional.

The goal in beta is simple: prove the signal performs in your hands before any real capital is on the line.

---

## [SCENE 3 — WHAT YOU NEED]
*[Lower third: "BEFORE YOU BEGIN"]*  
*[Three graphic cards appear on screen: TradingView logo, Key icon, Brokerage icon]*

---

Before we get into setup, three things you need to have ready.

**One.** A TradingView account. A free account works for viewing signals and paper trading manually. If you want alerts to fire automatically to NIGHTHAWK, you'll need at least the Essential paid plan.

**Two.** Your access credentials. Your admin — that's me — will issue you a Webhook URL, a TV Secret key, and a Trader ID. You cannot generate these yourself. Do not skip this step.

**Three.** A brokerage account. For paper trading, any paper account works. For the TRNQL futures script, you'll want NinjaTrader or an Apex Trader Funding evaluation account.

Got all three? Let's go.

---

## [SCENE 4 — STEP 1: TRADINGVIEW ACCOUNT]
*[Lower third: "STEP 1 — CREATE YOUR TRADINGVIEW ACCOUNT"]*  
*[Screen overlay: TradingView.com homepage]*

---

Head to TradingView dot com and create a free account.

One important note here: **sign up with email, not a social login.** Your TradingView username is how I identify you when granting script access — make it something clean and professional.

Something like your name followed by underscore trader. Not a random set of numbers.

Once you're registered, write down your username. You'll need it in the next step.

---

## [SCENE 5 — STEP 2: REQUEST ACCESS]
*[Lower third: "STEP 2 — REQUEST SCRIPT ACCESS"]*  
*[Screen overlay: Email template or contact card graphic]*

---

Iron Sight scripts are **private, invite-only** publications on TradingView. You cannot find them by searching — I have to grant you access directly.

Send me an email — the address is at the bottom of the onboarding page at Iron Sight Docs — with the following:

Your TradingView username. The script or scripts you're requesting. Your broker and account type. And whether you're starting with paper or live intent.

Once I've granted access and registered your model in the Sentinel database, I'll reply with your **Webhook URL**, your **TV Secret**, and your **Trader ID.** 

Keep that TV Secret private. Treat it like a password.

---

## [SCENE 6 — STEP 3: ADD THE SCRIPT TO YOUR CHART]
*[Lower third: "STEP 3 — ADD THE SCRIPT TO YOUR CHART"]*  
*[Screen overlay: TradingView chart with Indicators panel open → Invite-Only Scripts section]*

---

Once access is granted, the Iron Sight scripts will appear in your **Invite-Only Scripts** library inside TradingView.

Here's how to add one to your chart:

Open TradingView. Navigate to the correct ticker and timeframe for your assigned script. For TRNQL, that's MNQ1! on a one-minute or five-minute chart.

Click **Indicators** at the top — or press the forward slash key.

Select **Invite-Only Scripts** from the left panel. You'll see the scripts I've shared with you.

Click the script name. It will load onto your chart with signal markers, key levels, and gap labels already plotted.

Do not adjust the default settings unless I specifically tell you to. The parameters are pre-calibrated.

---

## [SCENE 7 — STEP 4: SET UP THE WEBHOOK ALERT]
*[Lower third: "STEP 4 — SET UP YOUR WEBHOOK ALERT"]*  
*[Screen overlay: TradingView alert dialog with Webhook URL field highlighted]*

---

This is the step that connects your chart to NIGHTHAWK — our signal router.

Right-click anywhere on your chart and select **Add Alert.** Or press Alt plus A.

In the alert dialog:

Set the **Condition** to the Iron Sight script name and select the correct alert condition.

Set **Trigger** to **Once Per Bar Close.** This is important — do not use Once Per Bar. That fires on intrabar ticks and will flood the system with noise.

Under **Notifications**, enable **Webhook URL** and paste the Webhook URL I gave you.

Leave the **Message field completely empty.** The script builds the JSON payload automatically — it already includes your TV Secret and Trader ID. Overwriting it will break signal authentication.

Click **Create.** You'll see a green bell on the chart — that means the alert is live.

---

## [SCENE 8 — STEP 5: PAPER TRADING]
*[Lower third: "STEP 5 — BEGIN PAPER TRADING"]*  
*[Graphic: tracking sheet / spreadsheet visual]*

---

You're now connected. Here's what to do from day one.

Download the **Live Signal Tracking Template** from me or from the onboarding page. Every time a signal fires, log it — whether you take the trade or not. A skipped signal is data. I need it.

Follow the paper trading SOP exactly: entry timing, contract selection, T1 and T2 exit rules, and the **2:30 PM Eastern hard close.** No exceptions.

Also log your VIX reading at entry. High VIX — above 20 — inflates option premiums significantly. Knowing this context is critical when we review your results.

Your target is **five completed paper signals.** After five, we review together and make a go or no-go decision on live capital.

---

## [SCENE 9 — WHAT HAPPENS NEXT]
*[Lower third: "WHAT HAPPENS AFTER SETUP"]*  
*[Timeline graphic: Access Granted → Paper Trading → Review → Live Authorization]*

---

Here's what the full pipeline looks like:

**First**, you receive access and your credentials. Your model is registered in Sentinel in Observation Mode.

**Then**, you paper trade. Signals log automatically. You track them manually and submit your sheets after five signals.

**Then**, we review. T1 hit rate, average premium expansion, exit quality. If the data is strong — T1 hit rate at sixty-five percent or above — we move to the next phase.

**Finally**, your Sentinel model is switched to LIVE. From that point, every qualified signal routes an order to your broker automatically, within milliseconds of the alert firing on your chart.

That's the full path from setup to live execution.

---

## [SCENE 10 — CALL TO ACTION / OUTRO]
*[Avatar centered. S3 logo visible. Lower third: ironsightdocs.executivespecialservice.us]*

---

If you're ready to get started, the full onboarding guide with every link, credential request template, and script reference is at:

**Iron Sight Docs dot Executive Special Service dot U S**

Email me directly at the address on that page — include your TradingView username and your broker setup — and I'll have you registered and access granted within twenty-four hours.

This is a precision system. The setup matters. Follow the steps in order, paper trade the minimum five signals, and trust the process.

We'll be in touch.

*[S3 logo holds on screen. Fade to black.]*

---

## POST-PRODUCTION NOTES
- **Chapters** (for YouTube/embedded player):
  - 0:00 — Introduction
  - 0:40 — What Is Iron Sight
  - 1:10 — What You Need
  - 1:45 — Step 1: TradingView Account
  - 2:10 — Step 2: Request Script Access
  - 2:50 — Step 3: Add the Script
  - 3:30 — Step 4: Set Up the Webhook Alert
  - 4:20 — Step 5: Paper Trading
  - 5:00 — What Happens Next
  - 5:40 — Get Access
- **Thumbnail text:** "Iron Sight — New Trader Setup Guide"
- **Title (YouTube):** Iron Sight New Trader Onboarding — Setup Guide | S3 Development
- **Description tag:** Iron Sight, TradingView, Signal System, MNQ, TRNQL, Futures, Paper Trading, Project Black-Box
