# WR1 Analysis — Predicting the 2025 WR1 (PPR)

Identify a short list of wide receivers most likely to finish **WR1 in 2025** using historical patterns and public NFL data via [`nfl_data_py`].

[![Open In Colab](https://colab.research.google.com/github/bradley-a-mosher/wr1_analysis/blob/main/wr1_analysis.ipynb#scrollTo=0e93a2be)

---

## What is this?

A reproducible notebook that:
- Builds **QB rankings** and **team passing totals** (handles injuries/trades correctly).
- Finds each season’s **WR1 (PPR)** and their **prior-year PPR per game**.
- Checks **draft-team continuity** (still on the team that drafted them).
- Applies a simple, evidence-based profile to list **2025 WR1 candidates**.

**Why it works (historical pattern):**
- WR1s come from **productive passing offenses**.
- They’re usually tied to **top passing QBs/teams**.
- They’re **still on their drafting team**.
- They were already **16+ PPR/G the year before**.
- They’re in their **prime (Years 3–8)**.

---

## Quick Start (Google Colab)

1. Click the **Open in Colab** badge above.  
2. In Colab, go to **Runtime → Run all**.  
3. Scroll to **“2025 WR1 Candidate Shortlist”** for the final table  
   (**Team · WR · 2024 PPR/G**).

> **Note:** On the first run, Colab may install packages and prompt to **Restart runtime**. Accept the restart and **Run all** again—this usually clears any import hiccups.

---

## What the notebook produces

- **QB Seasonal Stats Table:** top QBs by passing yards each year.  
- **Team Passing Offense:** team ranks by total passing yards each season.  
- **WR1 History:** the WR1 (PPR) for the last 10 seasons.  
- **Proof of Context:** WR1s paired with their team pass rank and primary QB rank.  
- **Draft-Team Continuity:** confirms WR1s stayed with their drafting team.  
- **Prior-Year Production:** WR1s were **16+ PPR/G** the year before.  
- **2025 Candidate Shortlist:** applies all filters to reveal likely WR1s.

**Filters used for 2025 shortlist**
- Entering **Years 3–8** in 2025  
- **On drafted team** (by team ID)  
- **≥ 16.0 PPR/G in 2024**  
- **Top-15 passing offense in 2024**

---

## Data & Notes

- Data via **`nfl_data_py`** (weekly + seasonal).  
- Weekly stats use `recent_team` to credit production to the correct team each week.  
- Team IDs normalize franchise code changes (e.g., **OAK/LV**, **STL/LAR**), so joins stay stable.

---

## Troubleshooting (first run)

- **Package install / `nfl_data_py` import error:**  
  In Colab, accept **Restart runtime** if prompted, then **Run all** again.
- **NameError / KeyError right after opening:**  
  You likely didn’t run every cell. Use **Runtime → Run all**.

---

## Repository

- `wr1_analysis.ipynb` — the full analysis and candidate screen.

---

## Credits

- Data plumbing by the **`nfl_data_py`** community.
- Analysis & curation by @bradley-a-mosher.
