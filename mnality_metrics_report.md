# Mnality Metrics Report

## Definition Used

Mnality is treated as the number and balance of distinct topology states/components active in the video system.

- **Active M states** = count of distinct detected topology states.
- **Entropy M-eff** = effective number of states, calculated as exp(Shannon entropy).
- **Simpson M-eff** = diversity effective number, calculated as 1 / sum(p²).
- **M uniformity** = Entropy M-eff / Active M.
- **M redundancy** = 1 - M uniformity.
- **Transition tension** = state changes per ordered record step.
- **Triality balance** = normalized entropy after folding states into 3 branches.
- **Nonality balance** = normalized entropy after folding states into 9 branches.
- **M=46 ceiling** = prior Mnality stability reference: active M ≥ 46 is a ceiling breach; effective M below 46 is still sub-ceiling in distributional practice.

## Core Mnality Summary

| dataset                                  | records    |   active_M_states |   entropy_M_eff |   simpson_M_eff |   M_uniformity |   M_redundancy |   transition_tension |   triality_balance_0_to_1 |   nonality_balance_0_to_1 |   M46_active_margin | M46_active_breach   |   M46_eff_stability |
|:-----------------------------------------|:-----------|------------------:|----------------:|----------------:|---------------:|---------------:|---------------------:|--------------------------:|--------------------------:|--------------------:|:--------------------|--------------------:|
| 10 snapshots                             | 10.0000    |                10 |         10      |         10      |         1      |         0      |               1      |                    0.556  |                    0.7718 |                  36 | False               |              0.7826 |
| 100 snapshots                            | 100.0000   |                49 |         41.4104 |         32.6797 |         0.8451 |         0.1549 |               0.4848 |                    0.9764 |                    0.9816 |                  -3 | True                |              0.0998 |
| 7,560 frames / 49 states, frame-weighted | 7,560.0000 |                49 |         42.5215 |         33.122  |         0.8678 |         0.1322 |               0.0064 |                    0.9856 |                    0.9846 |                  -3 | True                |              0.0756 |
| 49 unique states, state-native uniform   | 49.0000    |                49 |         49      |         49      |         1      |         0      |               1      |                    0.9996 |                    0.9981 |                  -3 | True                |              0      |
| 49 unique states, segment-weighted       | 49.0000    |                49 |         42.5215 |         33.122  |         0.8678 |         0.1322 |               1      |                    0.9856 |                    0.9846 |                  -3 | True                |              0.0756 |

## Metric-Weighted Effective Mnality

| dataset                     |   simulon_count_M_eff |   simulon_field_energy_M_eff |   intersection_points_M_eff |   enclosure_total_M_eff |   vascular_total_length_px_M_eff | mean_simulon_count   | mean_field_energy   |   mean_simulon_per_intersection |
|:----------------------------|----------------------:|-----------------------------:|----------------------------:|------------------------:|---------------------------------:|:---------------------|:--------------------|--------------------------------:|
| 10 snapshots                |                7.0904 |                       5.4851 |                      6.8084 |                  9.546  |                           7.6898 | 27,645.1000          | 5,939.4403          |                          1.1981 |
| 100 snapshots               |               33.2512 |                      23.5051 |                     31.9696 |                 43.2013 |                          37.9749 | 25,496.3800          | 5,209.3882          |                          1.1692 |
| 7,560 frames                |               33.5739 |                      23.4298 |                     32.2377 |                 44.4069 |                          38.7763 | 25,770.0443          | 5,298.7066          |                          1.1689 |
| 49 states, segment-weighted |               38.7888 |                      29.8554 |                     37.5248 |                 48.0866 |                          42.2772 | 26,497.3265          | 5,298.9872          |                          1.1598 |

## Interpretation

The 10-snapshot dataset is structurally clean but sparse: it hits 10 distinct states with perfect sample-level uniformity.  
The 100-snapshot dataset already sees all 49 states, but its entropy-effective Mnality is only about 41.41, meaning the full 49-state structure is present but unevenly occupied.  
The full 7,560-frame dataset also has 49 active states and an entropy-effective Mnality of about 42.52, confirming a broad but still plateau-dominated state distribution.  
The 49-state native uniform view is the pure ceiling-breach layer: M-eff = 49.  
The segment-weighted 49-state view equals the full-frame distributional Mnality, because the full video is a time expansion of those 49 visual topology states.

## Charts

- chart_01_effective_mnality_vs_m46.png
- chart_02_active_vs_effective_mnality.png
- chart_03_triality_nonality_balance.png
- chart_04_transition_tension.png
- chart_05_metric_weighted_mnality.png
