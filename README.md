# Shift-Aware, Leakage-Audited One-Class Intrusion Detection (NF-ToN-IoT-v3)

Authors: Amina Iqrar, Abeer Zahra (FAST-NUCES, Islamabad)

## What this is
Benign-only detector (denoising MLP autoencoder + RBF OC-SVM, split-conformal
thresholds at 0.1%, 1%, 5%), compared with Isolation Forest, a raw-feature
OC-SVM and a supervised LightGBM reference. Held-out family: DoS + DDoS.
Includes drift monitors, abstain/recalibrate, and a leakage audit (L1-L3).

## Data
NF-ToN-IoT-v3, DOI 10.48610/44d7c5e. Not included here. Download it and
create the working sample as described in the paper (sampling seed 2026).

## Files
- common.py: preprocessing, splits, conformal threshold, evaluation, audit checks
- notebooks (.ipynb): run in order; each starts by mounting Google Drive
- results: per-seed result CSVs and monitor outputs
- environment.txt: software versions

## Reproduce
Seeds 13, 23, 37, 51, 73. Google Colab CPU, Python 3.13.
Results are benchmark-proxy findings, not proof of real zero-day protection.
