# PEARLSKI

PEARLSKI uses architecture-specific CUDA kernels to deliver maximum sustained
hashrate while preserving full Pearl proof-of-work correctness. Mixed NVIDIA
GPU rigs are detected and configured automatically.

## Supported GPUs

- NVIDIA RTX 30 series and A100/A40 (`sm_80` / `sm_86`)
- NVIDIA RTX 40 series, L4 and L40S (`sm_89`)
- NVIDIA H100 and H200 (`sm_90`)
- NVIDIA RTX 50 series (`sm_120`)

## Run

Download the latest Linux archive from **Releases**, then:

```bash
./pearlski-miner --user prl-wallet --worker rig01 --pool pearl.jetskipool.ai:6970
```

PEARLSKI mines on all visible supported GPUs by default.
Select specific GPUs:
with `--gpus 0,2`, or inspect them with `--list-gpus`

## Developer Fee

PEARLSKI has a transparent **1% developer fee**

---
<p align="center"><sub> LICENSED UNDER ANTI-MILITARY LICENSE</sub></p>
