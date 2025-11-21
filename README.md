# Private 5G Network Threat Detection — Open5GS + srsRAN + AWS GuardDuty

**Master's Thesis / Project**  
This repository contains the implementation, configuration and reproduction instructions for a simulated private 5G network used to evaluate AWS GuardDuty threat detection. The original thesis PDF is in `docs/Ammad-Masters-Thesis.pdf`. :contentReference[oaicite:2]{index=2}

## Quick links
- Full thesis: `docs/Ammad-Masters-Thesis.pdf`
- Setup guide: `docs/SETUP.md`
- Open5GS configs: `configs/open5gs/`
- srsRAN configs: `configs/srsran/`
- AWS scripts & Cloud formation: `aws/`
- Diagrams: `diagrams/`

## What this project demonstrates
- Deploy a simulated private 5G core (Open5GS) + RAN (srsRAN) in AWS.
- Generate attack vectors (nmap, SSH brute force, DNS exfiltration) and observe GuardDuty findings.
- Provide reproducible steps and configuration to replicate experiments described in the thesis. :contentReference[oaicite:3]{index=3}

## Quick start (local)
1. Read `docs/SETUP.md` for step-by-step environment preparation.
2. Review `configs/` for example config snippets used in the experiment.
3. Use VM or EC2 instances described in the thesis to run the simulation. :contentReference[oaicite:4]{index=4}

## Contact
- Your Name: Ammaduddinbajwa702@gmail.com
- LinkedIn: https://www.linkedin.com/in/ammaduddinbajwa

