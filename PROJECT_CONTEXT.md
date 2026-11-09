# Project context for Codex and collaborators

## Authoritative assignment
- **Primary specification:** `docs/Entregable1DeepLearningProject_extracted.txt` — full text extraction of the 34-page user-uploaded `Entregable1DeepLearningProject (1).pdf`. Text extraction can distort formulas; use original PDF to check layout and equations.
- `docs/Practica_RNN_extracted.txt` is a **separate RNN practice**, not the final project rubric.
- Deliverable 1: a rigorous state-of-the-art review, exhaustive EDA, and implementation/benchmarking of **exactly three simple Deep Learning baseline architectures** selected from published literature; reproducibility and data-leakage prevention are essential.
- Deliverable 2 (later): expand the benchmark to 10 models.
- Deliverable 3 (later): production and an original model.

## Scope under consideration (not yet finalized)
- Candidate application: **binary image segmentation of screws** in **WDSD** (WEEE Disassembly Screw Dataset), converting screw instance masks into foreground/background masks. Source: https://vcl.iti.gr/dataset/weee-disassembly-screw-dataset/
- Why segmentation: the rubric admits image segmentation but **does not explicitly list object detection or 6D pose estimation** among the allowed task types.
- Potential basic model families listed illustratively in the rubric: simple FCN, basic convolutional encoder-decoder, reduced U-Net. **DO NOT claim they are the selected three until a reproducible literature review establishes their use/frequency as baselines and their nonredundancy.**
- Research beyond scope (for later robotics work): YOLO screw detection, ROBI 6D object pose, Phillips heads, physical screwdriving, RGB-D/CAD-based plate pose. Do not turn those into requirements for this assignment.

## Deliverable 1: compulsory requirements
1. Formal mathematical task definition, dataset licensing/version/provenance, metric(s), practical significance margin delta, independence unit (e.g. scene/image group), and frozen train/val/test split defined **a priori**.
2. EDA with explicit impact on preprocessing, architecture, and leakage risk. For segmentation inspect overlay alignment, empty masks, class pixel counts/background fraction, object sizes, resolutions, illumination, duplicates, and grouping by scene/source.
3. Reproducible literature search: Boolean searches, execution dates and counts, Scopus/WoS/IEEE Xplore where accessible, inclusion/exclusion and quality criteria, PRISMA-style flow, frequency table of simple DL baselines, and articles with verifiable results/DOIs. **Do not invent search counts or access to subscription databases.**
4. Implement exactly 3 literature-derived **simple baselines**, same preprocessing/data splits, same optimization effort, documented hyperparameter search space, learning rates, batch sizes, optimizers, losses, early stopping and code dependencies.
5. Pilot: **at least 5 independent runs per baseline on validation**, report mean/standard deviation/CV, estimate paired-difference variation, prespecify practical difference delta, perform power calculation to determine final run count.
6. Final benchmark: multiple documented seeds (at least 5; 6 if relying on signed-rank tests, or more if required by power analysis), report uncertainty including CI 95%, effect size, run time, model parameter count, per-image analysis and appropriate corrected paired comparisons. Report low power honestly.
7. Hold test set untouched for tuning; final evaluation only after models and hyperparameters are fixed.
8. Package **Jupyter Book report**, end-to-end executable EDA + training + statistical evaluation, dependency lock/list, run configurations, dataset retrieval scripts/instructions, results tables, plots, literature search record.

## Evaluation weighting
- EDA 30%
- Literature review & extraction of three baselines 30%
- Baseline implementations 20%
- Benchmark/statistical inference 20%

## Fairness and hardware
- Hyperparameter tuning can be distributed across different computers **if** budgets/search methods/data/versions are comparable; track device and software differences and ideally recheck tuned configurations on the common target environment.
- Prefer pilot and final performance/latency benchmarks on the same GPU so compute-time comparisons are interpretable. The rubric does not literally mandate identical GPUs.
- No measured runtimes or accuracy numbers have been produced yet. Previous chat estimates are speculative.

## What Codex should do first
1. Read this file and the **entire** authoritative extracted rubric; request the original PDF if mathematical notation is needed.
2. Check dataset license, availability, annotation format and split integrity before committing to WDSD.
3. Create a minimal reproducible repo plan with commands, folder structure, dataset download/prep, EDA notebook, baseline implementations, training and analysis.
4. Avoid generating artificial experimental results, unverifiable paper citations, fake PRISMA counts, or choosing final models before the literature extraction.
