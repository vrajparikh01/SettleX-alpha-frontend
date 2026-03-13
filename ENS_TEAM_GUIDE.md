# SettleX × ENS — Team Demo & Presentation Guide

> **For team members presenting to judges.**
> You don't need to know the code. Just follow each section.
> "SHOW" = where to click. "SAY" = exact words to speak.

---

## The One Sentence (Memorize This)

> *"Most apps use ENS as a display name. We use ENS as a decentralized identity, reputation, and trading preferences layer for peer-to-peer OTC."*

---

## Opening Pitch (Say This First — 30 Seconds)

> *"OTC trading is peer-to-peer. You send thousands of dollars directly to a stranger's wallet. The biggest unsolved problem in DeFi OTC is: who am I actually trading with? SettleX solves this with ENS — not just name resolution, but a full identity system. Every trader's ENS name becomes their trading profile. Their reputation, their social presence, and their token preferences — all stored on Ethereum, zero database, zero signup, completely decentralized."*

---

---

# DEMO STEPS — Follow in Order

---

## DEMO 1 — Trade Cards Show ENS Identity

**SHOW:** Open `/otc` page → Grid view → look at any trade card

**What the card looks like:**
```
┌─────────────────────────────────────────┐
│  [token logo]  500 LAVA                 │
│                $0.028 / LAVA            │
│  ─────────────────────────────────────  │
│  [60%]  [🖼] vraj.eth → [🖼] alice.eth  │
│                             [🛡 85]     │
│               🐦 🔗 💻                  │
│                              [Buy]      │
└─────────────────────────────────────────┘
```

**SAY:**
> *"Every trade card shows the creator and counterparty as ENS names — not wallet addresses. You see 'vraj.eth → alice.eth' with an arrow showing the trade direction. Next to the name is a trust score badge — that green shield with 85 — calculated purely from on-chain ENS data. Below it, tiny social icons: Twitter, GitHub, Discord, Farcaster, Lens — all pulled live from ENS text records on Ethereum mainnet. No centralized profile system anywhere."*

---

## DEMO 2 — ENS Trust Score (Explain the Score)

**SHOW:** Point to the `🛡 85` badge on any card with a score

**SAY:**
> *"This trust score — zero to 100 — is computed entirely from what a trader chose to publish on Ethereum. There is no admin, no KYC, no off-chain database."*

Then read this out loud slowly:

```
ENS name registered  →  30 pts   (they own a real on-chain identity)
Avatar set           →  20 pts   (they care about their presence)
Twitter record       →  15 pts   (public social accountability)
GitHub record        →  15 pts   (developer credibility)
Discord record       →  10 pts   (community member)
Description set      →   5 pts   (completed their profile)
settlex.prefs set    →   5 pts   (verified SettleX trader)
─────────────────────────────────────────────────────────
Maximum              → 100 pts
```

> *"Score 70 or above: Verified Trader — green badge. 40 to 69: Active Trader — blue. Under 40: Basic Profile — gray. Zero: Anonymous — no badge shown at all. In high-value OTC trading, a verified score of 90 is a very different counterparty than an anonymous wallet."*

---

## DEMO 3 — ENS-Only Filter

**SHOW:** `/otc` toolbar → click the **"ENS only"** button (top right area, shield icon)

**What happens:** Some trade cards disappear. Only traders with ENS names remain.

**SAY:**
> *"Traders can choose to only deal with counterparties who have an ENS name — no anonymous wallets. One click. The marketplace resolves every trader address against the ENS registry in real time. This filter literally cannot exist without ENS."*

---

## DEMO 4 — ENS Name Search

**SHOW:** `/otc` search bar → slowly type `alice.eth`

**What happens:**
- Border turns blue and pulses → (resolving)
- Border turns green → (found)
- Cards filter to show only that trader's deals
- Text shows: "Showing trades by alice.eth (0x1234…)"

**SAY:**
> *"You can search the OTC marketplace by ENS name. Type alice.eth, we resolve it on-chain to her address, then show only her trades. The search bar's color tells you the status — pulsing blue means resolving on Ethereum mainnet right now, green means found, red means that ENS name doesn't exist."*

---

## DEMO 5 — Type ENS in the Deal Form (BIGGEST MOMENT)

**SHOW:** `/otc` → click **Buy** on any card → modal opens

In the **"Receiver Address"** field, slowly type: `vitalik.eth`

