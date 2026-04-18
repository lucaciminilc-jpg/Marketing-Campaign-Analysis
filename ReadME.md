# 📊 Global Ads Marketing Campaign Analysis

## 🎯 Project Overview

**Role**: Marketing Analyst  
**Objective**: Analyze global Ads campaigns to identify high-performing channels and optimize budget allocation.

**Tools Used**: Google Sheets  
**Dataset**: Global Ads Performance (Google, Meta, TikTok)  
- 1,800 campaigns  
- €11.1M total ad spend  
- €54.2M total revenue  
- Full year 2024 (Jan 1 - Dec 30)

---

## 🎯 Executive Summary

Analysis of 1,800 marketing campaigns (€11.1M spend, €54.2M revenue) across 4 platforms, 5 industries, 4 campaign types, and 7 countries revealed **critical budget misalignment** and **€22-23M revenue opportunity** through reallocation.

### Top 3 Critical Findings

#### 1. Platform Misalignment (HIGH IMPACT)
- **TikTok Ads** delivers ROAS 7.62 (best) but receives only 24% budget
- **Google Ads** delivers ROAS 3.47 (worst) but receives 57% budget
- **Action**: Shift €2.4M from Google to TikTok
- **Impact**: +€10M annual revenue

#### 2. Geographic Misalignment (MEDIUM IMPACT)
- **USA** is worst market across ALL platforms (Google 2.97, Meta 4.88, TikTok 6.53)
- **Australia/Canada** are top performers (TikTok Australia 8.75, Canada 8.52)
- **Action**: Cut USA -€900k, Scale Australia/Canada +€800k
- **Impact**: +€5M annual revenue

#### 3. Platform Choice > All Other Factors
- TikTok's worst campaign (Shopping 7.56) beats Google's best campaign (Search 3.92)
- Platform variance: 119% | Industry variance: 12% | Campaign Type variance: 16%
- **Action**: Prioritize platform optimization over industry/campaign rebalancing
- **Impact**: +€5.6M through campaign-level precision

### Total Potential Impact

**+€22-23M annual revenue** through budget reallocation:
- Platform reallocation (Google → TikTok): +€10M
- Geographic precision (USA → Australia/Canada): +€5M
- Campaign-level optimization: +€5.6M
- Seasonal timing (Q4 TikTok boost): +€2-3M

**No additional spend required** — pure efficiency gains.

---

## 🧹 Data Cleaning Process

### Issues Identified:
❌ Numeric columns imported as text (apostrophe prefix)  
❌ Revenue column with double decimals (e.g., "4803.43.00")  
❌ Google Sheets auto-converting revenue to duration format  

### Cleaning Steps Applied:

| Issue | Fix | Method |
|-------|-----|--------|
| Numbers as text | Re-imported CSV with auto-convert disabled | Import settings: "Convert text to numbers" unchecked |
| Revenue column | Converted text to numeric values | `=VALUE(SUBSTITUTE(cell;".00";""))` formula |
| Decimal formatting | Standardized to 2 decimals | Format → Number → 2 decimal places |

**Result**: Clean dataset with 1,800 campaigns, all numeric columns ready for analysis.

---

## 📈 Analysis Performed

### 📊 Exploratory Data Analysis

**Dataset Composition**:
- **1,800 campaigns** across 4 platforms, 5 industries, 7 countries, 4 campaign types
- **Date range**: Jan 1 - Dec 30, 2024 (full year)

**Distribution**:
- **Platforms**: Google Ads (40%), Meta Ads (35%), TikTok Ads (25%)
- **Industries**: Balanced distribution (19-21% each)
- **Countries**: Balanced distribution (13-15% each)
- **Campaign Types**: Balanced distribution (23-27% each)

**Note**: TikTok Ads underrepresented (25% vs 40% Google Ads). Sample size (450 campaigns) is sufficient for analysis.

---

## Analysis 1: Platform Performance

### ROAS by Platform

![ROAS by Platform](Images/_ROAS%20by%20Platform.png)

**Key Finding**: TikTok Ads ROAS 7.62 vs Google Ads 3.47

