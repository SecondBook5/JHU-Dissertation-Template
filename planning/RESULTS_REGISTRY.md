# StageBridge Thesis Results Registry

This registry separates the current biological narrative from final thesis-ready statistics. A result is **locked** only after it is regenerated from the frozen CCRT analysis and linked to a source table, script, model version, and unit of analysis.

| Result | Current working value or interpretation | Status | Required action |
|---|---|---|---|
| Donors | 25 | Working | Confirm from frozen cohort manifest |
| Single-cell / single-nucleus scale | Approximately 1.4 million profiles across study and integrated resources | Working | Report modality-specific counts clearly |
| Spatial scale | Approximately 639,816 observations | Working | Confirm retained spots and sample breakdown |
| Ordered stages | Normal, AAH, AIS, MIA, LUAD | Stable | Preserve stage-resolved modeling |
| Normal-to-preinvasive drift alignment | `0.964 +/- 0.008` | High-priority verification | Regenerate from frozen CCRT checkpoints |
| Overall drift alignment | `0.309 +/- 0.081` | High-priority verification | Regenerate with exact metric definition |
| Full-model validation loss | Poster registry near `0.00356`; older tables use another scale | Conflicted | Reconcile metric, normalization, and model version |
| No-context ablation | Poster registry reports modest degradation; older draft reports much larger degradation | Conflicted | Do not quote until regenerated in one evaluation pipeline |
| Gating ablation | Working registry reports degradation after gate removal | Working | Recover fold-level values and confidence interval |
| Dual-reference contribution | HLCA-only and LuCA-only models underperform full fusion | Working | Recompute under identical folds and seeds |
| Baseline comparison | StageBridge outperformed pooling, DeepSets, flat Set Transformer, and GraphSAGE baselines | Working | Re-run all baselines under common output contract |
| IL1B-positive observations | Normal approximately 31%, preinvasive approximately 49%, invasive approximately 51% | Biological working result | Recalculate at donor/sample level |
| IL1B fold change | Approximately 2.8-fold increase | Biological working result | Confirm definition and donor-aware test |
| IL1B stage association | Working summary reports Spearman rho approximately 0.336 | Provisional | Confirm independent unit and p-value |
| Transition-region IL1B | Working summary reports approximately 0.35 versus 0.28 | Provisional | Recover region definition and donor-aware test |
| T-cell composition | Working values 15.9%, 5.7%, 10.9% for Normal, preinvasive, invasive | Conflicted | Resolve 57% versus 64% reduction discrepancy |
| Macrophage composition | Working values 11.0%, 5.0%, 6.7% | Provisional | Recalculate at donor/sample level |
| Fibroblast composition | Working values 24.8%, 10.7%, 15.9% | Provisional | Recalculate at donor/sample level |
| Proliferation | Approximately 7.1% Normal to 25.7% invasive; 3.6-fold increase | Biological working result | Confirm scoring threshold and donor-level model |
| Context dimension associated with TGF-beta | Working correlation approximately 0.18 | Provisional | Map old latent dimension to frozen CCRT output |
| Context dimension associated with TNF-alpha/NF-kappaB | Working correlation approximately 0.12 | Provisional | Map old latent dimension to frozen CCRT output |
| TF network sequence | Expansion in AAH, sharp contraction in AIS, sparse AIS/MIA state, re-expansion in LUAD | Central narrative | Recover exact network statistics from source output |
| AAH-to-AIS regulatory bottleneck | Major loss of TF co-regulation before invasion | Central narrative | Add donor-aware robustness and threshold sensitivity |
| FOS--SP1 disruption | Previously identified lost coordination | Provisional | Confirm exact edge and direction |
| FOS--NF-kappaB disruption | Previously identified lost coordination | Provisional | Confirm regulator definition and exact edge |
| MMP / ECM transition | Matrix program changes direction and composition around MIA-to-LUAD | Central narrative | Recover exact MMPs, compartments, effects, and tests |
| Vascular remodeling | Angiogenic / vascular adaptation contributes to invasive switch | Working narrative | Lock exact pathways and source populations |
| Immune suppression | Treg / dysfunctional T-cell programs contribute to invasive switch | Working narrative | Lock markers, cell states, and donor-level statistics |
| Prime--Collapse--Switch | Prime in AAH, collapse at AAH-to-AIS, switch at MIA-to-LUAD | Thesis-level synthesis | Support each phase with one primary figure and one result table |

## Canonical interpretation

StageBridge should not be described as showing that niche context determines all progression. The intended interpretation is:

> Epithelial receiver state defines a strong baseline transition field, while local inflammatory, stromal, immune, vascular, and matrix contexts contribute stage-specific residual effects that alter progression-associated transport.

## Evidence lock order

1. Cohort manifest and patient-aware folds.
2. Frozen CCRT model and output contract.
3. Transition metrics and architectural ablations.
4. IL1B, composition, and proliferation.
5. Stage-specific TF networks and AAH-to-AIS edge turnover.
6. MMP/ECM identities and MIA-to-LUAD direction change.
7. Integrated figure and final abstract.
