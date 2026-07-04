# Simulation Relativity Metrics from Mnality

## Definition Used

This report treats **Mnality** as the effective dimensional reference frame of the visual topology system.

Let:

- `C_M = 46`, the prior Mnality ceiling reference.
- `M_eff = exp(H)`, the entropy-effective Mnality from the Mnality report.
- `β_M = M_eff / C_M`, the M-frame velocity / ceiling pressure.
- `γ_M = 1 / sqrt(1 - β_M²)` for sub-ceiling systems.
- For `β_M > 1`, γ becomes imaginary; this is labeled a **super-ceiling imaginary** regime.

Additional Simulation Relativity metrics:

- **Proper-time ratio**: `τ/T = 1/γ_M`.
- **Simulation mass density**: mean Simulons per entropy-effective M.
- **Field energy density**: mean Simulon field energy per entropy-effective M.
- **Intersection curvature**: mean intersection points per entropy-effective M.
- **Enclosure curvature**: mean enclosed cells per entropy-effective M.
- **Vascular flux**: mean vein+artery length per entropy-effective M.
- **Arterial flux**: artery-weighted vascular flux per entropy-effective M.
- **Plateau inertia**: repetition-weighted stability of the M-frame.
- **M-strain index**: structural M=46 breach plus near-ceiling distribution pressure.

## Compact Metrics

| dataset                                | records    |   active_M_states |   entropy_M_eff |   M_beta_eff | M_gamma_real   |   M_gamma_imaginary_magnitude | gamma_regime            | proper_time_ratio_tau_over_T   | simulation_mass_density_simulons_per_Meff   |   field_energy_density_per_Meff | intersection_curvature_per_Meff   |   enclosure_curvature_per_Meff | vascular_flux_px_per_Meff   |   plateau_inertia |   M_strain_index |
|:---------------------------------------|:-----------|------------------:|----------------:|-------------:|:---------------|------------------------------:|:------------------------|:-------------------------------|:--------------------------------------------|--------------------------------:|:----------------------------------|-------------------------------:|:----------------------------|------------------:|-----------------:|
| 10 snapshots                           | 10.0000    |                10 |         10      |       0.2174 | 1.0245         |                        0      | sub-ceiling real        | 0.9761                         | 2,764.5100                                  |                         593.944 | 2,599.8400                        |                       164.67   | 10,768.0100                 |            0      |           0      |
| 100 snapshots                          | 100.0000   |                49 |         41.4104 |       0.9002 | 2.2966         |                        0      | sub-ceiling real        | 0.4354                         | 615.6997                                    |                         125.799 | 574.8858                          |                        40.8139 | 2,582.5816                  |            1.0513 |           0.1154 |
| 7,560 frames / 49 states               | 7,560.0000 |                49 |         42.5215 |       0.9244 | 2.6214         |                        0      | sub-ceiling real        | 0.3815                         | 606.0477                                    |                         124.612 | 566.1304                          |                        39.9173 | 2,523.1364                  |          153.306  |           0.1396 |
| 49 unique states, state-native uniform | 49.0000    |                49 |         49      |       1.0652 |                |                        2.7248 | super-ceiling imaginary |                                | 540.7618                                    |                         108.143 | 504.7855                          |                        35.9763 | 2,312.9679                  |            0      |           0.2804 |
| 49 unique states, segment-weighted     | 49.0000    |                49 |         42.5215 |       0.9244 | 2.6214         |                        0      | sub-ceiling real        | 0.3815                         | 606.0477                                    |                         124.612 | 566.1304                          |                        39.9173 | 2,523.1364                  |            0      |           0.1396 |

## Reading

The **10-snapshot set** is safely sub-ceiling: `β_M = 0.2174`, with a real gamma of about `1.0245`. It behaves like a sparse but clean observer frame.

The **100-snapshot set** is structurally over-ceiling because it sees 49 active states, but its effective M stays below the ceiling: `M_eff = 41.4104`, `β_M = 0.9002`, and `γ_M = 2.2950`. This is a high-dilation Mnality frame.

The **7,560-frame set** is the most important Simulation Relativity frame: it has 49 active states but an effective M of `42.5215`, giving `β_M = 0.9244` and `γ_M = 2.6238`. Because transition tension is very low, it has extremely high plateau inertia: the system is not flickering randomly; it is holding long relativistic topology plateaus.

The **49-state native uniform layer** is the pure super-ceiling state: `M_eff = 49`, so `β_M = 1.0652`. Its gamma is imaginary, meaning it is not dynamically stable under the M=46 ceiling unless it is projected back through segment weights.

The **49-state segment-weighted layer** matches the full-frame distributional Mnality and therefore restores the real sub-ceiling gamma frame.

## Charts

- chart_01_m_beta_gamma.png
- chart_02_density_curvature_metrics.png
- chart_03_plateau_inertia.png
- chart_04_vascular_arterial_flux.png
- chart_05_m_strain_index.png