| Platform | ROAS | CTR | CPC | CPA | Budget % |
|----------|------|-----|-----|-----|----------|
| **TikTok Ads** | **7.62** | 5.0% | €1.01 | €29.20 | 24% |
| **Meta Ads** | 5.66 | 2.0% | €1.32 | €39.10 | 19% |
| **Google Ads** | 3.47 | 4.0% | €2.16 | €64.06 | 57% |

### Budget Allocation Misalignment

![Budget vs ROAS](Images/Budget%20Allocation%20vs%20ROAS%20—%20Misalignment.png)

**Critical Problem**: Budget inversely correlated with performance
- Google Ads: 57% budget, ROAS 3.47 (worst)
- TikTok Ads: 24% budget, ROAS 7.62 (best)

**This is backward allocation** — investing heavily in worst performer!

### Recommendations

**1. Reallocate Budget: Shift €2.4M from Google Ads to TikTok Ads**
- Current TikTok: €2.65M × 7.62 = €20.2M revenue
- Proposed TikTok: €5.05M × 7.62 = €38.5M revenue (+€18.3M)
- Reduced Google: €3.95M × 3.47 = €13.7M revenue (-€8.3M)
- **Net gain: +€10M annual revenue**

**2. Google Ads Audit**: Investigate why CPA is 2x higher (€64 vs €29 TikTok)
- Review keyword targeting, landing pages, bidding strategy
- Quality Score analysis
- Conversion funnel optimization

**3. Scale TikTok**: Increase campaigns from 450 to 800+ (currently underutilized)

---

## Analysis 2: Industry Profitability

### ROAS by Industry

![Industry ROAS](Images/ROAS%20by%20Industry%20—%20Balanced%20Performance.png)

### Key Finding: Well-Balanced Performance Across Industries

Unlike platform performance (where TikTok outperformed Google 2:1), industry performance is remarkably balanced:

| Industry | ROAS | Budget % | Total Spend | Total Revenue |
|----------|------|----------|-------------|---------------|
| SaaS | 5.04 | 21.22% | €2,357,562 | €11,891,991 |
| EdTech | 5.03 | 20.68% | €2,296,979 | €11,549,934 |
| E-commerce | 5.01 | 17.32% | €1,923,987 | €9,637,280 |
| Healthcare | 4.84 | 20.33% | €2,258,684 | €10,930,814 |
| Fintech | 4.48 | 20.45% | €2,271,538 | €10,173,311 |

**Comparison with Platform Analysis**:
- **Platform variance**: 4.15 points (TikTok 7.62 vs Google 3.47) — 119% spread
- **Industry variance**: 0.56 points (SaaS 5.04 vs Fintech 4.48) — 12% spread

**Industry is NOT the primary performance driver** — platform choice (TikTok vs Google) has far greater impact on ROI.

### Recommendation: Maintain Current Industry Allocation

Industry budget allocation is **already optimized** with minimal room for improvement.

**Focus optimization efforts on platform mix** (shift Google → TikTok) rather than industry rebalancing.

**Minor adjustment**: Increase E-commerce budget by +2% (+€200k) given strong ROAS (5.01) and current under-investment (17.32%).

---

## Analysis 3: Campaign Type Efficiency

### ROAS by Campaign Type

![Campaign Type ROAS](Images/ROAS%20by%20Campaign%20type%20—%20Balanced%20Performance.png)

### Key Finding: Balanced Performance, Search Slightly Ahead

All campaign types deliver strong ROAS (4.58-5.31 range):

| Campaign Type | ROAS | CTR | CPA | Budget % |
|---------------|------|-----|-----|----------|
| **Search** | **5.31** | 3.94% | €44.30 | 25.82% |
| Display | 4.84 | 3.81% | €45.85 | 23.81% |
| Video | 4.77 | 3.76% | €48.36 | 25.17% |
| Shopping | 4.58 | 3.85% | €48.00 | 25.20% |

**Budget allocation already optimized** — Search (top performer) receives highest share (25.82%).

**Comparison**:
- Campaign Type variance: 0.73 (16% spread)
- Platform variance: 4.15 (119% spread)

**Conclusion**: Campaign Type is NOT a major performance driver compared to Platform choice.

