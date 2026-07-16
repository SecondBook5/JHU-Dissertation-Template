# StageBridge Master's Thesis Workplan

**Branch:** `stagebridge-thesis`  
**Working title:** *StageBridge: Context-Conditioned Residual Transport for Premalignant Epithelial Transitions*  
**Target submission:** August 2026

## Canonical thesis identity

StageBridge is a **context-conditioned residual transport (CCRT)** framework. The final thesis should consistently use the following concepts:

- **receiver-intrinsic transition field:** the progression-associated transition expected from the epithelial receiver state and ordered stage edge;
- **context-residual transition field:** the additional transition associated with typed local sender context;
- **regulatory mediation:** the portion of the context residual mapped through pathway, transcription-factor, or regulon programs;
- **counterfactual context perturbation:** the change in predicted transport after removal or attenuation of a sender state or biological program.

Do not return to the earlier named **self--world** framing. Receiver and context remain technically separate, but CCRT is the thesis-level terminology.

## Central thesis claim

> StageBridge decomposes premalignant epithelial progression into a receiver-intrinsic transition field and a structured context residual. In lung adenocarcinoma precursors, this framework identifies a nonlinear sequence of inflammatory regulatory priming, transcription-factor network collapse before invasion, and later matrix-centered invasive tissue-system rewiring.

## Thesis scope

The completed thesis is centered on the LUAD precursor system:

`Normal -> AAH -> AIS -> MIA -> LUAD`

PanIN is a future cross-tissue generalization test, not a requirement for the master's thesis.

## Chapter map

1. **Introduction**
   - premalignant progression as a tissue-transition problem;
   - cross-sectional single-cell and spatial inference gap;
   - CCRT hypothesis and thesis contributions.
2. **Multimodal LUAD progression data**
   - cohort and stage sequence;
   - snRNA-seq, spatial transcriptomics, WES, HLCA, and LuCA;
   - receiver and sender-context construction;
   - patient-aware splits and biological readouts.
3. **StageBridge methods**
   - receiver-intrinsic field;
   - context residual and regulatory bottleneck;
   - receiver-centered Set Transformer;
   - dual-reference fusion;
   - optimal transport and conditional flow matching;
   - counterfactual context perturbation;
   - ablations and evaluation.
4. **Results**
   - transition-field recovery;
   - contribution of structured context;
   - IL1B-associated inflammatory priming;
   - AAH transcription-factor network expansion;
   - AAH-to-AIS regulatory collapse;
   - MIA-to-LUAD MMP/ECM and tissue-system switch;
   - integrated Prime--Collapse--Switch model.
5. **Discussion and conclusions**
   - computational contribution;
   - biological model;
   - cross-tissue and perturbational validation.

## Result-lock requirements

Before any number is treated as final, record:

1. dataset manifest and checksum;
2. model branch, commit, configuration, and checkpoint;
3. fold, held-out donors, and random seed;
4. exact metric definition and scale;
5. unit of biological analysis;
6. statistical test, covariates, and multiple-testing procedure;
7. source table and plotting script;
8. figure and caption using the result.

## Immediate unresolved items

- Reconcile the two validation-loss and no-niche ablation scales.
- Regenerate every primary metric from the frozen CCRT checkpoint set.
- Verify donor-level folds and absence of patient leakage.
- Recalculate IL1B, immune composition, and proliferation at the donor or sample level.
- Resolve the T-cell percentage discrepancy.
- Recover exact stage-specific TF network statistics and edge lists.
- Confirm the reported FOS--SP1 and FOS--NF-kappaB disruptions.
- Recover the exact MMP identities, directions, cell compartments, and stage contrasts.
- Freeze one output contract for model, residual, counterfactual, and biological outputs.

## Proposed primary figure sequence

1. **Figure 1:** LUAD progression system and StageBridge CCRT overview.
2. **Figure 2:** Multimodal cohort, reference integration, and receiver-centered context construction.
3. **Figure 3:** Transition-field recovery, held-out metrics, baselines, and ablations.
4. **Figure 4:** Receiver-intrinsic field versus context residual and counterfactual context effects.
5. **Figure 5:** Prime -- IL1B-associated inflammatory/stromal niche remodeling in AAH.
6. **Figure 6:** Collapse -- stage-specific TF networks and AAH-to-AIS regulatory bottleneck.
7. **Figure 7:** Switch -- MMP/ECM, vascular, immune-suppressive, and proliferative rewiring in LUAD.
8. **Figure 8:** Integrated Prime--Collapse--Switch model.

## Writing order

1. Freeze the results registry.
2. Finalize the Methods chapter against the implementation.
3. Write Results one figure at a time.
4. Expand the Introduction around the exact computational gap.
5. Complete Discussion after the result language is locked.
6. Finalize abstract, title page, acknowledgments, bibliography, and appendices.
