# SmartNutri Pet Food Match Report

> Algorithm: v2.0-lite

---

## Report Summary

| Item | Details |
|------|---------|
| **Pet** | Golden Retriever · Male · Neutered · 9 yrs · 31 kg |
| **Food** | Premium Grain-Free Formula (No Grain Ingredients · No Meals Added) |

---

## Match Score

```
        ┌─────────┐
        │   84    │
        │  /100   │
        └─────────┘
    Good Match  🟢
```

**Rating: Good Match (75–89)** — Meets most needs with minor room for improvement. A solid choice — review the radar chart for optimization areas.

---

## Six-Dimension Radar

```
              Nutrition 85
                  ╱╲
                ╱····╲
              ╱··      ··╲
    Digest 100··            ·╲ Safety 95
             ·                ·
            ·                  ·
    Joint 70·                  · Palat. 100
            ·                  ·
             ·                ·
              ··            ·╱
                ╲··      ··╱
                  ╲····╱
              Skin & Coat 85
```

| Dimension | Score | Rating | Weight |
|-----------|-------|--------|--------|
| Nutritional Balance | 85 | Good | 18.4% |
| Safety | 95 | Excellent | 18.4% |
| Palatability | 100 | Excellent | 7.4% |
| Skin & Coat | 85 | Good | 9.6% |
| Bone & Joint | 70 | Good | **35.9%** |
| Digestive Health | 100 | Excellent | 10.3% |

---

## Risk Alerts

### 🟡 Caution ×1

> **Y01 — Elevated Fat for Senior Dog**
>
> Fat content is 20.5% (DMB), above the recommended senior dog upper limit of 15%. While this food uses high-quality animal fats, the elevated level may contribute to weight gain in a low-activity senior dog. Monitor body condition closely and adjust portions as needed.

### 🟢 Suggestions ×1

> **Optimization** — Glucosamine is present at 600 mg/kg, but no chondroitin sulfate was detected. For more comprehensive joint support, consider supplementing with chondroitin (~15 mg/kg body weight/day) alongside the glucosamine already provided by the food.

---

## Scoring Details

### Input Data

**Pet Profile:**

| Field | Value | System Inference |
|-------|-------|------------------|
| Species | Dog | — |
| Breed | Golden Retriever | Standard adult weight 25–34 kg → Large breed |
| Age | 9 years (108 months) | Large breed > 7 yrs → **Senior** |
| Weight | 31 kg | Within breed standard |
| Sex | Male | — |
| Neutered | Yes | DER coefficient adjustment |
| Allergies | **None** | No D2 allergen deductions |
| Conditions | Arthritis | Triggers D5 weight ×2.5 |

**Ingredient List (Top 15):**

| # | Ingredient | Category | Notes |
|---|-----------|----------|-------|
| 1 | Chicken | Named fresh meat | ✅ First ingredient = animal protein |
| 2 | Turkey | Named fresh meat | ✅ |
| 3 | Salmon | Named fresh meat | ✅ Omega-3 source |
| 4 | Whole Herring | Named fresh fish | ✅ Omega-3 source |
| 5 | Chicken Liver | Named organ meat | ✅ |
| 6 | Dehydrated Chicken | Named dehydrated protein | ✅ |
| 7 | Dehydrated Turkey | Named dehydrated protein | ✅ |
| 8 | Dehydrated Chicken Liver | Named dehydrated organ | ✅ |
| 9 | Dehydrated Egg | Egg protein | ✅ |
| 10 | Dehydrated Sardine | Named dehydrated fish | ✅ Omega-3 source |
| 11 | Chicken Fat | Named animal fat | |
| 12 | Whole Red Lentils | Legume | |
| 13 | Whole Pinto Beans | Legume | |
| 14 | Whole Navy Beans | Legume | |
| 15 | Whole Green Lentils | Legume | |

**Key functional ingredients detected:**

