MDP-ZKP-MCPS: Modified Differential Privacy Composition with Zero-Knowledge Proofs for Medical Cyber-Physical Systems
 Overview
This repository contains the implementation of the MDP-ZKP framework, a novel approach combining Differential Privacy with Zero-Knowledge Proofs for privacy-preserving medical data analysis in distributed healthcare environments.


 Prerequisites
- Python 3.10+
- MIMIC-III dataset access (requires credentialing)
- 8GB+ RAM recommended
 Installation

Data Preparation
Obtain MIMIC-III credentials from PhysioNet

Run data preprocessing:

python data/preprocess_mimic.py --mimic_path /path/to/mimic/data --output data/processed/

Running Experiments
Baseline Differential Privacy

python experiments/run_baseline_dp.py --config config/experiment_params.yaml
Full MDP-ZKP Pipeline

python experiments/run_mdp_zkp_full.py --config config/experiment_params.yaml --nodes 5 --iterations 50
RL-based Privacy Adjustment


python experiments/run_rl_agent.py --config config/experiment_params.yaml --episodes 100
Generate All Figures
jupyter notebook experiments/plot_generation.ipynb

Reproducing Results
All experiments are seeded for reproducibility. Key results include:

60% reduction in privacy budget exhaustion

64% lower mean squared error

57ms per-query computation time

98% verification success rate under noise


