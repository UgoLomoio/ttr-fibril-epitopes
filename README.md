# Native-to-fibril structural remodelling reveals an amyloid-selective transthyretin epitope for AI-guided binder design

Companion repository for the manuscript (npj Structural Biology submission).

Transthyretin (TTR) amyloidosis involves refolding of the native tetramer into cross-β fibrils. Analysing relative solvent accessibility across all 30 patient-derived TTR fibril structures deposited to date, we find that the N-terminal region adjacent to the Cys10 modification hotspot — buried in the native tetramer (mean RSA 0.067 for residues 11–15) — is selectively exposed in every fibril (lowest 0.168). Three BoltzGen/RFAntibody design campaigns generate candidate nanobodies that, under Boltz-2 counter-prediction, engage the Pro11/Met13/Lys15 epitope on fibrils (ipTM 0.72–0.88) while docking at distal surfaces on native states: the epitope is pan-amyloid, not tissue-specific.

## Repository structure

```
├── figures/               All main and supplementary figures (PNG; SVG where available)
├── data/                  All data files generated in this study (see below)
```

## Data files (`data/`)

| File | Content |
|---|---|
| `thermompnn_ssm.csv`, `thermompnn_cataloged.csv` | Saturation-mutagenesis ΔΔG predictions (all 2,413 single mutants; cataloged variants) |
| `structural_metrics.csv` | Per-variant structural metrics |
| `epitope_profiles.csv`, `epitope_positions.json` | Per-variant epitope profiles and positions |
| `rsa_full_assembly_sites.csv`, `fibril_rsa_full_assembly.json`, `wt_tetramer_nterm_rsa.csv` | Full-assembly fibril RSA values (Sander–Roupé reference) and wild-type tetramer N-terminal RSA |
| `rsa_expanded_panel.json` | Expanded 30-structure RSA panel with per-residue values (Tien et al. 2013 maximum-ASA reference) |
| `nterm_pairwise_rmsd.npy`, `nterm_pairwise_rmsd_order.json` | 30×30 pairwise N-terminal RMSD matrix (Å) and structure order |
| `ptm_metrics.csv`, `ptm_nterm_rsa.csv` | Boltz-2 PTM model metrics and N-terminal RSA per model |
| `docking_summary.csv` | Ligand complex-prediction summary |
| `design_fibril_site1.yaml`, `design_f64s_nterm.yaml`, `design_f64s_gate.yaml` | BoltzGen design specifications (fibril-targeted, F64S N-terminal, and gate-region campaigns) |
| `final_nanobody_sequences.json`, `f64s_nanobody_sequences.json`, `f64s_gate_nanobody_sequences.json` | Candidate binder sequences |
| `interface_residues.json`, `f64s_interface_residues.json` | Counter-prediction interface residue contacts |
| `counter_pred_scores.json`, `f64s_counter_pred_scores.json` | Boltz-2 counter-prediction scores (fibrils vs native states) |

## Structural data source

Cryo-EM structures were retrieved from the RCSB PDB (accessed 3 October 2026): native tetramer `1ICT` and the 30 patient-derived fibril structures `6SDZ, 8ADE, 8E7D, 8G9R, 8GBR, 8E7H, 8TDN, 8TDO, 8E7E, 8E7J, 7OB4, 9W9J–9WA2`.

## Software for reproduction.

Analyses were performed using ProteoformAnalyzer (https://github.com/UgoLomoio/proteoform_analyzer), including ThermoMPNN-based stability assessment, structural impact analysis of post-translational modifications and missense mutations, Boltz-2 structure prediction, epitope prediction, BoltzGen-based design, and RFAntibody design. The analysis code, configuration files, candidate sequences, and software versions are provided in the Supplementary Data and will be deposited in a public repository upon publication.

## License

Code is released under the MIT License (see `LICENSE`). Data and figures are provided under the same license for this companion release.

## Citation

If you use these data, please cite the manuscript (citation to be updated upon publication).
