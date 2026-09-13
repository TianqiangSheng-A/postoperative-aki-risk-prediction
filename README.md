# Postoperative AKI Risk Prediction

A single-file, browser-based risk calculator for **acute kidney injury (AKI) after cardiac valve repair surgery**, embedding the random-forest model from our multicentre study (500 trees, 9 preoperative predictors, Platt-calibrated).

## Use online

Once GitHub Pages is enabled (Settings → Pages → Deploy from a branch → main → / (root)):

**https://tianqiangsheng-a.github.io/postoperative-aki-risk-prediction/**

All computation runs locally in the visitor's browser — no data are transmitted or stored.

## Files

- `index.html` — calculator UI (English/中文)
- `model.part1.js`, `model.part2.js`, `model.part3.js` — embedded model data loaded by `index.html`

The UI together with the model parts can also be downloaded and opened offline, or hosted on any web server as-is.

## Model

- Predictors: age, neutrophil count, plasma D-dimer, fibrinogen, NT-proBNP, hs-cTnI, γ-GT, serum uric acid, serum creatinine
- Internal test AUC 0.770 (Brier 0.176); external two-centre validation AUC 0.732 (95% CI 0.647–0.813, Brier 0.174)
- Youden-derived risk threshold: 0.29 (sensitivity 0.76–0.79, NPV 0.86–0.88)

*For research and educational use only — not a substitute for clinical judgement.*
