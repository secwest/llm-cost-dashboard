# LLM Cost Dashboard — Inference & Training (Feb 2026)

Interactive visualization of LLM cost trends. Inference cost decline (with microwave-oven energy equivalents) and training cost escalation (with Boeing 777-300ER metal smelting equivalents). Single self-contained HTML file, no build step.

**🔗 Live:** [https://secwest.github.io/llm-cost-dashboard/](https://secwest.github.io/llm-cost-dashboard/)

---

## Sections

### ⚡ Inference Cost

Per-query cost decline from **$0.06** (2022) toward **$0.000001** (2027 est.), with a microwave energy equivalent toggle showing how cheap each query has become in everyday terms.

### ✈ Training Cost × 777

Frontier model training costs expressed as **Boeing 777-300ER metal smelting equivalents**, with sub-views for:

- **Frontier trend** — exponential growth of training budgets
- **Replication cost decline** — how quickly costs drop to reproduce frontier capabilities
- **Equivalence table** — training runs mapped to number of 777 airframes worth of smelting energy

### 📊 Combined Summary

The **"scissors effect"**: inference is commoditizing (costs falling 1000×) while training concentrates (costs rising 1000×). The chart overlays both trends on a single timeline.

---

## Data Sources

- [Epoch AI](https://epochai.org/) — compute trends and training cost estimates
- [Stanford AI Index 2024/2025](https://aiindex.stanford.edu/) — industry benchmarks
- OpenAI pricing history
- DeepSeek technical reports
- NVIDIA hardware roadmaps (H100 → B200 → R100)
- Boeing / Airbus material composition data (aluminium, titanium, composites)

## Tech Stack

| Component | Version | Source |
|-----------|---------|--------|
| React | 18 | cdnjs.cloudflare.com |
| Recharts | 2.7.3 | cdnjs.cloudflare.com |
| Babel standalone | latest | cdnjs.cloudflare.com |
| JetBrains Mono | — | fonts.googleapis.com |
| DM Sans | — | fonts.googleapis.com |

**Zero dependencies to install.** The entire dashboard is a single `index.html` file (~38 KB) that loads everything from CDN. No npm, no bundler, no build step.

## Run Locally

```bash
# Any static file server works
python3 -m http.server 8000
# Then open http://localhost:8000
```

Or just open `index.html` directly in a browser.

## License

[MIT](LICENSE)
