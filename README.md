# gate io copy trading: what it costs, how to pick a lead trader, and the smallest amount you can start with

Most people searching this want three numbers before anything else: the minimum you can put in, the cut the trader takes out of your profit, and the trading fees you still pay on every fill. Everything else — futures or stocks, one trader or four, how much leverage — matters less than those three.

So here's the short version. On Gate, following someone is free to start. The follower's minimum is set by the lead trader, and it can be as low as 10 USDT. The default profit share on live copy trading is 10%, charged only when your closed PnL over the settlement window is positive. You still pay normal contract or spot fees on every fill. That's the whole cost structure in three sentences.

The rest of this is the detail behind those numbers, plus the parts that trip people up: why your ROI won't match the trader you're copying, and where the real risk sits.

*One naming note, because it confuses people:* Gate.io rebranded to **Gate** and moved to gate.com in May 2025. In the EU you'll still see the Gate.io name on regional entities. Same group, same account system. If you're holding out for a specific "gate.io copy trading" page, you're already on it.

## How copy trading actually works on Gate

The mechanic is simpler than the marketing language around it. When a lead trader adjusts a position, the system calculates a mirrored order for you:

**Your copied order size = copy ratio × the trader's adjustment size**, rounded down. If the result is below the contract's minimum order size, nothing gets copied at all.

Two things determine how big that ends up being. In **smart mode**, the default is proportional by total assets — if the lead trader's total assets are 100 USDT and they put 10 USDT into a position, you put 10% of your total assets in. In **advanced mode** you pick a fixed multiple; set 3x and a 1 BTC position on their side becomes 3 BTC on yours.

One detail people miss: your margin doesn't come from a separate "copy trading wallet." When you start following, funds move from your **spot account into a virtual sub-account** tied to that one trader. When you stop copying, the sub-account is settled, profit share and trading fees are deducted, and what's left returns to spot.

## The copy trading products Gate currently runs

"Copy trading" on Gate isn't one product. There are five paths under that name, and they don't share the same assets, leverage or fee logic. Mixing them up is the most common mistake — a 40% profit share on a private futures setup and a 5% bot split are not comparable numbers.

| Product | What actually gets copied | Profit share | Settlement | Where to start |
| --- | --- | --- | --- | --- |
| **Futures copy trading** | USDT-margined perpetual contract positions, hedge mode | Default 10%, adjustable once per day; up to 30% for expert-level lead traders, higher ceilings in private mode | Daily, only when the follower's PnL for the period is positive | Contract trading → Copy Trading |
| **Spot copy trading** | The lead trader's spot buy/sell actions, alongside their contract activity | Same lead-trader-set structure as live copy | Daily, tied to the live copy cycle | Same copy trading hub |
| **Stock copy trading** | Real US, Hong Kong and Korea stock and ETF positions via licensed brokers, 12,500+ instruments, fractional from 0.01 share | HWM-based: charged only when cumulative net PnL beats the previous high-water mark | Not charged during drawdown recovery | Gate App V8.29.0+ → Copy Trading → Stocks (web version announced as coming soon) |
| **CFD copy trading (TradFi)** | Synthetic CFD exposure on traditional markets, run through MT5 accounts | 20% default, adjustable in a 0%–20% range | Weekly, every Sunday 00:00 (UTC+8), paid out no later than Monday 23:59 | App → Copy Trading → CFD |
| **Bot copy trading** | Another user's trading bot parameters, which become your own bot | Free to copy; 5% of profit goes to the original bot creator when the bot ends | On bot termination | Trading Bots → Bot Square |

