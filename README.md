# TDA Market Signals
### Detecting topological transitions in financial markets before they occur

> Markets leave topological fingerprints before they break. This repo finds them.

---

## What This Repo Does

Financial markets undergo **topological transitions** before major crises — the shape of return dynamics changes in ways that standard statistical measures miss. This repo builds a pipeline to detect these transitions early.

We reproduce and extend **Gidea & Katz (2018)**, the foundational paper on TDA applied to financial markets, then test their methodology with principled parameter selection.

The pipeline:
1. **Establish baseline** — what does calm market topology look like?
2. **Detect transitions** — how does topology change approaching a crisis?
3. **Build early warning signal** — $L^2$ norm + spectral density, 250 days ahead
4. **Test** — does persistence-based window selection outperform $w = 50$?
5. **Generalize** — does the signal work on TSLA and BTC?

---

## Repository Structure

tda-market-signals/
├── README.md
├── requirements.txt
├── notebooks/
│   ├── 01_topological_baseline.ipynb
│   ├── 02_topological_transitions.ipynb
│   ├── 03_early_warning_signal.ipynb
│   ├── 04_improving_the_pipeline.ipynb
│   └── 05_generalization.ipynb
├── src/
│   ├── init.py
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

- [ ] Notebook 01: Topological baseline — calm market topology
- [ ] Notebook 02: Topological transitions — reproducing Gidea & Katz
- [ ] Notebook 03: Early warning signal — L² norm + spectral density
- [ ] Notebook 04: Testing pipeline improvements — FNN vs d=10, persistence-based w vs w=50
- [ ] Notebook 05: Generalization — TSLA and BTC, 2020 COVID crash
- [ ] src/ modules
- [ ] tests/

---

## References

- Gidea & Katz (2018) — *Topological Data Analysis of Financial Time Series* — [arxiv.org/abs/1703.04385](https://arxiv.org/abs/1703.04385)
- Güzel (2026) — *Persistent Homology of Time Series through Complex Networks* — [arxiv.org/abs/2605.01624](https://arxiv.org/abs/2605.01624)
- Guritanu et al. (2025) — *Topological Machine Learning for Financial Crisis Detection* — [doi.org/10.3390/computers14100408](https://doi.org/10.3390/computers14100408)

---

## Author

**TDA-Gabo**
*You may not see the data, but you can always describe its shape.*