| Ingredient | Function |
|-----------|----------|
| Pollock Oil | Fish oil → EPA/DHA Omega-3 source |
| Zinc Proteinate | Organic chelated zinc → skin health |
| Vitamin E Supplement | Antioxidant → skin cell protection |
| Dried Chicory Root | Prebiotic (inulin/FOS source) |
| Dried *Bacillus coagulans* | Probiotic (100M CFU/lb) |
| Turmeric | Natural anti-inflammatory |
| Rosemary Extract | Natural preservative / antioxidant |
| Mixed Tocopherols | Natural preservative |

**Not detected:** Chondroitin sulfate · BHA · BHT · Ethoxyquin · Artificial colors

**Guaranteed Analysis:**

| Nutrient | As-Fed | DMB | Source |
|----------|--------|-----|--------|
| Crude Protein (min.) | **38%** | 43.2% | Label |
| Crude Fat (min.) | **18%** | 20.5% | Label |
| Crude Fiber (max.) | **4%** | 4.55% | Label |
| Moisture (max.) | **12%** | — | Label |
| Ash | 8% | 9.1% | Default estimate |
| Carbohydrate (NFE) | 20% | 22.7% | Calculated |
| DHA (min.) | **0.2%** | 0.23% | Label |
| EPA (min.) | **0.2%** | 0.23% | Label |
| Calcium (min.) | **1.2%** | 1.36% | Label |
| Phosphorus (min.) | **1%** | 1.14% | Label |
| Ca:P Ratio | — | 1.19:1 | Calculated (excellent) |
| Vitamin E (min.) | **750 IU/kg** | — | Label |
| Omega-6 (min.) | **3%** | 3.41% | Label |
| Omega-3 (min.) | **0.8%** | 0.91% | Label |
| Omega-6:Omega-3 Ratio | — | 3.75:1 | Calculated (excellent) |
| Glucosamine (min.) | **600 mg/kg** | — | Label |
| Probiotics (min.) | **100M CFU/lb** | — | Label (*B. coagulans*) |
| ME | ~3,560 kcal/kg | — | Modified Atwater est. |

---

### D1 — Nutritional Balance: 85

Threshold group: Dog – Senior

| Sub-factor | DMB Value | MIN | MAX | Calculation | Score |
|-----------|-----------|-----|-----|-------------|-------|
| Protein | 43.2% | 25 | 40 | Exceeds MAX by 3.2 → 100−3.2÷40×100 | **92** |
| Fat | 20.5% | 5.5 | 15 | Exceeds MAX by 5.5 → 100−5.5÷15×100 | **63** |
| Carbohydrate | 22.7% | 0 | 50 | Within MIN–MAX | **100** |

**D1 = (92 + 63 + 100) ÷ 3 = 85**

> Protein at 43.2% DMB is above the senior dog optimal ceiling (40%), earning a slight deduction — very high protein can increase kidney workload in seniors, though healthy kidneys handle this well. Fat at 20.5% DMB significantly exceeds the senior ceiling (15%), the main deduction driver. Carbohydrate at 22.7% is well within limits and low for a kibble — a strength of this grain-free formula.

---

### D2 — Safety: 95

| Check | Result | Deduction |
|-------|--------|-----------|
| Allergen match | No allergies on file | 0 |
| Disease contraindication | Arthritis — no dietary restriction | 0 |
| Dangerous additives | Mixed tocopherols + citric acid (both natural) | 0 |
| Life stage | No explicit "Senior" claim → minor mismatch | −5 |

**D2 = max(0, 100 − 5) = 95**

---

### D3 — Palatability: 100

| Check | Result | Score |
|-------|--------|-------|
| First ingredient type | Chicken = named fresh meat | Base **80** |
| ≥2 named animal sources in top 5? | Chicken, Turkey, Salmon, Whole Herring, Chicken Liver → **5 out of 5** | +**20** |

**D3 = 80 + 20 = 100**

> All five top ingredients are named animal proteins — an exceptionally rare and high-quality composition.

