# Deep Learning — Entregable 1

> **Actualización (10 nov 2026):** el repositorio principal de experimentos es [BESADAJ/wdsd-segmentacion-tornillos-entregable-1](https://github.com/BESADAJ/wdsd-segmentacion-tornillos-entregable-1). Este repositorio contiene el contexto y la rúbrica. [Leer el historial recuperable de nuestra conversación para Codex](CHATGPT_HISTORIAL_DISPONIBLE.md) (**parcial**, no transcripción íntegra). La integración de GitHub no permitió escribir en BESADAJ (403), por lo que se dejó aquí.


Academic project: **state of the art, exploratory data analysis (EDA), and rigorous benchmarking of three *simple* Deep Learning baselines**.

## Start here
- [**CODEX_LEER_CONVERSACION_COMPLETA.md**](CODEX_LEER_CONVERSACION_COMPLETA.md) — **priority instruction to open the shared chat in a browser and extract the literal conversation** (pending execution in Codex).
- [PROJECT_CONTEXT.md](PROJECT_CONTEXT.md) — shared project decisions and rubric checklist for Codex.
- [AGENTS.md](AGENTS.md) — Codex instructions.
- [Full-text extraction of assignment (34 pages)](docs/Entregable1DeepLearningProject_extracted.txt) — official Deliverable 1 rubric, extracted from the PDF.
- [RNN practice (separate assignment)](docs/Practica_RNN_extracted.txt) — not part of Deliverable 1.

**Original PDFs:** The above text versions were uploaded first for immediate searchability. The original PDF binaries are **not yet in the repository**; attach them to Codex or add them under `docs/` to preserve layout/equations.

## Proposed scope — pending literature confirmation
Binary image segmentation of screws with [WDSD](https://vcl.iti.gr/dataset/weee-disassembly-screw-dataset/). The rubric permits **image segmentation**; it does not explicitly admit stand-alone object detection or 6D pose estimation.

Possible *candidate* baseline families named in the rubric are simple FCN, basic convolutional encoder–decoder, and reduced U-Net. These are **not yet validated as the final selected architectures**; choice must be supported by a reproducible literature search.

## Primary deliverable
A Jupyter Book report, full reproducible code, EDA, literature search methodology + PRISMA accounting, pilot and final repeated trainings, fair hyperparameter selection, statistical comparisons with CIs/effect sizes, and frozen data splits.

Rubric weights: EDA 30%, literature review 30%, implementation 20%, statistical benchmark 20%.

## Codex kickoff
Read `PROJECT_CONTEXT.md`, `AGENTS.md`, and the full 34-page assignment extract. Then audit WDSD availability/license and propose a minimal implementation plan aligned with the specification. Do not invent results, bibliography entries, or PRISMA counts.

> **Note:** This repository is **public**. Do not commit private data, secrets, personal documents, or redistributable datasets without checking their licenses.
