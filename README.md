# ML4SCI DeepLense — GSoC 2026 Evaluation Tests
**Author:** Nikhil Chhokar  
**GitHub:** github.com/nikhilchhokar  
**Email:** nikhilchhokar89@gmail.com  
**Institution:** GTBIT, GGSIPU Delhi (B.Tech IT, 2024–2028)

---

## Results Summary

### Common Test I — Multi-Class Classification
Dataset: no_sub / sphere (CDM) / vort (axion) | 75,000 images | 90:10 split

| Model | Accuracy | Macro AUC |
|---|---|---|
| ResNet-18 | 96.47% | 0.9961 |
| EfficientNet-B3 | 97.72% | 0.9976 |
| **Ensemble** | **97.67%** | **0.9979** |

> Surpasses Prasha et al. 2025 reference (AUC 0.968)

### Specific Test V — Gravitational Lens Finding
Dataset: Real HSC observational images | 1:100+ class imbalance

| Metric | Default (t=0.5) | Optimal (t=0.069) |
|---|---|---|
| AUC | 0.9848 | 0.9848 |
| Sensitivity | 86.15% | **93.85%** |
| Specificity | 98.91% | 97.95% |
| TP / FN | 168 / 27 | 183 / 12 |

### Specific Test VII — Physics-Informed Neural Network
Architecture: LensPINN (EfficientNet + InverseLensLayer)  
Physics: Gravitational lensing equation β⃗ = θ⃗ − α⃗(θ⃗)

| Metric | Value |
|---|---|
| Test Accuracy | 96.35% |
| **Macro AUC** | **0.9951** |
| AUC no_sub | 0.9954 |
| AUC sphere | 0.9921 |
| AUC vort | 0.9980 |

### Specific Test IX — Foundation Model (MAE)
*Running — results will be added*

---

## Proposals Submitted
- DEEPLENSE7: Data Processing Pipeline for the LSST
- DEEPLENSE5: Gravitational Lens Finding
- HumanAI SIRA1: Learning the SIR Model

---

## Related Contributions
PRs to ML4SCI/DeepLense: #166, #151, #148, #144, #136, #130, #129, #122