If you want to see which lead traders are actually live right now rather than reading about them, 👉 [browse the futures copy trading desk on Gate](https://bit.ly/GateVIP). You can sort by ROI, Sharpe ratio, 7-day performance or copy scale before committing anything.

The stock copy path is the newest and the least obvious. It mirrors genuine share positions rather than derivatives — you're following equity and ETF holdings across three markets, with proportional sizing designed to track the lead's portfolio weights. The trade-off is straightforward: no perpetual-style leverage engine, but also stock market hours instead of 24/7 crypto. Enter through 👉 [Gate's copy trading hub](https://bit.ly/GateVIP) on a recent app build.

## What you actually pay

Three separate costs stack on top of each other, and only one of them is the headline number.

**1. Trading fees.** Every copied order is a real order and pays real fees. Gate's own fee summaries list non-VIP spot starting at 0.1% maker/taker with VIP tiers down to roughly 0.03% maker and 0.045% taker, and futures starting at 0.02% maker / 0.05% taker, down to 0% maker and 0.028% taker at the highest tier. Fees scale with 30-day volume and asset balance. One caveat worth knowing: third-party reviews written at different times cite different starting figures for spot — some say 0.2%. Fee schedules change, so check the current page inside your account rather than trusting any review, including this one.

**2. Profit share.** This only applies to gains, and the trigger differs by product. On live futures copy, the default is 10%, set by the lead trader and adjustable once per day. It's applied against your net profit for the settlement window — if your PnL over that period is negative, no share is taken. The formula is simple: share = net profit × the trader's ratio, rounded down. There's a real cost consideration here. A trader running 30% who averages 8% monthly is worse for you than one running 10% who averages the same, and the ranking tables won't show you that difference.

**3. Funding rates.** Perpetuals charge funding, usually every eight hours. Copied positions are exposed to it exactly like manual ones. During volatile stretches funding can climb well past 0.1% per interval, which over multi-day holds becomes a genuine drag that never appears in a trader's advertised ROI.

> On the private lead trading side, Gate announced on 27 January 2026 that the maximum profit share ratio for private lead trading accounts would be adjusted from up to 99% down to a uniform 40%, effective 2 February 2026. Existing accounts above 40% were auto-adjusted.

## Minimum amounts, for both sides of the trade

For **followers**, the floor is set by each lead trader individually. Gate's own FAQ puts the starting range at 10 USDT, with many traders setting 50, 100 or 300 USDT as their entry point. That's your allocation, not your total account — but remember it's margin, so 10 USDT at 20x is 200 USDT of notional exposure, not 10.

For **lead traders**, the numbers Gate publishes are less consistent. Its help centre states a minimum of 1,000 USDT for lead traders, while the lead trading setup flow references keeping at least 100 USDT of total assets in the futures account to activate. Treat the higher figure as the working number and confirm on the application page.

Becoming a lead trader takes an email on the registered account, agreement to the trader terms, and a review that typically resolves in one to two business days for live copy and around an hour for CFD copy. Two conditions worth flagging before you apply: you can't be following anyone else while your application is pending, and once approved as a lead trader you permanently lose the ability to follow other traders on that account.

## Why your returns won't match the trader's

This is the part the screenshots never explain. Gate's own documentation lists six reasons your PnL diverges from the person you're copying:

- **Different capital.** Copy funds get used up. Once your available copy balance is exhausted, you're technically still following but no longer mirroring new positions.
- **Different entry prices.** If the trader already held a position before you started and then added to it, your average entry cost isn't theirs.
- **Leverage mismatch.** Followers are capped at **20x**. Some lead traders run up to **100x**. You can set your own leverage, and if you do, expect a different result.
- **Copy ratio settings.** Your multiplier is your decision, and it changes outcomes.
- **Slippage and fill timing.** Gates' slippage protection cancels a copied order when the price gap versus the trader's fill is too wide — which protects you but also means partial replication.
- **Shared risk limits.** Large copied orders can hit shared risk limits and fail outright.

The practical implication: don't size your position against the trader's percentage gain. Size it based on the drawdown you can genuinely stomach, then look at whether the return justifies it.

## Risk controls to set before you click copy

Quick copy and advanced copy both let you configure parameters. The order matters more than the settings:

**Stop loss first, then the trader.** Most people do this backwards — they rank traders by ROI, then think about limits. Set your maximum loss per position, your total copy allocation, and your multiplier before you open the leaderboard.

Then filter. Sharpe ratio and maximum drawdown tell you more about consistency than a headline ROI, which can be one lucky week. Look at the return curve over time, not the total. A trader with a red recent segment is in drawdown right now, and the recovery may or may not happen.

Third, spread it. Copying one trader means that trader's worst week is your worst week. Three or four with different styles smooths the curve, though it also means the best performer gets diluted.

Fourth, review weekly. Stop-loss settings exist for the moment you're away from the screen; they don't replace actually looking at what's happening.

Platform-level protections sit underneath your settings — Prometheus leverage limits and net-value drawdown stops on the system side, plus the slippage guard mentioned earlier. Those are safety nets, not a risk framework. They won't stop a position from going against you.

## A few things people ask before signing up

**Do I need to complete KYC?** Copy trading sits behind identity verification on Gate, along with futures, margin and the Startup launchpad. Basic spot trading is available without it, but copying isn't. One regional caveat: Gate does not serve US residents, and access from the US is blocked.

**Is following a trader free?** Yes. There's no subscription, no flat fee, no monthly charge. You pay trading fees on your own fills and the profit share on positive closed PnL. If the trader makes nothing, the profit share is zero.

**Can I stop mid-position?** Yes, you can stop copying at any time. Positions can be closed manually or left to settle depending on your settings, and remaining funds return to your spot account once the sub-account settles. Switching between smart and advanced mode mid-copy is also supported.

**Does copying a lead trader make them stop when they stop?** No. If the original trader terminates their lead trading, you get an app notification and an in-app message — your copied positions do not close automatically. That's yours to manage.

## Where to start

The honest summary: copy trading removes the need to pick entries, not the need to pick a risk level. The numbers on Gate are among the friendlier ones — 10 USDT starting allocations on some traders, 10% default profit share on live copy, no subscription fee — but the leverage available on the futures side (20x for you, up to 100x for the person you're following) is the thing that will decide your outcome far more than any fee.

If you want to look at real lead trader profiles with live performance data before committing anything, 👉 [create your Gate account and open the copy trading desk](https://bit.ly/GateVIP). Set your stop loss first, then pick.
