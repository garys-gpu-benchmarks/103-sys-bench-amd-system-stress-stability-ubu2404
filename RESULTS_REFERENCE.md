# Results: 103 CPU + System Stress (Baseline Health)

**Main goal:** Analyze thermal and power under CPU stress-ng and rocBLAS load  
**Tools:** Run stress-ng --cpu, rocblas-bench, amd-smi metric, and sysfs power1_average

Reference results measured by the maintainer on the system shown in each section (generator TEMPLATE_00_141 · recorded 2026-11-14). Your own runs write `results/RESULTS_ACTUAL.md` in the same format.

> Smoke runs use deliberately small sizes. They check that the workload installs and runs end to end; their numbers are not performance results. Baseline and extended are.

<!-- profile:smoke -->
## smoke

- **System:** 1× AMD Instinct MI300X VF (196288 MB) · INTEL(R) XEON(R) PLATINUM 8568Y+ · Ubuntu 24.04.5 LTS · kernel 6.8.0-147-generic · driver 7.1.9.31600000
- **Run:** 2026-11-14T10:50:27Z · status **N/A-EXPECTED** (exit 0)
- **Time (mm:ss):** setup 03:44 · benchmark 00:13 · whole run 04:06
- **Source:** run 103_20261114_105027
- **Command:** `bash run_benchmark.sh --smoke --num-threads 16 --cpu-load-percent 50 --gpu-load-percent 50 --temp-threshold 100 --power-threshold 1000 --duration 5 --poll-interval 1`

| # | Metric | Result |
|---|---|---|
| 1 | Peak GPU junction temperature (peak_gpu_junction_temp_c) | 63.0 |
| 2 | Sustained GPU power (sustained_gpu_power_w) | 693.25 |
| 3 | Uncorrectable ECC errors, RAS counter delta (ras_uncorrectable_ecc_delta_count) | 0.0 |
| 4 | Thermal throttle events (thermal_throttle_event_count) | na (expected: throttle counter not exposed) |
<!-- /profile:smoke -->
