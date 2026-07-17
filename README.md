# PEARLSKI Miner

**State-of-the-art CUDA miner for Pearl proof-of-work**

PEARLSKI is powered by precision-tuned CUDA kernels built for maximum performance and sustained hashrate on every compatible NVIDIA GPU

---

## Features

- **Linux, Hive OS, and Windows support**
- **Precision-tuned CUDA kernels** engineered for the highest sustained Pearl hashrate
- **Per-GPU kernel mapping** — applies the optimal tune to every GPU
- **Automatic mixed-rig support** — detects and configures compatible NVIDIA GPUs
- **Flexible multi-GPU control** — mine on all devices or select individual GPUs
- **CMP 170HX compute unlock** — unlocks and tunes restricted FMA throughput

## HiveOS
 
Set a **Custom miner** in your flight sheet
 
| Field | Value |
|---|---|
| Miner name | `pearlski` |
| Installation URL | `https://dl2.jetskipool.ai/pearlski-latest.tar.gz` |
| Wallet and worker template | `%WAL%.%WORKER_NAME%` |
| Pool URL | `pearlski.jetskipool.ai:6970` |
| Extra config arguments | *(optional — e.g. `--gpus 0,2`)* |
 
`%WAL%` expands to the wallet set in the flight sheet and `%WORKER_NAME%` to the rig's worker name, so shares are credited per-rig without any manual editing

## Run
Download the latest Linux/Windows build from the [Releases](../../releases) page, then extract and run:

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
./pearlski-miner --gpus 0,2        # mine on devices 0 and 2 only
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

PEARLSKI has a transparent **2% developer fee**

---

<p align="center"><sub>LICENSED UNDER ANTI-MILITARY LICENSE</sub></p>
