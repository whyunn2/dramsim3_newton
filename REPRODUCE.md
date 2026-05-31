# Newton Reproduction Guide

## Target Paper

Fill in the paper title, authors, venue, year, and link before implementing the
paper-specific model.

## Baseline

- Upstream repository: <https://github.com/umd-memsys/DRAMsim3>
- Upstream commit: `29817593b3389f1337235d63cac515024ab8fd6e`
- Baseline tag in this repository: `dramsim3-baseline`

## Build

```bash
mkdir build
cd build
cmake ..
make -j4
```

## Baseline Smoke Test

```bash
./build/dramsim3main configs/DDR4_8Gb_x8_3200.ini --stream random -c 100000
```

## Experiment Checklist

Document each reproduced figure or table with:

1. The configuration and workload inputs.
2. The exact execution command.
3. The expected output files.
4. The script used to generate the final result.
5. Any modeling assumptions or known deviations from the paper.

Large traces and raw simulator outputs should remain outside Git. Commit small
configuration files, scripts, and the minimal processed data required to
regenerate final plots.
