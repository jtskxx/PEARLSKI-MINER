# PEARLSKI Miner

**A high-performance CUDA miner for Pearl proof-of-work**

PEARLSKI uses architecture-specific CUDA kernels to deliver maximum sustained hashrate while preserving full Pearl proof-of-work correctness 
Mixed NVIDIA GPU rigs are detected and configured automatically

---

## Supported GPUs

| Architecture | Compute capability | Example cards |
|---|---|---|
| Ampere | `sm_80` / `sm_86` | RTX 30 series, A100, A40 |
| Ada Lovelace | `sm_89` | RTX 40 series, L4, L40S |
| Hopper | `sm_90` | H100, H200 |
| Blackwell | `sm_120` | RTX 50 series |


## Run
Download the latest Linux archive from the [Releases](../../releases) page, then extract and run:

```bash
./pearlski-miner --user prl-wallet --worker rig01 --pool pearlski.jetskipool.ai:6970
```

PEARLSKI mines on **all visible supported GPUs by default**

### Pools

PEARLSKI can mine on any pool just point `--pool` at the endpoint you want

| Pool | Endpoint | Website |
|---|---|---|
| PEARLSKI pool | `pearlski.jetskipool.ai:6970` | [pearl.jetskipool.ai](https://pearl.jetskipool.ai) |

```bash
# Mining on the PEARLSKI pool
./pearlski-miner --user prl-wallet --worker rig01 --pool pearlski.jetskipool.ai:6970
```

### Selecting GPUs

```bash
./pearlski-miner --list-gpus            # inspect detected devices
./pearlski-miner --gpus 0,2 ...         # mine on devices 0 and 2 only
```

## Options

| Flag | Description |
|---|---|
| `--user <wallet>` | Pearl wallet address to credit |
| `--worker <name>` | Worker/rig identifier reported to the pool |
| `--pool <host:port>` | Pool endpoint |
| `--gpus <ids>` | Comma-separated device IDs (default: all supported) |
| `--list-gpus` | Print detected devices and exit |

## Developer Fee

PEARLSKI has a transparent **1% developer fee**

---

<p align="center"><sub>LICENSED UNDER ANTI-MILITARY LICENSE</sub></p>
