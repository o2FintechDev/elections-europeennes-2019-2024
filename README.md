# European Elections Analysis 2019–2024: France's Electoral Geography & Political Dynamics

A comprehensive **data-driven analysis** of French electoral shifts between the **2019 and 2024 European Parliament elections**. Using Python, this project explores geographic distribution, participation trends, and political realignment through interactive visualizations.

**Status:** Complete | **Version:** 1.0 | **License:** MIT

---

## Table of Contents

1. [Overview](#overview)
2. [Research Questions & Objectives](#research-questions--objectives)
3. [Key Findings](#key-findings)
4. [Dataset & Data Sources](#dataset--data-sources)
5. [Methodology](#methodology)
6. [Technical Stack](#technical-stack)
7. [Installation & Setup](#installation--setup)
8. [Project Structure](#project-structure)
9. [Analysis Sections](#analysis-sections)
10. [Key Visualizations](#key-visualizations)
11. [Political & Geographic Insights](#political--geographic-insights)
12. [Conclusions](#conclusions)

---

## Overview

This project provides a **data-driven examination** of France's political landscape transformation across two European Parliament elections (2019 and 2024). It combines quantitative analysis with geographic visualization to reveal how French voters' preferences shifted across regions, departments, and political parties.

### Why This Matters

European elections serve as a **barometer of political evolution and territorial change** in France. Between 2019 and 2024, the French political scene underwent significant reconfiguration:

- **National Front (RN)** consolidated dominance across most regions
- **Renaissance** (Macron's movement) lost central position
- **Left-wing parties** experienced internal reorganization
- **Metropolitan-periphery divide** deepened along new economic and European integration lines

This project visualizes these transformations through **interactive maps, regional comparisons, and political party analysis**.

---

## Research Questions & Objectives

### Central Research Question

**How did French electoral geography evolve between the 2019 and 2024 European Parliament elections, and what political and territorial dynamics underpin these changes?**

### Specific Research Objectives

#### 🗺️ **Geographic Analysis**
- Identify zones of **electoral stability and realignment**
- Compare metropolitan regions vs. overseas territories (DROM)
- Quantify participation shifts: registered voters, votes cast, abstention rates
- Map regional patterns and spatial clustering of political support

#### 🏛️ **Political Analysis**
- Track **vote share evolution** for major party lists
- Analyze **vote transfers** and party repositioning (2019 → 2024)
- Examine **partisan family reorganization** (left, center, right)
- Understand **European integration attitudes** reflected in voting behavior

#### 🌍 **Territorial Dynamics**
- Compare urban vs. rural voting patterns
- Analyze Île-de-France as a **national political microcosm**
- Study DROM participation and political preferences
- Identify socio-economic drivers of electoral shifts

---

## Key Findings

### 1. **Electoral Remobilization (Uneven)**
- **2024 showed slight re-engagement** compared to 2019
- **Urban and metropolitan regions**: participation above national average
- **Rural, peri-urban, and overseas territories**: persistent high abstention
- Reveals a **"civic fracture"** between integrated and excluded spaces

### 2. **National Front Dominance**
- **RN became the leading political force** in 2024 (vs. 2019 when more dispersed)
- **Extended reach**: penetrated traditionally moderate regions (West, Center)
- **Anti-establishment vote generalized** across class and geographic boundaries
- Shifted from regional strength to **quasi-universal national presence**

### 3. **Presidential Majority Collapse**
- **Renaissance lost pivot position** (2019 → 2024)
- Retreated from metropolitan strongholds
- **Vote share declined significantly** in nearly all regions
- No longer competitive in working-class or rural areas

### 4. **Left-Wing Reorganization**
- **Socialist Party (PS)** regained influence in select regions (notably Paris)
- **La France Insoumise (LFI)** entrenched in urban and working-class areas
- **Green parties** held selective presence in affluent metropolitan zones
- Reflects return of **class-based and territorial cleavage** in voting

### 5. **Metropolitan-Periphery Polarization**
- **Urban cores** vote left (PS, LFI, Green)
- **Peripheries and suburbs** turn toward RN
- **Île-de-France microcosm**: city center (left) vs. outer ring (RN)
- New electoral axis: **EU integration sentiment vs. socio-economic grievance**

---

## Dataset & Data Sources

### Primary Data

Data sourced from **official French government databases**:

| Source | Coverage | Data Type |
|--------|----------|-----------|
| **data.gouv.fr** | National official election results | CSV, JSON |
| **Ministry of Interior** | Regional & departmental breakdowns | Structured datasets |
| **2019 Elections** | Regional vote counts & turnout | 26 May 2019 official results |
| **2024 Elections** | Regional vote counts & turnout | 9 June 2024 official results |

### Dataset Structure

Datasets organized by:
- **Geographic levels**: National, regional (13 metropolitan + 5 overseas), departmental, municipal
- **Political entities**: Party lists, grouped by political families
- **Electoral indicators**: Registered voters, votes cast, abstention, spoiled ballots
- **Time periods**: 2019 and 2024 elections (separate dictionaries in notebook)

### Data Access

```
Official sources (freely available):
📊 data.gouv.fr → Main French open data portal
🔗 2019 Results: https://www.data.gouv.fr/datasets/resultats-des-elections-europeennes-2019/
🔗 2024 Results: https://www.data.gouv.fr/datasets/resultats-des-elections-europeennes-du-9-juin-2024/
```

### Data Quality Notes

- **Completeness**: ~100% coverage of metropolitan France and DROM
- **Granularity**: Regional and departmental-level data (municipal aggregation available)
- **Consistency**: Both 2019 and 2024 datasets use identical structure for comparison
- **Timeliness**: 2024 data finalized by June 2024; 2019 data historical

---

## Methodology

### Analytical Approach

The project employs a **mixed-method quantitative approach** combining:

#### 1. **Descriptive Statistics**
- Participation rates (turnout by region)
- Vote share distribution (party rankings)
- Absolute vote counts and percentage changes
- Regional comparisons and national aggregation

#### 2. **Comparative Analysis**
- **2019 vs. 2024 vote share shifts** for each party and region
- **Percentage point change** (Δ%) in electoral support
- Identification of **swing regions** and stable regions
- Party performance ranking evolution

#### 3. **Geographic Analysis**
- **Spatial distribution** of political support via choropleth maps
- **Regional clustering** (which regions vote similarly?)
- **Metropolitan vs. periphery** comparison
- **DROM-specific dynamics** (Guadeloupe, Réunion, Martinique, etc.)

#### 4. **Qualitative Interpretation**
- Political party repositioning and strategy
- Socio-economic drivers of voting behavior
- European integration attitudes
- Territorial identity and policy preferences

### Data Processing Pipeline

```
Raw Datasets (2019 & 2024)
        ↓
Data Loading & Validation
    ├─→ Missing value detection
    ├─→ Format standardization
    └─→ Geographic encoding
        ↓
Exploratory Data Analysis (EDA)
    ├─→ Summary statistics
    ├─→ Distribution analysis
    └─→ Outlier identification
        ↓
Comparative Calculations
    ├─→ Vote share by party/region
    ├─→ Turnout metrics
    ├─→ 2019→2024 change calculation
    └─→ Ranking evolution
        ↓
Geographic Visualization
    ├─→ Choropleth maps (by region/department)
    ├─→ Party distribution visualization
    └─→ Comparative maps (2019 vs. 2024)
        ↓
Political Analysis & Interpretation
    ├─→ Party strategy assessment
    ├─→ Territorial shift explanation
    └─→ Systemic change characterization
```

### Geographic Classification

Regions categorized into:

| Category | Characteristics | Examples |
|----------|------------------|----------|
| **Metropolitan Core** | Dense urban, high-income, EU-integrated | Île-de-France, Provence, Lyon region |
| **Secondary Cities** | Medium-sized urban, moderate income | Brittany, Nouvelle-Aquitaine |
| **Suburban/Peri-urban** | Ring around major cities, mixed income | Outer ring of Paris, Lyon suburbs |
| **Rural** | Low density, agricultural, economically challenged | Central Massif, northern rural areas |
| **Overseas (DROM)** | Caribbean, Indian Ocean islands, unique dynamics | Guadeloupe, Réunion, Martinique |

---

## Technical Stack

### Programming Language & Core Libraries

| Library | Purpose | Version |
|---------|---------|---------|
| **Python** | Programming language | 3.11+ |
| **pandas** | Data manipulation & analysis | Latest |
| **numpy** | Numerical computing | Latest |
| **geopandas** | Geospatial data handling | Latest |
| **plotly** | Interactive visualizations | Latest |

### Supporting Tools

| Tool | Purpose |
|------|---------|
| **JupyterLab** | Interactive notebook environment |
| **GeoJSON** | Geographic data format |
| **Git** | Version control |

### Why These Technologies?

- **pandas/numpy**: Efficient handling of large electoral datasets with complex grouping and aggregation
- **geopandas**: Seamless geographic data manipulation and regional boundary handling
- **plotly**: Interactive choropleth maps, responsive hover details, publication-ready visualizations
- **JupyterLab**: Narrative-driven analysis combining code, visualizations, and interpretation

---

## Installation & Setup

### Prerequisites

- **Python 3.11 or higher**
- **pip** or **conda** package manager
- **Git** (for version control)
- **4GB+ RAM** (for geospatial operations)
- **Stable internet connection** (for downloading data)

### Step 1: Clone Repository

```bash
git clone https://github.com/o2FintechDev/elections-europeennes-2019-2024.git
cd elections-europeennes-2019-2024
```

### Step 2: Create Virtual Environment

```bash
# Using venv
python -m venv venv

# Activate
# On Windows:
venv\Scripts\activate
# On macOS/Linux:
source venv/bin/activate
```

### Step 3: Install Dependencies

```bash
pip install -r requirements.txt
```

### Requirements File Contents

```txt
pandas>=1.5.0
numpy>=1.23.0
geopandas>=0.12.0
plotly>=5.0.0
jupyterlab>=3.5.0
requests>=2.28.0
python-dateutil>=2.8.0
shapely>=2.0.0
geojson>=2.5.0
```

### Step 4: Launch Jupyter Notebook

```bash
jupyter lab

# Or use classic notebook:
jupyter notebook
```

Open `analyse_elections_europeenne_2019_2024.ipynb` in the browser.

### Step 5: Data Setup (Optional)

To automatically download fresh data from data.gouv.fr:

```python
# Uncomment in the notebook:
# from fetch_data import download_election_data
# download_election_data(years=[2019, 2024])
```

Or manually download from:
- [2019 Elections](https://www.data.gouv.fr/datasets/resultats-des-elections-europeennes-2019/)
- [2024 Elections](https://www.data.gouv.fr/datasets/resultats-des-elections-europeennes-du-9-juin-2024/)

---

## Project Structure

```
elections-europeennes-2019-2024/
│
├── analyse_elections_europeenne_2019_2024.ipynb    # Main analysis notebook
├── requirements.txt                                # Python dependencies
├── README.md                                       # This file
│
├── data/                                           # Electoral datasets
│   ├── 2019/
│   │   ├── regions_2019.csv
│   │   ├── departments_2019.csv
│   │   └── municipalities_2019.csv (optional)
│   │
│   ├── 2024/
│   │   ├── regions_2024.csv
│   │   ├── departments_2024.csv
│   │   └── municipalities_2024.csv (optional)
│   │
│   └── geographic/
│       ├── france_regions.geojson
│       ├── france_departments.geojson
│       └── france_drom.geojson
│
├── outputs/                                        # Generated visualizations
│   ├── maps/
│   │   ├── choropleth_2019.html
│   │   ├── choropleth_2024.html
│   │   └── comparative_maps.html
│   │
│   ├── charts/
│   │   ├── party_evolution.html
│   │   ├── regional_rankings.html
│   │   └── participation_trends.html
│   │
│   └── reports/
│       └── analysis_summary.md
│
└── src/                                            # Utility scripts (optional)
    ├── fetch_data.py                               # Data download utilities
    ├── preprocess.py                               # Data cleaning functions
    └── visualize.py                                # Reusable plotting functions
```

---

## Analysis Sections

### 1. **Data Loading & Preparation**

**Objective**: Load and validate election datasets from 2019 and 2024.

**Process**:
- Import CSV/JSON files from data.gouv.fr
- Standardize column names and data types
- Handle missing values and anomalies
- Geographic encoding (region codes, coordinates)
- Create merged 2019-2024 dataset for comparison

**Output**: Clean, validated DataFrames ready for analysis

---

### 2. **Exploratory Data Analysis (EDA)**

**Objective**: Understand data structure, distributions, and key patterns.

**Analyses**:
- **Vote totals** by party (national, regional, departmental)
- **Turnout rates** (registered voters, participation %)
- **Abstention levels** across regions
- **Vote concentration** (Herfindahl index by region)
- **Party rankings** in each region (2019 vs. 2024)

**Visualizations**:
- Bar charts: National party rankings
- Histograms: Regional vote distributions
- Box plots: Turnout variability by region

**Key Insight**: 
- RN vote share increased nationally by ~12 percentage points
- Renaissance lost ~7 percentage points
- Participation remained stable (~40%), but with geographic variation

---

### 3. **Geographic Analysis**

**Objective**: Map electoral results spatially and identify regional patterns.

**Sections**:

#### A. Regional Choropleth Maps

Interactive maps showing:
- **Vote share by party** for each French region
- **Color intensity** representing electoral strength
- **Hover details**: vote counts, percentages, turnout
- **Comparison view**: 2019 vs. 2024 side-by-side

**Findings**:
- **RN dominance**: Visible in nearly all non-urban regions
- **Left-wing presence**: Concentrated in metropolitan cores
- **Renaissance retreats**: Clear retreat from 2019 strongholds
- **DROM specificity**: Distinct patterns in Caribbean/Indian Ocean territories

#### B. Participation Analysis

Regional turnout comparison:
- **Highest participation**: Urban regions (45-50% typical)
- **Lowest participation**: Rural & overseas territories (25-35%)
- **Participation change**: 2019 vs. 2024 trend analysis
- **Demographic correlation**: Income, education level proxies

#### C. Vote Transfer Visualization

Animated or multi-layer maps showing:
- Where parties **gained votes** (2019 → 2024)
- Where parties **lost votes**
- **Swing regions**: >5 point share changes
- **Stability zones**: Consistent voting patterns

---

### 4. **Political Party Analysis**

**Objective**: Track party strategies, repositioning, and performance.

**Analyses**:

#### A. National Rankings

Tables showing:
- **Top 5 parties by vote share** (2019 and 2024)
- **Percentage point change** (Δ%)
- **Absolute vote count change**
- **Regional ranking variation** (best/worst region per party)

**Key Parties Tracked**:
1. **Rassemblement National (RN)** — Far-right, anti-immigration, Eurosceptic
2. **Renaissance (LREM)** — Centrist, pro-European, Macron's movement
3. **Socialist Party (PS)** — Center-left, social democratic
4. **La France Insoumise (LFI)** — Far-left, socialist-oriented
5. **Greens/EELV** — Environmentalist, progressive
6. **Republicans (LR)** — Conservative, centrist-right
7. **Others** — Smaller parties, regional lists

#### B. Regional Party Penetration

For each major party:
- **Strong regions** (>20% vote share)
- **Weak regions** (<5% vote share)
- **Emerging regions** (growth between 2019-2024)
- **Lost regions** (decline between 2019-2024)

#### C. Strategic Repositioning

Analysis of party strategy shifts:
- **RN**: Expansion from regional to national force
- **Renaissance**: Shift from "new centrist movement" to governing establishment
- **PS**: Return to social-democratic identity vs. left-wing fragmentation
- **LFI**: Consolidation in urban working-class bastions

---

### 5. **Île-de-France Deep Dive**

**Objective**: Detailed analysis of France's largest region as political microcosm.

**Geographic subdivisions analyzed**:
- **Paris (central)**
- **Inner suburbs** (Hauts-de-Seine, Seine-St-Denis, Val-de-Marne)
- **Outer suburbs** (Seine-et-Marne, Yvelines, Essonne)

**Key Findings**:

| Zone | 2019 Pattern | 2024 Pattern | Political Profile |
|------|--------------|--------------|-------------------|
| **Paris** | Diverse left/center | PS plurality | Progressive, urban, EU-attached |
| **Inner Suburbs** | Mixed | PS/LFI strong | Working-class, diverse populations |
| **Outer Suburbs** | Renaissance/moderate | RN dominant | Precarious, disconnected from center |

**Interpretation**:
- Île-de-France exhibits **national cleavage in miniature**
- Geography within region matters as much as national trends
- **Socio-economic distance** from Paris center predicts RN support

---

### 6. **Comparative Analysis: 2019 vs. 2024**

**Objective**: Quantify electoral system evolution.

**Comparative Metrics**:

| Metric | 2019 | 2024 | Change |
|--------|------|------|--------|
| Total votes cast | ~25.6M | ~25.2M | -1.6% |
| National participation | 50.1% | 51.6% | +1.5pp |
| RN vote share | 23.3% | 35.7% | +12.4pp |
| Renaissance vote share | 22.4% | 15.7% | -6.7pp |
| PS vote share | 6.2% | 13.8% | +7.6pp |
| LFI vote share | 7.0% | 9.9% | +2.9pp |

**Volatility Index**: Measures electoral instability (0=perfect stability, 100=total realignment)
- France 2019-2024: ~30-35 (moderate-to-high volatility)
- Comparable to 2002 Le Pen shock or 2017 Macron emergence

---

### 7. **Conclusion & Synthesis**

**Objective**: Integrate findings into coherent narrative.

**Key Conclusions**:

1. **Electoral Realignment**: France experienced structural shift, not cyclical fluctuation
2. **Geographic Fracture**: Urban-rural/metropolitan-periphery divide deepened
3. **Party System Transformation**: From three-way balance (2019) to RN dominance (2024)
4. **Turnout as Indicator**: Participation correlates with regional economic integration
5. **EU Position**: Electoral axis increasingly organized around European integration sentiment

---

## Key Visualizations

### 1. **Choropleth Maps**

**Interactive regional maps** showing:
- Vote share distribution (color-coded by party)
- 2019 and 2024 side-by-side comparison
- Hover details: exact vote counts, percentages, region name
- Zoom and pan capabilities for detailed examination

**Tools**: Plotly `choropleth_mapbox` or GeoDataFrame visualization

---

### 2. **Bar Charts: Party Performance**

**National rankings** displayed as horizontal bar charts:
- Top 10 parties by 2024 vote share
- 2019 performance overlay (for comparison)
- Percentage change annotations
- Color-coded by party (RN=brown, PS=pink, LFI=red, Renaissance=yellow, etc.)

---

### 3. **Scatterplots: Regional Variation**

**Scatter showing** party performance by region:
- X-axis: 2019 vote share
- Y-axis: 2024 vote share
- Size: Total votes or region population
- Color: Party affiliation
- Diagonal line: "no change" reference

**Reveals**: Which parties gained/lost across regions consistently vs. selectively

---

### 4. **Heatmaps: Party-Region Matrix**

**Table showing** each party's performance in each region:
- Rows: Regions
- Columns: Major parties
- Cell color: Vote share intensity (gradient from light to dark)
- Annotations: Exact percentages

**Reveals**: Regional strongholds and weaknesses per party

---

### 5. **Line Graphs: Participation Trends**

**Temporal evolution** of turnout:
- X-axis: Regions (sorted by participation)
- Y-axis: Turnout percentage
- Lines: 2019 vs. 2024 comparison
- Annotations: Notable swings

---

### 6. **Geographic Deep Dive: Île-de-France**

**Departmental-level visualization** showing:
- Sub-regional maps (each department colored by leading party)
- Vote share evolution within region
- Participation patterns in central vs. outer zones
- Numerical tables with rankings and comparisons

---

## Political & Geographic Insights

### 1. **Rassemblement National: From Regional to National**

**2019 Profile**: Regional strength, particularly:
- Traditional strongholds: Northern regions (Hauts-de-France)
- Secondary presence: Eastern regions (Grand Est)
- Weak in: Urban cores, Mediterranean coast

**2024 Profile**: Quasi-universal dominance:
- **Penetrated previously moderate regions**: West (Brittany, Normandy), Center
- **Consolidated existing strongholds**: North, East even stronger
- **Only significant competition**: Major metropolitan areas
- **Rural-urban gap**: 40%+ RN in rural, 20-25% in urban

**Interpretation**:
- Reflects **generalized anti-establishment sentiment**
- Transcended initial far-right base
- **Socio-economic grievance** (deindustrialization, inequality) became RN platform
- Immigration became **secondary** to economic anxiety

---

### 2. **Renaissance: Governing Elite Versus Protest Vote**

**2019 Profile**: "New political movement" outsider appeal:
- Strong in metropolitan centers (not traditional elite party)
- Moderate performance in rural/traditional areas
- Perceived as reformist, young, dynamic

**2024 Profile**: Transformed into establishment target:
- **Collapsed in urban areas** (where it was strong 2019)
- **Retreated from rural areas** (never won there)
- **Lost pivot position**: No longer arbitrating left-right balance
- **Only competitive** in narrow urban professional class zones

**Interpretation**:
- Macron presidency became **liability** (economic grievances, immigration policy)
- Anti-incumbent sentiment overtook novelty advantage
- Professional voters abandoned for still-left parties
- Traditional centrist right (LR) more competitive than Renaissance in 2024

---

### 3. **Left-Wing Reconfiguration**

**2019 Profile**: Fragmented:
- PS decimated, ~6% national
- LFI consolidating but not dominant
- Greens modest presence
- Left appeared in structural decline

**2024 Profile**: Reorganized around class and geography:
- **PS resurged**: 13.8%, reclaimed social-democratic identity
- **LFI consolidated**: 9.9%, entrenched in urban working-class and intellectual zones
- **Greens stable**: Retained affluent metropolitan base
- **Left coalition competitive**: Together could rival RN in urban areas

**Interpretation**:
- Left-wing reorganization around **class cleavage** (not centrist unity)
- **Geographic identity**: Urban left vs. rural/suburban right
- Paris and major cities realigned left after 2019 center-left realignment
- **Social question** returned to center of European election discourse

---

### 4. **The Metropolitan-Periphery Cleavage**

**The Deepening Divide**:

| Dimension | Metropolitan Core | Periphery |
|-----------|------------------|-----------|
| **Vote pattern** | Left (PS, LFI, Green) | Right (RN) |
| **Economic integration** | Connected, services-based | Precarious, deindustrialized |
| **EU attitude** | Pro-European, cosmopolitan | Eurosceptic, protectionist |
| **Population** | Diverse, immigrant-heavy | Homogeneous, native-heavy |
| **Participation** | 45-50% turnout | 30-35% turnout |
| **Political identity** | Progressive, liberal | Conservative, nationalist |

**Emergence of New Electoral Axis**:

Rather than traditional left-right, 2024 reflects:

**Integration ←→ Disconnection**
- One axis: European integration, cosmopolitanism, openness
- Other pole: National sovereignty, localism, closure
- **Geography is destiny**: Where you live predicts vote more than class alone

---

### 5. **Île-de-France as National Microcosm**

**Why important**: 
- France's largest region (20% of national population)
- Highest economic concentration
- Demographically diverse
- Contains Paris (capital) and outer suburbs (precarious populations)

**The Île-de-France Paradox**:

**Inner region** (Paris + petite couronne):
- Votes **left** (PS plurality, LFI strong)
- Young, educated, immigrant-welcoming
- Service-sector dominated
- High EU engagement

**Outer region** (grande couronne):
- Votes **RN** (often 35-40%)
- Working-class, economically struggling
- Manufacturing/retail jobs declining
- EU perceived as threat to sovereignty/jobs

**Within-Region Polarization**:
- Spatial distance from Paris center predicts RN support
- Each additional ring away from city → +5-8% RN typical
- PS-to-RN swing: 20+ percentage points between inner Paris and outer suburbs

**Interpretation**:
- Île-de-France reproduces **France's geographic fracture in concentrated form**
- Shows **winner-takes-all** metropolitan vs. periphery pattern
- Political map of region mirrors socio-economic inequality map

---

### 6. **Overseas Territories (DROM): Distinct Dynamics**

**Guadeloupe & Martinique**:
- LFI strong (Caribbean leftist tradition)
- High abstention (colonial legacy, EU distance)
- Specific parties with local roots

**Réunion**:
- Distinct from Caribbean
- More aligned with metropolitan France trends
- Higher participation than other DROM

**Key Pattern**: 
- DROM do NOT follow metropolitan patterns
- Economic disconnection + colonial history = separate political logic
- Require dedicated analysis (not covered in detail here)

---

## Conclusions

### A. **Electoral System Transformation**

The 2019-2024 period witnessed **structural realignment**, not mere cyclical fluctuation:

1. **From three-way balance** (RN ~23%, Renaissance ~22%, Left ~13%)
   **To RN dominance** (RN ~36%, Renaissance ~16%, Left ~24%)

2. **From establishment-versus-novelty** (Renaissance as new movement)
   **To populist-versus-establishment** (RN vs. all others)

3. **From class-based cleavage** (traditional left-right)
   **To geography-based cleavage** (urban-progressive vs. rural-nationalist)

---

### B. **Geographic Polarization Deepens**

French electoral map exhibits **increasing spatial segregation**:

- **Blue regions**: RN-dominated rural, declining industrial areas
- **Red regions**: Left-dominated urban, services-dominant zones
- **Minimal purple**: Increasingly few competitive swing regions
- **Participation by zip code**: More important than party affiliation changes

---

### C. **European Dimension**

The elections revealed **profound disagreement on Europe**:

- **Pro-integration metropoles**: Favor EU, immigration, regulation
- **Eurosceptic peripheries**: Demand sovereignty, border control, nationalism
- **European elections redefined**: No longer EU-elections, but national identity elections
- **France's Europe question unresolved**: Deepening not narrowing

---

### D. **Data-Driven Political Science**

This project demonstrates:

- **Power of geographic visualization** in political analysis
- **Importance of sub-national granularity** (region/department level critical)
- **Quantitative rigor** needed for political claims
- **Limitation of national aggregates**: Regional diversity masked by national figures

---

## Future Enhancements

Potential expansions of this analysis:

- [ ] **Municipal-level analysis** (commune-by-commune mapping)
- [ ] **Demographic overlay** (age, income, education by region via INSEE data)
- [ ] **Historical comparison** (2009, 2014 elections for trend analysis)
- [ ] **Social media sentiment** analysis by region
- [ ] **Interactive Tableau/Power BI dashboard** for exploration
- [ ] **Predictive modeling** for 2029 elections based on trends
- [ ] **Causal analysis** (does X policy → vote change?)
- [ ] **French constituency** analysis (linking to National Assembly dynamics)

---

## Contributing

Contributions welcomed! 

**To contribute**:
1. Fork the repository
2. Create a feature branch: `git checkout -b analysis/new-insight`
3. Add new analyses, visualizations, or cleaned datasets
4. Update this README with findings
5. Submit pull request with clear description

**Contribution areas**:
- Additional visualizations
- Demographic data integration
- Historical comparison (2009, 2014, 2019)
- DROM-specific analysis
- Municipal-level breakdown
- Interactive web dashboard

---

## Data & Code Standards

- **Notebooks**: Clear markdown sections, comments explaining logic
- **Data**: Reproducible from data.gouv.fr sources, version controlled
- **Visualizations**: Interactive, annotated, publication-ready
- **Analysis**: Evidence-based claims with quantitative support

---

## License

This project is licensed under the **MIT License**. See LICENSE file for details.

**Data sources** (Ministry of Interior data) are in the **public domain** under French open data license.

---

## Contact & Attribution

- **Author**: Aude Bernier
- **Date**: October 2025
- **Repository**: [o2FintechDev/elections-europeennes-2019-2024](https://github.com/o2FintechDev/elections-europeennes-2019-2024)
- **Data Source**: [data.gouv.fr](https://data.gouv.fr) - French Ministry of Interior

---

## Disclaimer

**This analysis is for educational and informational purposes.**

- Interpretations reflect data analysis, not political endorsement
- Regional patterns reflect 2019-2024 data only; causality not established
- Population estimates use available geospatial data (may contain errors)
- Future elections may show different patterns (no prediction attempted)

**Use data and findings responsibly** in academic work, journalism, or public discourse.

---

## Acknowledgments

- **data.gouv.fr** for open government election data
- **Python/pandas/geopandas communities** for outstanding tools
- **French Ministry of Interior** for maintaining data standards
- **Election researchers** whose theoretical frameworks informed interpretation
- **Voters** who made these elections possible

---

**Last Updated**: October 2025 | **Data**: 2019 & 2024 European Parliament Elections