---

### D4 — Skin & Coat: 85

| Check | Result | Score |
|-------|--------|-------|
| Omega-3 source | Pollock oil (fish oil) + salmon + herring + sardine | Lookup = **60** |
| Zinc supplement? | ✅ Zinc proteinate (organic chelated form) | +**15** |
| Vitamin E? | ✅ 750 IU/kg (15× AAFCO minimum) | +**10** |
| Biotin? | Not specifically listed | +0 |

**D4 = min(100, 60 + 15 + 10) = 85**

> Omega-6:Omega-3 ratio of 3.75:1 is excellent (optimal range 5:1–10:1, this is even better). EPA 0.2% + DHA 0.2% provide 0.4% combined long-chain Omega-3, strongly supporting skin barrier function and anti-inflammatory activity.

---

### D5 — Bone & Joint: 70

| Check | Result | Score |
|-------|--------|-------|
| Joint support ingredients | **Glucosamine 600 mg/kg** (listed in GA) — chondroitin sulfate **not detected** | Lookup = **40** (one of the two) |
| Fish oil Omega-3 bonus | ✅ Pollock oil + multiple fish sources | +**30** |

**D5 = min(100, 40 + 30) = 70**

> Glucosamine at 600 mg/kg is a meaningful inclusion. For this 31 kg dog eating ~310 g/day, that delivers ~186 mg glucosamine/day, or ~6 mg/kg BW/day — below therapeutic dose (~20 mg/kg/day) but valuable as maintenance support. The EPA+DHA from fish oils provides clinically relevant anti-inflammatory action (Bauer, 2011). Adding chondroitin sulfate would complete the joint support profile and push D5 toward 100.

---

### D6 — Digestive Health: 100

| Check | Result | Score |
|-------|--------|-------|
| Fiber 4.55% DMB | Within MIN(2.0)–MAX(5.0) optimal range | S_fiber = **100** |
| Prebiotic? | ✅ Dried chicory root (inulin/FOS) | +**25** |
| Probiotic? | ✅ *Bacillus coagulans* 100M CFU/lb | +**25** |
| Gut health component | min(100, 50 + 25 + 25) | **100** |

**D6 = (100 + 100) ÷ 2 = 100**

> Perfect score. Fiber is in the optimal range, chicory root provides prebiotic support, and *Bacillus coagulans* is a well-studied spore-forming probiotic that survives kibble processing and stomach acid. Additionally, turmeric in the formula provides natural anti-inflammatory support for digestive comfort.

---

### Dynamic Weighting

Active conditions: Joint issue · Senior (no allergy)

| Dimension | Base Weight | Multiplier | After | Normalized |
|-----------|------------|------------|-------|------------|
| D1 Nutrition | 25 | — | 25.00 | **18.4%** |
| D2 Safety | 25 | — | 25.00 | **18.4%** |
| D3 Palatability | 10 | — | 10.00 | **7.4%** |
| D4 Skin & Coat | 13 | — | 13.00 | **9.6%** |
| D5 Joint | 13 | ×2.5 (joint) ×1.5 (senior) = ×3.75 | 48.75 | **35.9%** |
| D6 Digestive | 14 | — | 14.00 | **10.3%** |
| Total | | | 135.75 | 100% |

---

### Final Score

| Dimension | Weight | Score | Contribution |
|-----------|--------|-------|-------------|
| D1 Nutrition | 18.4% | 85 | 15.6 |
| D2 Safety | 18.4% | 95 | 17.5 |
| D3 Palatability | 7.4% | 100 | 7.4 |
| D4 Skin & Coat | 9.6% | 85 | 8.2 |
| D5 Joint | 35.9% | 70 | 25.1 |
| D6 Digestive | 10.3% | 100 | 10.3 |
| **Weighted Total** | | | **84.1 ≈ 84** |

**Safety Veto Check:** D2 = 95 > 30 → Not triggered