### Recommendation

**Minor adjustment**: Increase Search budget by +2% (25.82% → 28%)
- Source: Reduce Shopping by -2% (25.20% → 23%)
- Expected impact: +€500k revenue

**However**: Focus remains on **platform optimization** (Google → TikTok shift), which yields **20x greater ROI** than campaign type rebalancing.

---

## Analysis 4: Geographic Performance

### ROAS by Country

![Geographic ROAS](Images/ROAS%20by%20country.png)

### Key Finding: India Underinvested, USA Overinvested

| Country | ROAS | Budget % | CPA |
|---------|------|----------|-----|
| **India** | **5.50** | 12.95% | €45.25 |
| Australia | 4.99 | 14.28% | €48.76 |
| Germany | 4.96 | 13.96% | €45.62 |
| UK | 4.95 | 13.93% | €45.81 |
| UAE | 4.92 | 14.54% | €45.29 |
| Canada | 4.79 | 14.79% | €50.32 |
| **USA** | **4.16** | **15.55%** | €45.44 |

### Budget Allocation Misalignment

![Budget vs ROAS Geographic](Images/Budget%20Allocation%20vs%20ROAS.png)

**Budget Misalignment**:
- **India**: ROAS 5.50 (best), receives only 12.95% budget (LOWEST!)
- **USA**: ROAS 4.16 (worst), receives 15.55% budget (HIGHEST!)

India delivers **32% better ROAS** than USA yet receives **2.6% less budget**.

### Recommendations

**1. Rebalance India ↔ USA**:
- Increase India budget: 12.95% → 15.5% (+€283k)
- Decrease USA budget: 15.55% → 13.0% (-€283k)
- **Expected impact**: +€400-600k annual revenue

**2. Investigate USA underperformance** (ROAS 4.16, 24% below average)
- Audit platform mix, audience targeting, campaign quality
- Higher competition/saturation in USA market?

**3. Test India scalability** — gradual budget increase with ROAS monitoring
- Increase +€50k/month for 3 months
- Monitor if ROAS holds >5.0 at scale

---

## Analysis 5: Platform × Campaign Type Matrix

### ROAS Heatmap

![Platform × Campaign Matrix](Images/ROAS%20x%20platform%20x%20campaign%20type.png)

### Key Finding: TikTok Dominates Across ALL Campaign Types

**ROAS Matrix**:

|  | Display | Search | Shopping | Video |
|----------|---------|--------|----------|-------|
| **TikTok** | 8.01 | **8.12** | 7.56 | 7.62 |
| **Meta** | 5.82 | 5.78 | 5.51 | 5.66 |
| **Google** | 3.16 | 3.92 | 3.53 | 3.47 |

**Winning Combination**: TikTok Search (ROAS 8.12)  
**Losing Combination**: Google Display (ROAS 3.16)

### Critical Insight: Platform Choice Matters MORE Than Campaign Type

**TikTok's worst campaign (Shopping 7.56) outperforms Google's best campaign (Search 3.92).**