**Watch what happens step by step:**

```
Step 1 — typing:
  ┌─────────────────────────────────────────┐  [⏳ spinning]
  │  vitalik.eth                            │
  └─────────────────────────────────────────┘
    Resolving ENS name…

Step 2 — ~1 second later:
  ┌─────────────────────────────────────────┐  [✓ green]
  │  vitalik.eth                            │
  └─────────────────────────────────────────┘
    Resolved to: 0xd8dA6BF26…96045

Step 3 — profile appears BELOW the input:
  ┌────────────────────────────────────────────────┐
  │  COUNTERPARTY PROFILE                          │
  │  [🖼] vitalik.eth  ✓  [🛡 Verified · 85]      │
  │       0xd8dA…45                                │
  │  🐦 @VitalikButerin  🔗 vbuterin               │
  │                                                │
  │  ┌──────────────────────────────────────────┐  │
  │  │ 🛡 ENS Trading Preferences               │  │
  │  │  Prefers   [USDC] [WETH]                │  │
  │  │  Deal size  $1,000 – $50,000            │  │
  │  │  Note      "Large deals only"           │  │
  │  │  Set via ENS text record · Ethereum     │  │
  │  └──────────────────────────────────────────┘  │
  │                                                │
  │  On-chain activity                             │
  │  12 deals · 4 fills · ~$4.2K vol              │
  └────────────────────────────────────────────────┘
```

**SAY:**
> *"This is the core demo. You are about to create an OTC deal targeting a specific counterparty — you type their ENS name, and instantly their entire trading profile appears. Their avatar, trust score, verification checkmark, social links."*

Pause. Point to the green box.

> *"But this — this is the innovation. Their ENS trading preferences. Which tokens they want, what deal sizes they accept, a personal note. All of this is stored in a custom ENS text record we invented called `settlex.prefs`. It lives on Ethereum. No database. No API. No backend. Type their name — see their deal terms. Instantly. Decentralized."*

Point to the stats row.

> *"And below that, their on-chain trading history from our platform — how many deals they've created, how many fills, estimated volume. You know exactly who you're trading with before sending a single dollar."*

---

## DEMO 6 — The `settlex.prefs` Record (Most Creative Feature)

**SHOW:** (Open `app.ens.domains` on a second tab if possible, or just explain)

**SAY:**
> *"Let me show you how a trader sets their preferences. On the ENS app, they go to their name, click Edit Records, and add one custom record."*

Show or describe:
```
Key:   settlex.prefs
Value: {"tokens":["USDC","WETH"],"min":"1000","max":"50000","note":"Large deals only"}
```

> *"They hit save, pay the gas, and from that moment — forever — any app that reads ENS can see their preferences. SettleX reads it. But so could Uniswap, Cowswap, any protocol. We created an open standard for OTC trading preferences stored on Ethereum."*

> *"Compare this to how most DeFi apps do it: you sign up, fill a profile form, it goes into a PostgreSQL database owned by the company. They can delete it, sell it, shut down. We store it on Ethereum. The trader owns it."*

---

## DEMO 7 — Confirm Modal: Full Counterparty Identity

**SHOW:** `/otc` → click **Buy** on a trade → the buy confirmation modal

**Look at the right panel — "Seller" section:**

```
┌───────────────────────────────────────────────┐
│  Offer details                                │
│                                               │
│  Seller                                       │
│  [🖼] alice.eth  ✓  [🛡 Verified Trader · 85]│
│       0x1234…5678                             │
│  🐦 @alice  🔗 alice_dev  💬 alice#1234       │
│  ⭐ 3yr veteran    🖼 BAYC holder             │
│                                               │
│  ┌───────────────────────────────────────┐    │
│  │ 🛡 ENS Trading Preferences            │    │
│  │  Prefers  [USDC] [WETH]              │    │
│  │  Deal     $1,000 – $50,000           │    │
│  │  Note     "Fast settlement preferred" │    │
│  │  Set via ENS text record · Ethereum  │    │
│  └───────────────────────────────────────┘    │
│                                               │
│  On-chain activity                            │
│  12 deals · 4 fills · ~$4.2K vol             │
└───────────────────────────────────────────────┘
```

