# Postoperative AKI Risk Prediction

A browser-based risk calculator for **acute kidney injury (AKI) after cardiac valve repair surgery**, embedding the random-forest model from our multicentre study (500 trees, 9 preoperative predictors, Platt-calibrated).

## Use online

Once GitHub Pages is enabled (Settings → Pages → Deploy from a branch → main → / (root)):

**https://tianqiangsheng-a.github.io/postoperative-aki-risk-prediction/**

All computation runs locally in the visitor's browser — no data are transmitted or stored.

## Files

- `index.html` — calculator UI (English / 中文)
- `model.part1.js` … `model.part24.js` — model data (gzip-compressed binary forest, base64-encoded and split into 24 chunks for reliable delivery) loaded in order by `index.html`

The calculator is also distributed as a standalone single HTML file (see releases / manuscript supplementary material), which can be opened offline or hosted on any web server as-is.

## Model

- Predictors: age, neutrophil count, plasma D-dimer, fibrinogen, NT-proBNP, hs-cTnI, γ-GT, serum uric acid, serum creatinine
- Internal test AUC 0.770 (Brier 0.176); external two-centre validation AUC 0.732 (95% CI 0.647–0.813, Brier 0.174)
- Youden-derived risk threshold: 0.29 (sensitivity 0.76–0.79, NPV 0.86–0.88)

*For research and educational use only — not a substitute for clinical judgement.*