**Performance variance**:
- **Within-platform variance**: 6-7% (campaign type doesn't matter much)
- **Between-platform variance**: 107% (platform choice is critical!)

**Pattern**: TikTok outperforms Google across ALL campaign types — no campaign type can save Google's poor performance.

### Recommendations

**1. Shift all Search budget**: Google → TikTok
- Google Search (3.92) → TikTok Search (8.12)
- Expected impact: +€3.7M revenue

**2. Cut Google Display entirely**: Reallocate to TikTok Display
- Google Display (3.16) worst overall → TikTok Display (8.01)
- Expected impact: +€1.9M revenue

**3. Maintain Meta Ads**: Consistent mid-tier performance (5.5-5.8) across all types

**Total incremental impact**: +€5.6M revenue through campaign-level reallocation.

---

## Analysis 6: Monthly ROAS Trend (Time Analysis)

### 12-Month ROAS Trend

![Monthly ROAS Trend](Images/ROAS%20per%20Month%20x%20Platform.png)

### Key Finding: TikTok Shows Growth Trend; Q4 Seasonality Identified

**Platform Trends**:

| Platform | Jan ROAS | Nov ROAS (Peak) | YoY Growth | Trend |
|----------|----------|-----------------|------------|-------|
| **TikTok** | 6.61 | **9.12** | +38% | ↗️ Growing |
| Meta | 6.82 | 5.46 | -20% | → Stable |
| Google | 3.45 | 3.24 | -6% | → Flat |

### Seasonality Pattern

**November (Black Friday/Holiday Season)**:

| Platform | Nov ROAS | vs Annual Avg | Seasonal Lift |
|----------|----------|---------------|---------------|
| **TikTok** | **9.12** | 7.62 | **+20%** 🚀 |
| Meta | 5.46 | 5.66 | -4% |
| Google | 3.24 | 3.47 | -7% |

**CRITICAL**: **Only TikTok benefits from Q4 holiday season!**

Google and Meta show **no seasonal lift** (actually decline in November).

### Additional Insights

- **March Peak**: TikTok ROAS 9.03 (Q1 momentum, second-highest month)
- **Google Worst Month**: May ROAS 2.81 (lowest of entire year)
- **Meta February Drop**: ROAS 4.90 (vs 6.82 in January) — potential algorithm change
- **TikTok Volatility**: High variance (6.61-9.12 range) suggests active optimization/testing phase

### Recommendations

**1. Q4 Budget Boost**: Increase TikTok budget +40% in November-December
- Capitalize on 9.12 ROAS peak (+20% vs average)
- Expected impact: +€2-3M revenue through seasonal timing

**2. Reduce Google in Low Months**: Cut Google budget -20% in May
- ROAS 2.81 (worst month)
- Reallocate to TikTok high months

**3. Monitor TikTok Volatility**: Track monthly performance closely
- Volatility = active optimization (positive signal)
- Watch for sustained growth trend continuation

**4. Investigate Meta Feb Drop**: February ROAS 4.90 (vs 6.82 Jan)
- Potential Facebook/Instagram algorithm change
- Review campaign performance Feb vs other months

---

## Analysis 7: Platform × Country Performance Matrix

### Key Finding: USA is Worst Market Across ALL Platforms; Australia Outperforms

**ROAS Matrix**:

|  | Australia | Canada | Germany | India | UAE | UK | USA |
|----------|-----------|--------|---------|-------|-----|-------|-----|
| **Google** | 3.49 | 3.15 | 3.49 | 3.82 | 3.80 | 3.70 | **2.97** |
| **Meta** | 6.52 | 5.27 | 6.56 | 5.85 | 6.03 | 5.12 | 4.88 |
| **TikTok** | **8.75** | 8.52 | 7.10 | 7.80 | 7.06 | 7.61 | 6.53 |

**Best Combination**: TikTok Australia (ROAS 8.75) 🏆  
**Worst Combination**: Google USA (ROAS 2.97) 🔴

### Critical Insights

**1. USA Underperforms Universally**
- **Google USA**: 2.97 (worst overall)
- **Meta USA**: 4.88 (worst Meta market)
- **TikTok USA**: 6.53 (worst TikTok market)

**USA is the lowest-performing market across ALL platforms** — not platform-specific issue but market-level problem.

**2. Australia/Canada = Hidden Opportunities**
- **TikTok Australia**: 8.75 (highest ROAS in entire dataset!)
- **TikTok Canada**: 8.52 (2nd highest)
- Currently **underinvested** (14% budget each)

**3. India Advantage is Platform-Specific**
- **Google India**: 3.82 (best Google country, but still below 4.0)
- **TikTok India**: 7.80 (3rd best, not highest as expected)
- India's overall strong performance (5.50) driven by **low CPC** (€1.52), not superior conversion quality

### Recommendations

**1. Cut USA Budget Aggressively** (-€900k total):
- **Google USA**: -80% (ROAS 2.97 unacceptable)
- **Meta USA**: -30% (ROAS 4.88 below average)
- **TikTok USA**: -20% (ROAS 6.53, lowest TikTok market)

**2. Scale Australia/Canada** (+€800k):
- **TikTok Australia**: +€500k (ROAS 8.75)
- **TikTok Canada**: +€300k (ROAS 8.52)

**3. Investigate USA Market Issues**:
- Universal underperformance suggests **market saturation** or **audience quality issues**
- Consider **exiting USA market for Google entirely** (ROAS 2.97)

**Expected Impact**: +€5M annual revenue through geographic precision allocation.

---

## 💡 Key Insights

### 1. Platform Choice is the Primary Performance Driver

**Evidence across all analyses**:
- Platform variance (119%) >>> Industry variance (12%), Campaign Type variance (16%), Geographic variance (32%)
- TikTok's worst combination (Shopping in USA: 6.53) > Google's best combination (Search in India: 3.92)
- Pattern holds across ALL dimensions: countries, industries, campaign types, months

**Implication**: **WHERE you advertise (platform) matters far more than WHAT you advertise (industry/campaign type) or TO WHOM (geography).**

### 2. Budget Allocation is Inversely Correlated with Performance

**Misalignments identified**:
- **Platform**: Google 57% budget (ROAS 3.47) vs TikTok 24% budget (ROAS 7.62)
- **Geography**: USA 15.55% budget (ROAS 4.16) vs India 12.95% budget (ROAS 5.50)
- **Platform × Country**: Google USA receives high budget (ROAS 2.97) while TikTok Australia underinvested (ROAS 8.75)

**Root cause**: Budget decisions likely based on **historical inertia** (Google = established player) rather than **current performance data**.

### 3. TikTok is in Growth Phase with Seasonal Peaks

**Growth trajectory**:
- YoY growth: +38% (Jan 6.61 → Nov 9.12)
- High volatility (6.61-9.12 range) = active optimization
- Q4 seasonal lift: +20% in November (Black Friday effect)

**Unlike Google/Meta**:
- Google: Flat, no trend (2.81-4.17 stagnant)
- Meta: Stable, no Q4 lift

**Strategic implication**: TikTok performance is **improving over time** while Google stagnates — early-mover advantage opportunity.

---

## 🎯 Overall Recommendations

### Immediate Actions (Next 30 Days)

**Priority 1: Platform Reallocation (HIGH IMPACT)**
- **Cut Google Ads budget by 40%** (-€2.5M)
  - Focus cuts on: Google USA (-80%), Google Display (-100%), Google Shopping (-50%)
- **Increase TikTok Ads budget by 100%** (+€2.5M)
  - Focus on: TikTok Australia/Canada (+€800k), TikTok Search globally (+€1.0M), TikTok India (+€300k)
- **Expected impact**: +€10M revenue

**Priority 2: Geographic Reallocation (MEDIUM IMPACT)**
- **Exit or drastically reduce USA** (-€900k total across all platforms)
  - Google USA: -80% (ROAS 2.97)
  - Meta USA: -30% (ROAS 4.88)
  - TikTok USA: -20% (ROAS 6.53)
- **Scale Australia/Canada** (+€800k)
  - TikTok Australia: +€500k
  - TikTok Canada: +€300k
- **Expected impact**: +€5M revenue

**Priority 3: Campaign-Level Optimization**
- **Cut Google Display entirely** (ROAS 3.16, worst combination)
- **Shift Search budget**: Google Search → TikTok Search
- **Expected impact**: +€5.6M revenue

### Short-Term Actions (Q2 2025)

**1. Google Ads Comprehensive Audit**
- **Investigate USA market failure** (ROAS 2.97)
  - Competitive landscape analysis
  - Audience quality assessment
  - Attribution model validation
- **Review Google India/UAE** (ROAS 3.8)
  - Can these markets be optimized to >4.0?
  - Or better to exit Google entirely?

**2. TikTok Scalability Testing**
- **Gradual budget increase**: +€500k/month for 3 months
- **Monitor ROAS degradation**: Does 7.62 hold at 2x scale?
- **Geography focus**: Australia (8.75), Canada (8.52), India (7.80)

**3. Meta Ads Position Evaluation**
- **Maintain current budget** (consistent 5.5-6.0 performance)
- **Investigate February drop** (4.90 vs 6.82 Jan)
- **Test Meta reallocation**: USA → Australia (6.52 vs 4.88)

### Long-Term Strategic Actions (H2 2025)

**1. Platform Mix Transformation**
- **Target allocation by end 2025**:
  - TikTok Ads: 50% (current 24%)
  - Meta Ads: 35% (current 19%)
  - Google Ads: 15% (current 57%)
- **Total budget**: Same €11.1M (pure reallocation)
- **Expected ROAS improvement**: 4.88 → 6.5 (+33%)

**2. Seasonal Budget Optimization**
- **Q4 TikTok boost**: +40% budget Nov-Dec (ROAS 9.12 peak)
- **Q2-Q3 budget reduction**: -10% in low months
- **Expected impact**: +€2-3M through timing optimization

**3. Market Exit Strategy**
- **Consider full USA exit for Google Ads** (ROAS 2.97 unsustainable)
- **Evaluate India scalability** (can market absorb +€1M spend?)
- **Explore new markets**: Test similar markets to Australia (New Zealand, Singapore)

---

## ⚠️ Limitations & Scope

### Data Limitations

**Missing Data Points**:
- ❌ **Profit margin/COGS** not available → Revenue ROAS only (not Profit ROAS)
- ❌ **Customer Lifetime Value (LTV)** not available → Acquisition metrics only
- ❌ **Multi-touch attribution data** not available → Last-click attribution assumed
- ❌ **Facebook vs Instagram** not separated within Meta Ads platform
- ❌ **Email marketing channel** not present in dataset

### Analysis Scope

**What WAS Analyzed**:
- ✅ Platform, industry, campaign type, geographic performance
- ✅ Budget allocation optimization
- ✅ Time trend analysis (monthly ROAS, seasonality)
- ✅ Cross-segmentation (Platform × Campaign, Platform × Country)
- ✅ Conversion funnel efficiency (CTR, CPC, CPA metrics)

**What was NOT Analyzed**:
- ❌ Individual campaign top/bottom performers
- ❌ Profit margin analysis (revenue ≠ profit)
- ❌ Customer journey mapping (multi-touch attribution)
- ❌ Cohort retention analysis (repeat purchase rates)
- ❌ Competitive benchmarking (industry ROAS standards)

### Recommendations for Future Analysis

**To complete the picture, integrate with**:
1. **CRM data**: Customer LTV, repeat purchase rates, cohort retention
2. **Financial data**: COGS, profit margins by product/industry
3. **Attribution platform**: Multi-touch attribution models
4. **Competitive intelligence**: Industry benchmark ROAS, market share data

---

## 🛠️ Skills Demonstrated

### Technical Skills

**Data Analysis**:
- Data cleaning & transformation (text-to-number conversion, format handling)
- Pivot tables (single dimension, cross-tabulation matrices)
- Calculated metrics (ROAS, Budget %, YoY growth %, conversion rates)
- Cross-segmentation analysis (Platform × Campaign Type, Platform × Country)
- Time series analysis (monthly trends, seasonality identification, YoY comparison)

**Data Visualization**:
- Multiple chart types (bar charts, combo charts, line charts, heatmaps)
- Conditional formatting for pattern identification
- Semantic color coding (green/yellow/red for performance tiers)
- Professional chart design (clear titles, axis labels, data labels)

### Business Skills

**Strategic Analysis**:
- Performance driver identification (Platform > Industry/Campaign/Geography)
- Budget misalignment detection (inverse correlation analysis)
- Opportunity quantification (€22M+ revenue impact calculated)
- Priority-based recommendation framework (Immediate/Short-term/Long-term)

**Communication**:
- Executive-level summary (Top 3 findings, total impact upfront)
- Actionable insights (specific reallocation amounts, expected impacts)
- Visual storytelling (charts support narrative)
- Technical documentation (limitations, scope, methodology transparent)

---

## 📫 Contact

**Luca Cimini**  
Product Operations Specialist

📧 luca.cimini.lc@gmail.com
🔗 [LinkedIn](https://linkedin.com/in/lucacimini)  
📍 Rome, Italy

---

*Analysis completed: April 2026*  
*Tools: Google Sheets*  
*Dataset: 1,800 campaigns | €11.1M spend | €54.2M revenue | Full year 2024*
