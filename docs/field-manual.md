# GALACTIC CONQUEST FIELD MANUAL

**Status:** Player-facing source of truth for in-game Help  
**Grounded in:** Live combat engine, server rules, and Doctrine V2 / Recon V3 behavior  
**Audience:** New and veteran commanders — read in ~5 minutes, reference during play  
**In-app:** Commander Record → Admiralty Records → **OPEN MANUAL** (`flutter_app/lib/core/manual/field_manual_content.dart`)

---

## Commander's Brief

**Your objective** is to grow your command: raise **Combat Rating (CR)**, climb **Command Rankings**, secure **Titanium (Ti)**, and build a record of successful strikes and holds.

- **Combat Rating (CR)** is your public skill standing; it sets your **military rank** and, after your first battle, your place on **Command Rankings**. See [Ranks & Promotions](#ranks--promotions).
- **Command Rankings** list commanders with at least one battle, ordered by CR (then wins, then win rate). **Wealth Rankings** order commanders by Ti held — a separate board with no battle requirement.
- **Titanium** is stolen when you **break through** a defense (a strong attack outcome). Failed strikes do not take Ti. Defenders lose Ti only when breached.

You **attack** on your initiative: choose targets, recon when you can, commit fleet and approach allocation, then strike. Defenders set **Defense Command** in advance; they do not react mid-battle.

**STRIKE** and **RECON** charges, plus **AUTO PROTECTION**, are separate from the **12-hour HOSTILE CONTACTS** window — see [Charges](#charges) and [Auto Protection](#auto-protection).

---

## Beginner Combat Guide

### Three steps to win a battle

1. **Recon** — learn doctrine, stance, trap, and lane assessment before you strike.
2. **Identify the prediction** — **Fortress** bets where fleet CP lands; **Counter** bets which hull carries the most CP.
3. **Make the prediction wrong** — shift lanes or hull mix so their doctrine **misses** (missed reads give attackers roughly **20% additional damage** on every hit).

### As a defender

Set **Primary** and **Secondary** stances plus a trap before you are struck. Use **Balanced** when intel is thin; specialize when you expect repeat matchups.

---

## Stances (strategy)

Defenders choose an **Initial Response (Primary)** and **Trap Response (Secondary)**. Only one is active — traps swap Primary for Secondary when fleet shape matches.

### Flat Armor

**The more attacks a fleet generates, the stronger Flat Armor becomes.**

Designed to suppress high-volume fleets and sustained attack pressure. Low-hit capital fleets remain its natural counter.

| | |
|--|--|
| **Identity** | Anti-hit-count defense — answers *“How many attacks is the fleet generating?”* More attacks → stronger armor; fewer attacks → weaker armor |
| **Mechanism** | Fleet Hits = (Frigates×3) + (Cruisers×1) + (Battleships×1). ≤4 → **20%** DR · 5–8 → **30%** · 9–20 → **40%** · 21+ → **50%** |
| **Strong when (defender)** | High hit-count fleets · frigate swarms · sustained volume (e.g. F20_C0_B0, F10_C5_B0) |
| **Weak when (defender)** | Low-hit capital fleets · concentrated burst attacks (e.g. F0_C0_B4) |
| **Attacker playbook** | Prefer low-hit capital lines over frigate swarms |
| **Defender playbook** | Choose when you expect many attacks; protection is reduced vs low-hit battleship fleets |
| **Common mistakes** | Expecting Flat to blunt pure Battleship stacks; feeding high hit-count fleets |
| **Recon notes** | Initial Scan shows Primary; deepen for trap and Secondary |

### Deflector Field

Anti-opener defense — disrupts a small number of powerful attacks.

| | |
|--|--|
| **Role** | Anti-opener defense — disrupts major opening attacks |
| **Strong when** | Attacker relies on Battleships; one decisive opening strike; Deflector active vs capital-heavy fleets |
| **Weak when** | Cruiser-heavy pressure; mixed fleets; sustained follow-up attacks |
| **Attacker playbook** | Confirm Deflector; do not rely entirely on Battleships; cruiser-heavy or mixed; maintain pressure after the opening exchange |
| **Defender playbook** | Disrupt capital-led attacks; pair traps carefully; expect cruiser pressure as the primary counter |
| **Common mistakes** | Believing Battleships counter Deflector; pure Battleship stacks without follow-up |
| **Recon notes** | Wrong stance read loses battles — deepen until confirmed |

### Absorptive Matrix

Frigates are strong against Absorb (~10% damage reduction). Cruisers face ~50%; Battleships are reduced the most (~60%). Pure Battleship stacks are a poor answer — frigate-heavy or mixed fleets usually beat capital-only attacks.

| | |
|--|--|
| **Role** | Anti-ship-class defense — reduces damage through class-based absorption bands |
| **Strong when (defender)** | Frigate-heavy attacker fleets; pure Battleship stacks |
| **Weak when (defender)** | Frigate volume or mixed fleets from the attacker |
| **Attacker playbook** | Confirm Absorb; lean on Frigate volume or a mixed fleet — not pure Battleship stacks |
| **Defender playbook** | Excellent anti-swarm Primary; trap Secondary for capitals |
| **Common mistakes** | Believing Battleships counter Absorb; pure Battleship stacks |
| **Recon notes** | Deepen until stance and trap are confirmed |

---

## Why Recon Wins Wars

1. Identify **stance** — Primary vs what fires after a trap.
2. Identify **doctrine** — Balanced, Counter hull, or Fortress lane.
3. Identify **traps** — fleet shape may swap the active response.
4. **Make the defender wrong:**
   - **Counter — Frigates** → do not lead Frigates
   - **Counter — Cruisers** → do not lead Cruisers
   - **Counter — Battleships** → do not lead Battleships
   - **Fortress** on an approach → pressure elsewhere without making that approach your strongest CP

---

## Common Combat Mistakes

- Using the same fleet against every defense.
- Ignoring traps — scouted stance may not be fought stance.
- Treating **Absorb**, **Flat Armor**, and **Deflector** the same.
- Overcommitting Battleships into **Deflector** without follow-up.
- Believing Battleships counter **Absorb**.
- Assuming bigger ships automatically win.
- Ignoring lane strategy and Fortress reads.
- Picking **Counter** or **Fortress** without intel.
- Leading the hull class they **Counter**.
- Feeding the **Fortress** lane your strongest CP.

---

## Target Search

Open **TARGET SEARCH** on the command rail. Pick a commander to enter **TARGET ACQUIRED**, then **RECON**, **OPEN INTEL REPORT**, or **STRIKE**.

### HOSTILE CONTACTS

- Up to **three** matchmaking commanders per **12-hour** acquisition window — one higher, one near, and one lower **COMBAT RATING**, all inside your CR matchmaking band (**±15%** widening to **±30%** if needed). Example at CR **1500**: **1275–1725** on the first pass.
- **Status:** **AVAILABLE**, **UNDER PROTECTION** (countdown when shown), or **UNAVAILABLE**.
- Cards show military title, **COMBAT RATING**, and **`#12 CALLSIGN`** when ranked; unranked commanders show **CALLSIGN** only.
- Contacts that become protected, undeployed, or invalid are **removed and replaced** without spending **REFRESH**.

### RETALIATION TARGETS

**STRUCK US · LAST 72H** — up to **three** revenge slots, separate from **HOSTILE CONTACTS**. They may sit outside your CR band and may show **UNDER PROTECTION**; **STRIKE** stays blocked until protection ends.

### REFRESH TARGETS

Use **REFRESH TARGETS** up to **twice** per window (see the **REFRESH** counter). An attempt counts only when **new** eligible commanders are found. At most **nine** distinct hostile contacts per window.

### TARGET ACQUIRED

| Control | When |
|--------|------|
| **RECON** | No active report on this target — spends **1** recon charge |
| **OPEN INTEL REPORT** | **RECON REPORT ACTIVE ON THIS TARGET** |
| **STRIKE** | Target **AVAILABLE** and **STRIKE** charges remain |

You may **RECON** or **STRIKE** only commanders on your board, on **RETALIATION TARGETS**, or bound to your active **RECON REPORT**. Protection and deployment are checked again at strike time.

---

## Charges

Shown on the resource strip as **RECON** `n/n` and **STRIKE** `n/n` (pip indicators). **REFRESH** appears on **TARGET SEARCH** only. Timers below do **not** reset the hostile-contact window.

### STRIKE charges

| Step | What you see |
|------|----------------|
| **2/2** → one **STRIKE** | **1/2** — no **NEXT STRIKE** countdown |
| **1/2** → final **STRIKE** | **0/2** — **NEXT STRIKE** on the Bridge (8 hours from empty) |
| Timer completes | **2/2** restored |

Before commit: **STRIKE CHARGES *n* REMAINING**. When empty: **NO STRIKE CHARGES REMAINING · NEXT CHARGES IN …**

### RECON charges

- **4** maximum. Each **RECON** or **CONTINUE RECON** spends **1** charge; **+1** returns **3 hours** later per spend.
- When empty: **NO RECON CHARGES REMAINING · NEXT CHARGES IN …**

---

## Recon Operations

**Intelligence** on the rail opens your active **RECON REPORT**. Recon improves what you see before a strike; it does **not** change ship stats or battle odds.

### Flow

1. **TARGET SEARCH** → **RECON** (1 charge) → **RECON REPORT** on Intelligence.
2. **CONTINUE RECON** — deepen the same report (up to **4** charges total: one **RECON** plus three **CONTINUE RECON**). At cap the UI shows **MAXIMUM DEPTH REACHED**.
3. **PROCEED TO STRIKE** — enter strike commit when the target is verified (**TARGET VERIFIED · STRIKE OPEN**).
4. **DISCARD REPORT** — abandon the report and return to the Bridge. Charges already spent are **not** refunded.

You cannot start a second **RECON** on the same target until you **CONTINUE RECON**, **DISCARD REPORT**, or strike.

### RECON REPORT layout

| Area | Contents |
|------|-----------|
| **LANE ASSESSMENT** | Believed CP per approach (≈ values); visuals are noisier on weaker reads |
| **DEFENSE ASSESSMENT** | **DEFENSE DOCTRINE**, **INITIAL RESPONSE**, **TRAP CONDITION**, **TRAP EFFECT**, **ASSESSMENT CONFIDENCE** |
| **LIKELY STRONGEST APPROACH** | Or **NO SINGLE APPROACH** on a tie |
| Header | **EXPIRES IN** — unused reports drop after **6 hours** |

### Progressive reveal

After the first **RECON**, **DEFENSE DOCTRINE** and **LANE ASSESSMENT** are visible. **INITIAL RESPONSE**, **TRAP CONDITION**, and **TRAP EFFECT** read **FURTHER RECON REQUIRED** until you spend at least one **CONTINUE RECON** on that report.

### ASSESSMENT CONFIDENCE

Single label on the report (strongest read on that report). Steps, weakest to strongest:

1. **LOW CONFIDENCE**
2. **PARTIAL READ**
3. **FIRM READ**
4. **CONFIRMED READ**

Deepening can raise **ASSESSMENT CONFIDENCE**; the report never renders weaker than before on that target.

### Strike without recon

Strike commit with no report shows **NO RECON · STRIKING BLIND**. Striking consumes the active report on that target.

---

## Ship Classes

All hulls use the same combat rules: **command points (CP)**, **hits**, and **damage per hit**. There is no hidden “hull beats armor” table — outcomes depend on **responses**, **doctrine**, **traps**, and **approach allocation**.

| Class | CP | Fire pattern | Total raw damage per hull |
|-------|----|--------------|---------------------------|
| **Frigate** | 1 | 3 hits × 20 | 60 |
| **Cruiser** | 2 | 1 hit × 150 | 150 |
| **Battleship** | 5 | 1 hit × 450 | 450 |

Within each approach, hits resolve in order: **all Frigate hits, then Cruiser, then Battleship**.

### Frigate

- **Role:** Many small hits — volume and follow-up after defenses are stressed.
- **Strengths:** Can wear down **Armor** over many events. **Absorb** softens Frigate attacks the least (~10% reduction). Early Frigate fire can interact with **Deflect** before larger ships shoot in the same approach.
- **Weaknesses:** Poor efficiency vs Armor per CP if Deflect blocks early volleys. Enemy **Counter — Frigates** (when their prediction is correct) cuts Frigate damage sharply.

### Cruiser

- **Role:** Solid single-hit damage per CP.
- **Strengths:** Efficient vs **Armor** (150 minus 15 per hit). Does not alone trigger Deflect **shatter** (threshold is 200+ on one hit).
- **Weaknesses:** One **Deflect** block can negate a Cruiser’s hit in that approach. Vulnerable to **Counter — Cruisers** when the defender’s prediction is correct.

### Battleship

- **Role:** Largest individual attacks in the game.
- **Strengths:** Strong against **low-hit Flat tiers**; efficient 20 CP burst; useful when attack volume stays low.
- **Weaknesses:** **Absorptive Matrix** is specifically tuned to reduce Battleship damage most aggressively (~60% reduction). **Deflector** can neutralize Battleship-led opening attacks. **Counter — Battleships** punishes predictable capital fleets.

### Absorptive Matrix (attacker note)

Frigates are strong against Absorb (~10% reduction). Battleships are reduced the most (~60%) — pure Battleship stacks are a poor answer. Frigate-heavy or mixed fleets usually beat capital-only attacks.

---

## Attack Lanes

Three approaches — **Approach One**, **Approach Two**, **Approach Three** — map to the battle’s three lanes.

### Lane weighting

Approach One counts **most** toward the final result, then Approach Two, then Approach Three (**40% / 35% / 25%**).

### Lane allocation

- **Attackers:** Up to **20 CP** of ships, split across approaches as you choose.
- **Defenders:** **10 CP** of garrison, split across approaches (independent of where you expect the strike).

Each approach fights its own fight: your ships there vs their garrison there, with the same defense responses and doctrine applying everywhere.

### Why lane choice matters

- Weighting means **concentrating fleet CP on Approach One** moves the needle most.
- **Fortress** doctrine rewards predicting which approach carries the **most attacker fleet CP** — not where garrison is heaviest.
- Empty approaches still have outpost defense; you can feint or overload, but unused attack CP does not help elsewhere.

---

## Defense Command

Transmit a full defense before you are safe to be struck: **10 CP** garrison, valid trap responses, and a chosen doctrine.

### Defense Doctrine

| Doctrine | Your prediction | If you are **right** | If you are **wrong** |
|----------|-----------------|----------------------|----------------------|
| **Balanced** | None | No bonus or penalty | No bonus or penalty |
| **Fortress** (pick Approach One, Two, or Three) | They put **most fleet CP** on that approach | Enemy hits on that approach deal **half** damage | **Every** enemy hit deals **~20% more** damage (all approaches) |
| **Counter** (Frigates, Cruisers, or Battleships) | That hull class carries **most fleet CP** | Hits from that hull deal **40%** of normal damage | **Every** enemy hit deals **~20% more** damage (all approaches) |

Ties count: if two approaches tie for most attacker CP, Fortress is correct if you picked either; if two hull types tie for CP, Counter is correct if you picked either.

Doctrine does **not** move garrison CP for you — it only rewards or punishes your **prediction** against what they actually bring.

### Initial Response

Your default stance when **no trap** fires (or no trap is set):

| Response | Effect |
|----------|--------|
| **Armor** | Subtract **15** from each hit (minimum 0) |
| **Deflect** | Battleship strikes above **~200** damage can **shatter** the field — that shatter hit deals **no** damage; **cruiser-heavy and mixed** follow-up is generally the preferred counter |
| **Absorb** | Frigate attacks **~10%** damage reduction; Cruiser **~50%**; Battleship **~60%** — tuned to reduce capital strikes most; mixed fleets are generally the preferred counter |

### Trap Conditions (strategy)

| Condition | Fires when | Attacker counterplay |
|-----------|------------|----------------------|
| **If they bring Battleships** | At least one Battleship in fleet | Recon trap; expect **Secondary** — or strike without Battleships to keep Primary |
| **If they bring no Frigates** | Zero Frigates in fleet | Include Frigates to avoid flip, or plan to beat **Secondary** |
| **No trap** | — | Primary always active |

### Defense Doctrine (why choose)

| Doctrine | Why | When wrong |
|----------|-----|------------|
| **Balanced** | No prediction — safe default | No penalty |
| **Counter** | Punish a leading hull class | ~20% extra damage on all enemy hits |
| **Fortress** | Punish one-lane CP dumps | ~20% extra damage on all enemy hits |

See the **Defense Doctrine** table above for prediction rewards.

### Trap Effects

When a trap fires, **Trap Response** replaces Initial Response for **all approaches** for that battle. Trap and Initial responses **must differ** when a trap is armed.

### Garrison Layout

Assign **10 CP** across the three approaches. More CP on an approach adds **defense strength** there (outpost power plus garrison). It does **not** change doctrine triggers — those use **attacker** fleet CP and hull mix.

---

## Combat Resolution

Battles are deterministic: same fleets, defenses, and rules always produce the same outcome.

### Damage score (GDS)

Each approach produces a **breach share** — how much of that approach’s defense was overcome. The **damage score** combines the three approaches using lane weights (40% / 35% / 25%). Think of it as **overall strike effectiveness**, not a literal hull count.

### Victory conditions

- **Attacker breaks through** if damage score is **above 50%**.
- **Defender holds** if damage score is **50% or below**.

A special scoring adjustment can apply when **Fortress** doctrine **missed** and the enemy still committed meaningful fleet CP to the predicted approach — the reported damage score may lean slightly toward the attacker without changing per-approach damage in the detailed trace.

### Titanium rewards

On a **breakthrough**, you steal Titanium scaled by how far above 50% the damage score rose. On a **hold**, you take **no** Ti. Stolen Ti cannot exceed what the defender had.

### Combat Rating rewards

After battle, both commanders’ ratings shift.

- **You always gain CR when you win** (breakthrough or hold) and **lose CR when you lose** — at least **±1 CR** when the fight was close.
- **How much** you gain or lose still depends on **how decisively you performed** versus what was expected for your matchup (the damage score and opponent strength). A crushing breakthrough earns more than a narrow one; a dominant hold earns more than a squeaker.

Technical detail: [`COMBAT_RATING.md`](./COMBAT_RATING.md).

---

## Ranks & Promotions

Combat Rating (**CR**) determines your military **rank**. After each battle, CR moves up or down based on how the fight went and how strong your opponent was rated. You do not apply for promotion — when your CR crosses the next threshold, your rank updates automatically.

Higher ranks:

- Reflect sustained battlefield performance
- Improve your standing on **Command Rankings**
- Mark progression through the command structure

### Why Combat Rating matters

- Shown on your profile, target cards, and battle results
- Drives **promotion** and **demotion** between ranks
- Sorts **Command Rankings** among commanders with battle history (skill ladder; tie-breakers apply at equal CR)
- Is separate from **Titanium** — wealth does not change your rank

### Rank structure

| Rank | Combat Rating |
|------|----------------|
| Recruit | below 1,200 |
| Cadet | 1,200 – 1,399 |
| Lieutenant | 1,400 – 1,599 |
| Commander | 1,600 – 1,799 |
| Captain | 1,800 – 1,999 |
| Commodore | 2,000 – 2,199 |
| Admiral | 2,200 – 2,399 |
| Grand Admiral | 2,400 – 2,599 |
| Supreme Admiral | 2,600 – 2,799 |
| Galactic Marshal | 2,800 – 2,999 |
| Legend | 3,000 and above |

### How promotions and demotions work

- **Promotion:** Reach the CR minimum for the next rank — your title advances (e.g. Captain → Commodore at 2,000 CR).
- **Demotion:** If CR falls into a lower band, your title can step down (e.g. Commander → Lieutenant).
- **Lieutenant floor:** Once you have **ever** reached Lieutenant (1,400 CR), your **displayed** rank **never shows** Recruit or Cadet again, even if CR dips below 1,400. You can still demote among Lieutenant and higher ranks (e.g. Captain → Commander → Lieutenant).

New commanders begin in the Lieutenant band with CR **1,500** and the Lieutenant display floor already active.

### Promotion progress (Commander Record)

Commander Record shows where you stand on the ladder:

- **Current rank** (visible title)
- **Current Combat Rating**
- **Next promotion** (next rank name)
- **Points required** (CR threshold for that rank)
- **Remaining** CR to the next promotion

Example:

| | |
|--|--|
| Current rank | Captain |
| Combat Rating | 1,870 |
| Next rank | Commodore |
| Required | 2,000 CR |
| Remaining | 130 CR |

Battle reports may also note a rank change when your title moves after a fight.

### Command Rankings and Wealth Rankings

- **Command Rankings** — global standings for commanders who have **completed at least one battle** (a win or a loss on record). Sorted by **Combat Rating** (higher CR ranks higher). When CR ties, **more career wins** rank higher, then **higher win rate**, then earlier commissioning as a tie-break.
- **Wealth Rankings** — sorted by **Titanium** held; economic standing only. Does **not** require a battle — only a valid callsign.
- **Global rank** on Commander Record comes from **Command Rankings**, not Wealth. Shows **—** until you have fought at least one battle.
- **Sector Reach** (Admiralty Records) lists callsigns from your current target board with the same **`#rank CALLSIGN`** prefix when that commander is ranked.

---

## Auto Protection

**AUTO PROTECTION** blocks incoming **STRIKE**s. You can still **RECON** and plan attacks until you commit your own **STRIKE**.

### On the Bridge

When protected, the status strip shows **AUTO PROTECTION** with a countdown. When strikes are recharging, **NEXT STRIKE** shows time until **STRIKE** charges return.

### New commanders

**4 hours** of **AUTO PROTECTION** starting immediately when the account is created.

### After you are struck

**4 hours** from the end of that battle — whether you **held** or were **breached**. On **TARGET SEARCH**, defenders show **UNDER PROTECTION** · **STRIKE BLOCKED** or a countdown until protection opens.

### Your own STRIKE

Committing a **STRIKE** clears **your** **AUTO PROTECTION** immediately (before the battle resolves). Commanders you attack still receive protection after the fight.

### What protection does not block

- The battle that just completed  
- Enemy **RECON** against you  
- **Combat Rating** or **Titanium** changes from that fight  

---

## Commander Record

Your career sheet from the Bridge.

### Statistics

Wins, losses, attacks, defenses, and related totals from your player record (and battle history where aggregated).

### Combat History

A permanent list of engagements: outcome, opponent callsign, Ti and CR deltas when recorded, and whether a **detailed report** is still stored.

### Global Rank

Your place on **Command Rankings** when the leaderboard is available. **Unranked** (**—**) until you have at least one resolved battle (win or loss). Wealth Rank uses the separate Titanium board and its own rules.

### Promotion progress

Current rank, CR, next rank, and CR remaining — see [Ranks & Promotions](#ranks--promotions).

### Leaderboards

Links to **Command** and **Wealth** boards for top commanders and your standing.

---

## Battle Reports

Open **BATTLE REPORT** from the command rail after combat. Detailed traces are kept for your **latest 100** engagements; older fights may be summary only.

### Verdict

- **Attackers:** **WE BROKE THROUGH** or **STRIKE REPELLED**
- **Defenders:** **DEFENSE BREACHED** or **DEFENSE HELD**

### WHY WE WON / WHY WE LOST

Narrative lines from the recorded trace — doctrine, trap, and how the damage score compared to the breakthrough line.

### EXPECTED OUTCOME

- **Attackers:** **LIKELY STRONGEST APPROACH**, **BELIEVED DEFENSE DOCTRINE**, and **CONFIDENCE** (assessment caption + recon charges spent) from the snapshot at strike — or *No recon on file. Blind strike.*
- **Defenders:** **OUR DEFENSE DOCTRINE** and **PREDICTION**

### FORCE ALLOCATION and GARRISON LAYOUT

- **Attackers:** **FORCE ALLOCATION** (your strike) and **ENEMY FORCE COMPOSITION** (their defense)
- **Defenders:** **GARRISON LAYOUT** (your deployment) and **ENEMY FORCE COMPOSITION** (their strike)

### ENGAGEMENT FACTORS

Trap triggered or not, active response, doctrine **CONFIRMED** / **MISSED**, damage score vs the 50% line, deflector shatter, fortress miss assist, and related notes.

### EACH APPROACH

Per-approach strike vs garrison CP, **BREACHED** / **HELD**, and damage share when the trace was recorded.

### RECON CHECK

**Attackers only:** Compare the **RECON REPORT** beliefs at strike time to the truth — doctrine, strongest approach, and **ASSESSMENT CONFIDENCE**.

### CONSEQUENCES

**Titanium** gained or lost, **Combat Rating** movement, and notes such as **AUTO PROTECTION** engaged after defense.

---

# Tactical Notes

- **Approach One** carries the most weight in the damage score — fleet CP there matters most.
- **Wrong Fortress or Counter** gives attackers **~20% additional damage on every hit** — high risk; **Balanced** is the safe default when intel is poor.
- **RECON** raises **ASSESSMENT CONFIDENCE**; it does **not** buff ships or change odds.
- **Fortress** keys off **where attackers put fleet CP**, not where you stacked garrison.
- **Deflect:** Battleship strikes above ~200 damage can shatter the field, but the shattering strike deals **no** damage — cruiser-heavy and mixed fleets are generally the preferred counter.
- **Armor** favors fewer, larger hits; **Absorb** favors **frigate volume** (high leak on small hits); **Deflect** punishes fleets that rely on one decisive opening strike.
- **Traps** punish fleet **shape** (Battleships present, or no Frigates), not lane choice.
- **AUTO PROTECTION** follows every strike you receive; new accounts start shielded — plan **RETALIATION TARGETS** or wait out 4 hours. **Your own STRIKE** drops your shield immediately.

---

*Maintainers: align in-game Help strings with `docs/COMBAT_ENGINE_SPEC.md`, `docs/FIELD_MANUAL.md`, `flutter_app/lib/core/ux/player_combat_copy.dart` (Deflector canonical copy, synced with `apps/combat-simulator/src/lib/player-combat-copy.ts`), `flutter_app/lib/core/ux/tactical_terms.dart`, and recon/doctrine docs when mechanics change.*
