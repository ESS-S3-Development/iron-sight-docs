# HeyGen Video Script
## Iron Sight — New Trader Onboarding
**Production:** S3 Development / Project Black-Box  
**Runtime:** ~7–8 minutes  
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

My name is Vincent Casella and along with Chris Casella we are the creators and developers behind Project Black-Box and the Iron Sight signal system.

In the next five minutes, we're going to walk you through exactly how to get set up — from creating your TradingView account to receiving your first live signal.

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

**Two.** Your access credentials. Your admin — that's us — will issue you a Webhook URL, a TV Secret key, and a Trader ID. You cannot generate these yourself. Do not skip this step.

**Three.** A brokerage account. For paper trading, any paper account works. For the TRNQL futures script, you'll want NinjaTrader or an Apex Trader Funding evaluation account.

Got all three? Let's go.

---

## [SCENE 3A — OPTIONAL: APEX TRADER FUNDING & NINJATRADER SETUP]
*[Lower third: "PROP TRADING PATH — APEX + NINJATRADER"]*  
*[Screen overlay: Apex Trader Funding website → account selection screen]*

---

If you want to trade TRNQL through the **prop trading path** — meaning you're trading a funded evaluation account instead of your own capital — this scene is for you. If you're paper trading only for now, you can skip ahead.

**What is Apex Trader Funding?**

Apex is a prop firm that gives you access to a simulated funded account. You pay a monthly evaluation fee, and in return you get a trading account with real market data and real execution — but it's their capital on the line, not yours. Pass the evaluation, and you can earn a share of the profits.

For TRNQL, we recommend the **TradeOvate 50K account with a two-thousand-dollar trailing drawdown.**

Let's break that down.

The **50K** means you're trading a simulated fifty-thousand-dollar account. The **two-thousand-dollar trailing drawdown** is the key risk parameter — it means if your account balance ever drops two thousand dollars below its highest point, the evaluation ends. So if you start at fifty thousand and run the account up to fifty-two thousand, your drawdown threshold moves up too. It protects gains. But breach it, and you're done for that evaluation cycle.

This account size and drawdown limit is calibrated for the single-contract MNQ positions that TRNQL trades. It gives you enough breathing room while keeping risk tight.

*[Screen overlay: Apex account selection page showing 50K TradeOvate plan]*

When you sign up at Apex Trader Funding, select the **TradeOvate** platform option and choose the **50K** plan. Complete checkout — you'll receive an email with your **Apex-assigned TradeOvate username and password.** These are different from your Apex website login. Write them down.

---

**Logging Into TradeOvate**

*[Screen overlay: TradeOvate login screen]*

When you open TradeOvate, you will be asked for a username and password. **Use the credentials Apex sent you — not your Apex website email and password.** This is a common point of confusion. The Apex website login and the TradeOvate platform login are two separate credential sets.

Log in, confirm your account is active, and you're ready to connect NinjaTrader.

---

**Setting Up NinjaTrader**

*[Screen overlay: NinjaTrader → Connections menu → New connection dialog]*

NinjaTrader is the charting and execution platform we use for TRNQL. Download and install it from NinjaTrader dot com. Once it's open:

**One.** Go to the top menu and click **Connections**, then select **Configure.**

**Two.** Click **Add** to create a new connection. Give it a name — something like **Apex TradeOvate** so you know exactly what it maps to.

**Three.** For the connection type, select **CQG** or **Rithmic** — whichever is listed as TradeOvate's data feed. Apex will specify this in your welcome email.

**Four.** Enter the **Apex-assigned TradeOvate username and password** in the credential fields. Again — these are the credentials from your Apex welcome email, not your Apex website login.

**Five.** Click **OK**, then go back to **Connections** and click your new connection name to go live. The status bar at the bottom of NinjaTrader will show **Connected** when it's working.

Once connected, you'll see your Apex simulated account populate in NinjaTrader. From there, TRNQL signals from TradingView will route through NIGHTHAWK and execute directly on that account.

---

## [SCENE 4 — STEP 1: TRADINGVIEW ACCOUNT]
*[Lower third: "STEP 1 — CREATE YOUR TRADINGVIEW ACCOUNT"]*  
*[Screen overlay: TradingView.com homepage]*

---

Head to TradingView dot com and create a free account.

One important note here: **sign up with email, not a social login.** Your TradingView username is how we identify you when granting script access — make it something clean and professional.

Something like your name followed by underscore trader. Not a random set of numbers.

Once you're registered, write down your username. You'll need it in the next step.

---

## [SCENE 5 — STEP 2: REQUEST ACCESS]
*[Lower third: "STEP 2 — REQUEST SCRIPT ACCESS"]*  
*[Screen overlay: Email template or contact card graphic]*

---

Iron Sight scripts are **private, invite-only** publications on TradingView. You cannot find them by searching — we have to grant you access directly.

Send us an email — the address is at the bottom of the onboarding page at Iron Sight Docs — with the following:

Your TradingView username. The script or scripts you're requesting. Your broker and account type. And whether you're starting with paper or live intent.

Once we've granted access and registered your model in the Sentinel database, we'll reply with your **Webhook URL**, your **TV Secret**, and your **Trader ID.** 

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

Select **Invite-Only Scripts** from the left panel. You'll see the scripts we've shared with you.

Click the script name. It will load onto your chart with signal markers, key levels, and gap labels already plotted.

Do not adjust the default settings unless we specifically tell you to. The parameters are pre-calibrated.

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

Under **Notifications**, enable **Webhook URL** and paste the Webhook URL we provided.

Leave the **Message field completely empty.** The script builds the JSON payload automatically — it already includes your TV Secret and Trader ID. Overwriting it will break signal authentication.

Click **Create.** You'll see a green bell on the chart — that means the alert is live.

---

## [SCENE 8 — STEP 5: PAPER TRADING]
*[Lower third: "STEP 5 — BEGIN PAPER TRADING"]*  
*[Graphic: tracking sheet / spreadsheet visual]*

---

You're now connected. Here's what to do from day one.

Download the **Live Signal Tracking Template** from us or from the onboarding page. Every time a signal fires, log it — whether you take the trade or not. A skipped signal is data. We need it.

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

Email us directly at the address on that page — include your TradingView username and your broker setup — and we'll have you registered and access granted within twenty-four hours.

This is a precision system. The setup matters. Follow the steps in order, paper trade the minimum five signals, and trust the process.

We'll be in touch.

*[S3 logo holds on screen. Fade to black.]*

---

## POST-PRODUCTION NOTES
- **Chapters** (for YouTube/embedded player):
  - 0:00 — Introduction
  - 0:40 — What Is Iron Sight
  - 1:10 — What You Need
  - 1:45 — Apex Trader Funding & NinjaTrader Setup (Prop Path)
  - 3:10 — Step 1: TradingView Account
  - 3:35 — Step 2: Request Script Access
  - 4:15 — Step 3: Add the Script
  - 4:55 — Step 4: Set Up the Webhook Alert
  - 5:45 — Step 5: Paper Trading
  - 6:25 — What Happens Next
  - 7:05 — Get Access
- **Thumbnail text:** "Iron Sight — New Trader Setup Guide"
- **Title (YouTube):** Iron Sight New Trader Onboarding — Setup Guide | S3 Development
- **Description tag:** Iron Sight, TradingView, Signal System, MNQ, TRNQL, Futures, Paper Trading, Project Black-Box
