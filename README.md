# AI Exposure by Occupation

Interactive visualization tool that shows how exposed different occupations are to AI automation.

## Live Demo

Visit: `https://germanjreyes.github.io/occ_exposure_demo/`

## How It Works

Users search for their intended occupation and see where it falls on an AI exposure scale (1 = most exposed, 100 = least exposed). Five visualization styles are available:

- **Tiered Steps** – Categorical view with exposure tiers
- **Gradient Bar** – Simple horizontal scale
- **Gauge** – Speedometer-style display
- **Distribution** – Position relative to all occupations
- **Minimal Card** – Clean summary card

## Files

| File | Description |
|------|-------------|
| `index.html` | Main application (self-contained) |
| `occupations.csv` | Occupation data with exposure rankings |

## Updating the Data

Edit `occupations.csv` with two columns:

```csv
occupation,ranking
Telemarketer,1
Software Developer,32
Nurse Practitioner,62
```

- **occupation**: Name of the occupation
- **ranking**: Exposure percentile (1-100, where 1 = most exposed)

If your CSV uses different column names, edit lines 22-23 in `index.html`:

```javascript
const NAME_COLUMN = "your_occupation_column";
const RANKING_COLUMN = "your_ranking_column";
```

## Local Testing

To test locally, you need a simple web server (browsers block CSV loading from `file://`). Options:

```bash
# Python 3
python -m http.server 8000

# Then visit http://localhost:8000
```
