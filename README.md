# Privacy-Preserving Collaborative Training

## Overview
A **federated learning** prototype for **privacy-preserving collaborative model training**.  
Supports **MPC** for secure aggregation and an optional **FHE** PoC for encrypted inference.  
*(Beta: local 3-party simulation.)*

---

## Architecture
- **Parties A/B/C:** Hold private datasets in separate containers
- **Coordinator:** Launches MPC protocol, aggregates model parameters
- **Evaluator:** Compares MPC-trained model accuracy vs plaintext baseline
- **Optional:** Encrypted inference demo using FHE

---

## Features
- [x] 3-party secure aggregation via MP-SPDZ / SecretFlow
- [x] Accuracy delta **<2%** vs plaintext baseline
- [ ] Encrypted threshold inference via FHE *(planned)*
- [ ] Federated multi-round training *(planned)*

---

## Tech Stack
**Languages:** Python  
**Frameworks:** MP-SPDZ, SecretFlow, OpenFHE  
**Tools:** Docker, PyTorch

---

## Quickstart

    # Clone repository
    git clone https://github.com/<your-username>/privacy-preserving-collab-training.git
    cd privacy-preserving-collab-training

    # Build and start containers
    docker compose up -d

    # Run secure aggregation demo
    python scripts/run_secure_agg.py --parties 3 --task logistic_regression

    # Evaluate accuracy vs plaintext baseline
    python scripts/eval.py --compare plaintext

---

## Status & Roadmap
- [x] 3-party secure aggregation (Beta)
- [x] Accuracy evaluation script
- [ ] FHE encrypted inference PoC *(planned)*
- [ ] Federated multi-round training *(planned)*
- [ ] Interactive dashboard *(planned)*

---

## License
MIT
