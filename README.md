# TDA Market Signals
### Detecting topological transitions in financial markets before they occur

> Markets leave topological fingerprints before they break. This repo reproduces and extends their methodology.

---

## What This Repo Does

Financial markets undergo what are called *topological transitions*. Standard statistics describe how much markets move. TDA describes how they move — detecting the emergence of correlated structure across indices before a crash is visible in prices.

We reproduce and extend **Gidea & Katz (2018)**, the foundational paper on TDA applied to financial markets, then test their methodology with principled parameter selection.

The pipeline:
1. **Establish baseline** — what does calm market topology look like?
2. **Detect transitions** — how does topology change approaching a crisis?
3. **Build early warning signal** — $L^2$ norm + spectral density, 250 days ahead
4. **Test** — does persistence-based window selection outperform $w = 50$?

---

## Repository Structure

tda-market-signals/
├── README.md
├── requirements.txt
├── notebooks/
│   ├── 01_market_data.ipynb
│   ├── 02_topological_transitions.ipynb
│   ├── 03_early_warning_signal.ipynb
│   └── 04_parameter_adjustment.ipynb
├── src/
│   ├── __init__.py
│   ├── rolling.py       ← rolling window TDA
│   ├── signals.py       ← L² norm, spectral density
│   └── visualization.py ← financial TDA plots
├── data/
└── tests/
└── test_signals.py

---

---

## Installation

```bash
git clone https://github.com/TDA-Gabo/tda-market-signals.git
cd tda-market-signals
pip install -r requirements.txt
```

---

## Roadmap

- [ ] Notebook 01: Market Data — collection data
- [ ] Notebook 02: Topological transitions — first view of topological transitions
- [ ] Notebook 03: Early warning signal — L² norm + spectral density for warning signals
- [ ] Notebook 04: Parameter Adjustment — persistence-based w vs w=50
- [ ] src/ modules
- [ ] tests/

---

## References

- Gidea & Katz (2018) — *Topological Data Analysis of Financial Time Series* — [arxiv.org/abs/1703.04385](https://arxiv.org/abs/1703.04385)

---

## Author

**TDA-Gabo**
*You may not see the data, but you can always describe its shape.*