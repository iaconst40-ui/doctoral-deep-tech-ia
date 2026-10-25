# MODEL CARD: FORECASTING VERTICAL INTERNAL BENDING MOMENTS (mu22)
## 1. Model Details
- **Developer:** UNMSM Doctoral Candidate in Deep Technologies.
- **Architecture:** MLP Neural Network via TensorFlow Core layers.
- **Version:** v1.0.0 (Deterministic Production Build).
## 2. Intended Use
- **Primary Uses:** Rapid calculation of ultimate vertical bending moments (`mu22`) in concrete walls.
- **Out-of-Scope:** Rectangular tanks or foundations under non-seismic conditions ($Z \neq 0.45$).
## 3. Factors
- Structural boundaries: Diameter ($2 \leq D \leq 9\text{ m}$) and Height ($2 \leq h_n \leq 8.5\text{ m}$).
## 4. Metrics
- Primary Target: $R^2$ Score. Baseline model performance reached: 0.94833.
## 5. Evaluation Data
- Isolated validation slice containing 20% of the master data array.
## 6. Training Data
- Built over 530 real parametric simulation rows mapped under $Z=0.45$ and $f'c=280\text{ kg/cm}^2$.
## 7. Quantitative Analyses & Ablation Studies
- Full Feature Config: $R^2$ = 0.94833
- Soil Features Dropped: $R^2$ = 0.87002 (Significance P-Value: 0.00000375)
## 8. Ethical Considerations
- Retaining liquid structures contain significant potential energy. Proof calculations under ACI-350 remain mandatory.
## 9. Caveats and Recommendations
- Extrapolation checks show boundary limits degrade if inputs fall outside the training space matrix.
