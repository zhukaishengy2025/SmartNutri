# SmartNutri Pet Food Match Report

> Algorithm: v2.0-lite

---

## Report Summary

| Item | Details |
|------|---------|
| **Pet** | Golden Retriever · Male · Neutered · 9 yrs · 28 kg |
| **Food** | Royal Canin Large Breed Adult |

---

## Match Score

```
        ┌─────────┐
        │   32    │
        │  /100   │
        └─────────┘
    Not Recommended 🔴
```

**Rating: Not Recommended (0–39)** — Significant risks or severe nutritional mismatch detected. Strongly recommend switching to a different food.

---

## Six-Dimension Radar

```
              Nutrition 99
                  ╱╲
                ╱    ╲
              ╱        ╲
      Digest 80╱           ╲ Safety 0 ⚠️
              ╱               ╲
             ╱                 ╲
     Joint 0 ╱                   ╲ Palat. 50
       ⚠️   ╲                   ╱
             ╲                 ╱
              ╲               ╱
               ╲             ╱
                ╲           ╱
                  ╲       ╱
                   ╲    ╱
                    ╲╱
              Skin & Coat 45
```

| Dimension | Score | Rating | Weight |
|-----------|-------|--------|--------|
| Nutritional Balance | 99 | Excellent | 17.2% |
| Safety | 0 | Critical ⚠️ | 34.5% |
| Palatability | 50 | Fair | 6.9% |
| Skin & Coat | 45 | Fair | 9.0% |
| Bone & Joint | 0 | Critical ⚠️ | 33.6% |
| Digestive Health | 80 | Excellent | 9.7% |

---

## Risk Alerts

### 🔴 Critical Risk

