# Insurance_claim_prediction

Forecast claim losses and claim likelihood for auto insurance using modern ML with a two‑step pipeline.
Targets: LC (Loss Cost per Exposure Unit), HALC (Historically Adjusted Loss Cost), and CS (Claim Status).


- Best results (validation): CS ROC‑AUC 0.849, LC RMSE 640.87, HALC RMSE 1172.55 using a two‑step model: XGBoost classifier for CS, then XGBoost regressors for LC/HALC on rows predicted as claims.
- Why two‑step: LC and HALC are zero‑inflated and heavy‑tailed. Separating “will there be a claim?” from “how big is the claim?” reduces error and improves stability.

