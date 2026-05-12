# Exploring Coral Bleaching Risk Using NOAA Coral Reef Watch DHW Data

A reproducible Python/Jupyter analysis of satellite-derived coral thermal stress metrics across five reef systems, using live NOAA Coral Reef Watch (CRW) Degree Heating Weeks (DHW) data.

**Portfolio project page:** [yourdomain.github.io/projects/coral-bleaching-dhw](https://yourdomain.github.io/projects/coral-bleaching-dhw)

---

## Study Sites

| Site | Ocean |
|------|-------|
| Florida Keys, USA | Caribbean/Atlantic |
| Grand Cayman | Caribbean |
| Roatán, Honduras | Caribbean (Mesoamerican Reef) |
| Bonaire | Southern Caribbean |
| Great Barrier Reef (Cairns sector) | Indo-Pacific |

## Key Metrics Analyzed

- **DHW (Degree Heating Weeks)** — accumulated coral thermal stress (°C-weeks)
- **SST Anomaly** — departure from daily climatological SST
- **HotSpot** — SST departure above the Maximum Monthly Mean (bleaching threshold baseline)
- **Bleaching Alert Levels** — NOAA CRW 5-level alert classification

## Data Source

NOAA Coral Reef Watch Version 3.1 Daily 5km Satellite Coral Bleaching Heat Stress Product Suite (CoralTemp). Updated daily. Available at: https://coralreefwatch.noaa.gov/

Data are fetched live via the CRW Virtual Station CSV feed and cached locally in `data/raw/` on first run.

---

## Quickstart

### 1. Clone the repo

```bash
git clone https://github.com/yourusername/coral-bleaching-dhw.git
cd coral-bleaching-dhw
```

### 2. Set up the environment

**Option A: Conda (recommended)**
```bash
conda env create -f environment.yml
conda activate coral-dhw
```

**Option B: Pip**
```bash
pip install -r requirements.txt
```

### 3. Run the notebook

```bash
jupyter notebook coral_bleaching_dhw_analysis.ipynb
```

On first run, the notebook fetches live data from NOAA CRW and caches CSVs to `data/raw/`. Subsequent runs use the cache. To force a refresh: set `force_refresh=True` in Section 3.

### 4. Render the Quarto page (optional)

```bash
quarto render coral-bleaching-dhw.qmd
```

---

## Repository Structure

```
coral-bleaching-dhw/
├── README.md
├── coral_bleaching_dhw_analysis.ipynb   # Main analysis
├── coral-bleaching-dhw.qmd             # Quarto portfolio page
├── references.bib                      # BibTeX citations
│
├── data/
│   ├── raw/                            # Cached CRW CSVs (auto-generated)
│   └── processed/                      # Cleaned/merged outputs
│
├── figures/                            # Saved plots (auto-generated)
│
├── references/                         # Key papers (PDFs)
│   ├── skirving_et_al_2020_coraltemp.pdf
│   └── liu_et_al_2013_crw_decision_support.pdf
│
├── environment.yml
├── requirements.txt
└── .gitignore
```

---

## Key References

1. Skirving, W., et al. (2020). CoralTemp and the Coral Reef Watch Coral Bleaching Heat Stress Product Suite Version 3.1. *Remote Sensing, 12*(23), 3856. https://doi.org/10.3390/rs12233856

2. Liu, G., et al. (2013). NOAA Coral Reef Watch 50 km Satellite SST-Based Decision Support System for Coral Bleaching Management. NOAA Technical Report NESDIS 143.

3. Hughes, T.P., et al. (2017). Global warming and recurrent mass bleaching of corals. *Nature, 543*, 373–377.

---

## License

Code: MIT License  
Data: NOAA CRW data are public domain per NOAA's open data policy.

---

*Part of a marine science and environmental data science portfolio.*  
*Built with Python · Jupyter · Quarto · NOAA Open Data*