> **R01 — Allergen Match**
>
> The ingredient list contains "chicken meal" (#3 ingredient) and "chicken fat" (#6 ingredient), both matching the keyword "chicken." Your pet has a confirmed chicken allergy. Consumption may cause itching, vomiting, diarrhea, or other allergic reactions.
>
> **Action: Avoid this food. Choose a formula with zero chicken-derived ingredients.**

### 🟡 Caution

> **Y04 — Senior Dog Without Joint Support**
>
> Your pet is 9 years old (senior stage for large breeds) and has confirmed joint pain, but this food contains no glucosamine, chondroitin sulfate, green-lipped mussel, or any other joint support ingredient. Consider switching to a joint-care formula or adding a joint supplement.

### 🟢 Suggestions

> **G01** — No Omega-3 source (fish oil / flaxseed) detected. Consider supplementing with fish oil for skin health and anti-inflammatory benefits.

> **G02** — No probiotics detected. Consider adding a probiotic supplement to support gut health.

---

## Scoring Details

### Input Data

**Pet Profile:**

| Field | Value | System Inference |
|-------|-------|------------------|
| Species | Dog | — |
| Breed | Golden Retriever | Standard adult weight 25–34 kg → Large breed |
| Age | 9 years (108 months) | Large breed > 7 yrs → **Senior** |
| Weight | 28 kg | Within breed standard |
| Sex | Male | — |
| Neutered | Yes | DER coefficient adjustment |
| Allergies | Chicken | Triggers D2 allergen check |
| Conditions | Arthritis | Triggers D5 weight ×2.5 |

**Food Composition (Dry Matter Basis):**

| Nutrient | As-Fed | DMB | Source |
|----------|--------|-----|--------|
| Crude Protein | 25% | 27.8% | Estimated |
| Crude Fat | 14% | 15.6% | Estimated |
| Crude Fiber | 1.5% | 1.67% | Estimated |
| Moisture | 10% | — | Estimated |
| Carbohydrate (NFE) | 42.5% | 47.2% | Calculated |
| Metabolizable Energy | — | 3,553 kcal/kg | Modified Atwater |

> Guaranteed Analysis values are estimated from publicly available product data, as GA numbers on the label image were not fully legible.

**Ingredient List (Top 13):**
Wheat, duck meal, **chicken meal** 🔴, soybean meal, wheat flour, **chicken fat** 🔴, beef fat, rice, beet pulp, brewer's yeast, soya bean oil, pet food aromas, mineral

**Key Additives:** Zinc sulfate · DL-alpha tocopherol (Vitamin E) · Biotin

**Not Detected:** Fish oil · Flaxseed · Glucosamine · Chondroitin sulfate · Probiotics

---

### D1 — Nutritional Balance: 99

Threshold group: Dog – Senior

| Sub-factor | DMB Value | MIN | MAX | Zone | Score |
|-----------|-----------|-----|-----|------|-------|
| Protein | 27.8% | 25 | 40 | Within MIN–MAX | 100 |
| Fat | 15.6% | 5.5 | 15 | Exceeds MAX by 0.6 → 100−0.6÷15×100 | 96 |
| Carbohydrate | 47.2% | 0 | 50 | Within MIN–MAX | 100 |

**D1 = (100 + 96 + 100) ÷ 3 = 99**

---

### D2 — Safety: 0

| Check | Result | Deduction |
|-------|--------|-----------|
| Chicken allergy × "chicken meal" | ✅ Contains "chicken" | −50 |
| Chicken allergy × "chicken fat" | ✅ Contains "chicken" | −50 |
| Disease contraindication | Arthritis has no dietary restriction | 0 |
| Dangerous additives | None detected (BHA/BHT/ethoxyquin) | 0 |
| Life stage | Senior dog + adult formula → minor mismatch | −5 |

**D2 = max(0, 100 − 50 − 50 − 5) = 0** → Triggers safety veto

---

### D3 — Palatability: 50

| Check | Result | Score |
|-------|--------|-------|
| First ingredient type | Wheat = grain | Base 30 |
| ≥2 named animal sources in top 5? | Duck meal + chicken meal = 2 ✅ | +20 |

**D3 = 30 + 20 = 50**

---

### D4 — Skin & Coat: 45

| Check | Result | Score |
|-------|--------|-------|
| Omega-3 source | No fish oil, no flaxseed | Lookup = 10 |
| Zinc supplement? | ✅ Zinc sulfate | +15 |
| Vitamin E? | ✅ DL-alpha tocopherol | +10 |
| Biotin? | ✅ | +10 |

**D4 = min(100, 10 + 15 + 10 + 10) = 45**

---

### D5 — Bone & Joint: 0

| Check | Result | Score |
|-------|--------|-------|
| Joint support ingredients | No glucosamine, no chondroitin, no green-lipped mussel | Lookup = 0 |
| Fish oil Omega-3 bonus | No fish oil | +0 |

**D5 = min(100, 0 + 0) = 0**

---

### D6 — Digestive Health: 80

| Check | Result | Score |
|-------|--------|-------|
| Fiber 1.67% DMB | Below MIN (2.0%) → 1.67 ÷ 2.0 × 100 | S_fiber = 84 |
| Prebiotic? | ✅ Beet pulp | +25 |
| Probiotic? | ❌ | +0 |
| Gut health component | min(100, 50 + 25) | 75 |

**D6 = (84 + 75) ÷ 2 = 80**

---

### Dynamic Weighting

Active conditions: Food allergy · Joint issue · Senior

| Dimension | Base Weight | Multiplier | After | Normalized |
|-----------|------------|------------|-------|------------|
| D1 Nutrition | 25 | — | 25.00 | **17.2%** |
| D2 Safety | 25 | ×2.0 (allergy) | 50.00 | **34.5%** |
| D3 Palatability | 10 | — | 10.00 | **6.9%** |
| D4 Skin & Coat | 13 | — | 13.00 | **9.0%** |
| D5 Joint | 13 | ×2.5 (joint) × ×1.5 (senior) = ×3.75 | 48.75 | **33.6%** |
| D6 Digestive | 14 | — | 14.00 | **9.7%** |
| Total | | | 145.15 | ≈100% |

---

### Final Score

| Dimension | Weight | Score | Contribution |
|-----------|--------|-------|-------------|
| D1 Nutrition | 17.2% | 99 | 17.0 |
| D2 Safety | 34.5% | 0 | 0 |
| D3 Palatability | 6.9% | 50 | 3.5 |
| D4 Skin & Coat | 9.0% | 45 | 4.1 |
| D5 Joint | 33.6% | 0 | 0 |
| D6 Digestive | 9.7% | 80 | 7.8 |
| **Weighted Total** | | | **32.4** |

**Safety Veto:** D2 = 0 ≤ 30 → Final Score = min(32, 39) = **32**

**Final Rating: Not Recommended 🔴**

---

## Feeding Reference

> The following feeding amounts are for reference only. Given the critical allergen and joint support mismatch, **switching to a different food is strongly recommended.**

| Step | Formula | Result |
|------|---------|--------|
| RER | 70 × 28^0.75 | 852 kcal/day |
| DER Factor (K) | Senior + neutered + low activity (arthritis) | 1.2 |
| DER | 1.2 × 852 | 1,022 kcal/day |
| Daily Amount | 1,022 ÷ 3,553 × 1000 | **288 g/day** |
| Per Meal (2×/day) | 288 ÷ 2 | **144 g/meal** |

---

## Food Switching Recommendations

| Priority | Criteria | Reason |
|----------|----------|--------|
| **Must** | No chicken-derived ingredients (chicken / chicken meal / chicken fat) | Allergen avoidance |
| **Must** | Contains glucosamine + chondroitin sulfate | Joint support for arthritis |
| **Strongly Recommended** | Contains fish oil (salmon oil / anchovy oil) | Anti-inflammatory + skin + joint |
| **Strongly Recommended** | Senior dog formula (Senior / Aging 8+) | Life stage appropriate nutrition |
| **Recommended** | Named animal protein as first ingredient (salmon / duck / lamb) | Better digestibility and palatability |

---

*⚕️ This report is generated by the SmartNutri algorithm engine for reference only and does not constitute veterinary advice. Please consult a licensed veterinarian for health concerns.*

*Algorithm v2.0-lite | AAFCO 2024 · NRC 2006*