**Final Rating: Good Match 🟢 (84/100)**

---

## Comparison with Previous Foods Tested

| Dimension | Royal Canin Maxi Adult (52) | High Omega-3 Formula (67) | **This Food (84)** | Improvement Driver |
|-----------|--------------------------|--------------------------|--------------------|--------------------|
| D1 Nutrition | 99 | 99 | **85** | Higher protein/fat exceeds senior ceilings — a trade-off of nutrient density |
| D2 Safety | 95 | 95 | **95** | Consistent — same pet, no allergies |
| D3 Palatability | 50 | 80 | **100** | All top 5 ingredients are named animal proteins |
| D4 Skin & Coat | 45 | 70 | **85** | Fish oil + zinc proteinate + high Vitamin E |
| D5 Joint | 0 | 30 | **70** | Glucosamine 600 mg/kg + fish oil Omega-3 |
| D6 Digestive | 80 | 75 | **100** | Perfect fiber + chicory root prebiotic + *B. coagulans* probiotic |
| **Total** | **52 🟠** | **67 🟡** | **84 🟢** | +32 points over Royal Canin |

> **Key takeaway:** This food scores highest because it addresses the pet's core need — joint support — with both glucosamine AND fish-oil-based Omega-3 anti-inflammatory support. It also excels in palatability and digestive health. The only trade-off is slightly elevated protein and fat for a senior dog, reflected in the D1 score of 85 (vs. 99 for the Royal Canin).

---

## How to Reach 90+ (Excellent Match)

| Current Gap | What Would Fix It | Impact |
|-------------|-------------------|--------|
| D5 = 70 (no chondroitin) | Choose a formula also containing chondroitin sulfate, or supplement with ~465 mg chondroitin/day | D5 → 100, Total → **95** 🟢 |
| D1 = 85 (fat 20.5% > 15% MAX) | Reduce daily portion by ~10% and add a low-calorie topper for volume | Mitigates weight gain risk |

---

## Feeding Reference

| Step | Formula | Result |
|------|---------|--------|
| RER | 70 × 31^0.75 | 921 kcal/day |
| DER Factor (K) | Senior + neutered + low activity (arthritis) | 1.2 |
| DER | 1.2 × 921 | 1,105 kcal/day |
| Daily Amount | 1,105 ÷ 3,560 × 1000 | **310 g/day** |
| Per Meal (2×/day) | 310 ÷ 2 | **155 g/meal** |

> Given the higher caloric density and fat content of this food, precise portioning is especially important for a senior dog. Consider weighing food rather than using cup measurements. Monitor body weight bi-weekly and adjust portions if weight increases.

---

## Summary

This premium grain-free formula is a **Good Match (84/100)** for your 9-year-old Golden Retriever with arthritis. Its strengths are:

- **Joint support (D5=70):** Glucosamine at 600 mg/kg + EPA/DHA from multiple fish sources provide both structural and anti-inflammatory joint support — the highest joint score across all foods tested.
- **Digestive health (D6=100):** Optimal fiber, chicory root prebiotic, and *Bacillus coagulans* probiotic — a perfect digestive profile.
- **Palatability (D3=100):** Five named animal proteins in the first five ingredients — exceptional ingredient quality.
- **Skin & coat (D4=85):** Rich Omega-3 sources + organic zinc + high Vitamin E.

The main consideration is that protein (43.2% DMB) and fat (20.5% DMB) exceed senior dog optimal ceilings. This is typical of high-protein grain-free formulas and is generally safe for dogs with healthy kidneys, but portion control is essential to prevent weight gain.

**One supplement to consider:** Adding chondroitin sulfate (~15 mg/kg/day) would complete the joint support profile and potentially push the score to 95+.

---

*⚕️ This report is generated by the SmartNutri algorithm engine for reference only and does not constitute veterinary advice. Please consult a licensed veterinarian for health concerns.*

*Algorithm v2.0-lite | AAFCO 2024 · NRC 2006*