**SAY:**
> *"Before you confirm a trade worth potentially thousands of dollars, this panel shows everything about your counterparty. Name, avatar, trust score. The verification checkmark means we checked both forward and reverse ENS resolution — they actually own this name, they can't spoof it. A veteran badge if their ENS name is over a year old. An NFT avatar badge if they're holding BAYC or CryptoPunks. Their social links. Their trading preferences from that custom ENS record. And their on-chain history."*

> *"This is ENS as the trust layer for peer-to-peer DeFi. All of it decentralized."*

---

## DEMO 8 — Preference Match Highlighting

**SHOW:** Connect a wallet with `settlex.prefs` set. Look at trade cards — some have a green glowing border.

**SAY:**
> *"If you have `settlex.prefs` set on your ENS name, we read your token preferences and highlight every trade that matches. Green glowing border means: this deal matches what you said you want to trade. Your preferences are on Ethereum. The marketplace reads them and personalizes itself. No account settings page, no cookie, no server. Pure ENS."*

---

---

# QUESTIONS JUDGES MAY ASK

**Q: Is `settlex.prefs` just something you made up?**
> *"Yes — and that's the point. ENS text records are open-ended. Anyone can create a custom key. We created `settlex.prefs` as an open standard for OTC preferences. Other DeFi protocols could adopt the same key and read each other's data. It's a composable, permissionless preference layer."*

**Q: What stops someone from faking a high trust score?**
> *"The score is computed from on-chain data — ENS text records and registration — that costs real ETH to set. Setting a fake Twitter record still requires an on-chain transaction. The verification checkmark also checks that forward and reverse resolution both match, which requires controlling the actual ENS name. It's not KYC-level security, but it's meaningfully better than nothing."*

**Q: Why not just use RainbowKit's built-in ENS?**
> *"RainbowKit only shows the name and avatar in the wallet button. We built custom hooks on wagmi v2 + viem v2 directly, which gives us control over all 11 text record keys including our custom `settlex.prefs` key, the reputation score, name age from The Graph subgraph, NFT avatar detection, and all the caching logic. RainbowKit doesn't expose any of that."*

**Q: Does this work for wallets without ENS?**
> *"Yes. Every component has a graceful fallback. No ENS = shortened address displayed, no badge shown, no social icons. The platform works identically — ENS just adds a layer of identity and trust for traders who have it."*

**Q: What chains does this work on?**
> *"ENS itself lives on Ethereum mainnet — that's where all our resolution happens. The actual OTC trades execute on Polygon or Base. Both are configured in our wagmi setup. No chain switching required — the ENS queries go to mainnet automatically, trading goes to the selected L2."*

---

---

# QUICK REFERENCE — ENS Names for Live Demo

Use these during the presentation (all have mainnet profiles):

```
vitalik.eth   → Vitalik Buterin. Has Twitter, GitHub, website, avatar.
nick.eth      → Nick Johnson (ENS founder). Full social profile.
brantly.eth   → Brantly Millegan. Twitter + GitHub.
ricmoo.eth    → Richard Moore (ethers.js author). Developer profile.

To show "ENS not found" red error in EnsInput:
  notreal99999.eth  → not registered → instant red X

For settlex.prefs demo:
  Use a team wallet with settlex.prefs set on app.ens.domains
```

---

# WHAT JUDGES WANT TO HEAR

The prize says: *"swap preferences stored in text records, DEX contracts named via ENS, decentralized interfaces — the most creative application of ENS."*

Hit these exact points in your demo:

| Judge Wants | What SettleX Does | Where to Demo |
|---|---|---|
| Preferences in text records | `settlex.prefs` key with OTC prefs as JSON | Demo 5 + Demo 6 |
| Beyond name resolution | Trust score, veteran badge, NFT avatar, search, filter | Demos 1, 2, 3, 4 |
| Decentralized interface | Zero backend for any identity data | Demo 6 (explain) |
| Real DeFi use case | OTC trust problem solved by ENS | Opening pitch |
| Creative, not forced | Prefs stored on ETH, read cross-platform | Demo 6 |

---

# CLOSING LINE (End Every Demo With This)

> *"ENS is infrastructure. We didn't just put names on wallets — we built a decentralized identity, reputation, and preferences system for OTC traders. Everything you saw: the trust score, the preferences, the social links, the counterparty preview — all of it lives on Ethereum. No database. No company controls it. The trader owns it."*

---

*SettleX × ENS — Built for ETHGlobal Hackathon*
