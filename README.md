Kurdish Scene Text Recognition Version 2.0 (KSTRV2) Dataset
Creators
Jacksi, Karwan (Supervisor)1
ORCID icon
 
Salih, Sardar (Annotator)2
ORCID icon
Description
KSTRV2 (Kurdish STR) Version 2 
KSTRV2 is a large-scale dataset developed for Kurdish Scene Text Recognition (KSTR), addressing the scarcity of resources for non-Latin script like Kurdish. It includes 1,420 real-world scene images and 19,872 extracted word-level samples across Kurdish (Sorani and Badini dialects), Arabic, and English. To expand coverage and improve generalizability, the dataset is augmented with 20,000 synthetic text examples, crafted with diverse typography, multi-angle orientations, simulated distortions, and intricate background textures. This synthesis enhances the dataset’s capacity to handle real-world variability, supporting robust training for text recognition systems in underrepresented languages.

KSTRV2 — Release Notes (September 2025)
Overview

KSTRV2 is an updated release of the Kurdish Scene Text Recognition dataset. It standardizes text encodings, fixes minor annotation issues, and rebalances a small slice of synthetic samples to better reflect realistic difficulty. Use KSTRV2 for any new training or benchmarking; results based on KSTRV1 are not directly comparable.

Dataset record (DOI): https://doi.org/10.5281/zenodo.15038953 (Zenodo) zenodo.org
Article describing KSTRV1: “KSTRV1: A scene text recognition dataset for central Kurdish (Arabic-Based) script,” Data in Brief, 2025. https://www.sciencedirect.com/science/article/pii/S2352340925003786 
Github Link : link
What’s new in v2.0
Unified Unicode encoding for annotations
Some visually identical characters had different code points due to mixed dictionary sources. All annotations are now standardized to a single encoding scheme to remove ambiguity and improve model robustness and reproducibility.
 Rebalanced synthetic subset difficulty
A small subset of synthetic word images that was overly complex has been replaced with easy-to-medium complexity images. The goal is to keep diversity while making the training and eval difficulty more representative of real scenes.
Annotation quality fixes
Minor spelling and labeling errors identified during validation were corrected.
Release readiness
With these changes, KSTRV2 is cleaner and more consistent, ready for both model development and standardized benchmarking.
Recommendation
Please migrate to KSTRV2 for all new work; KSTRV1 contains known inconsistencies that are resolved here.
Compatibility & migration notes
Do not mix versions in training or evaluation. Report results on KSTRV1 and KSTRV2 separately to avoid confounding from the encoding and labeling changes.
Unicode handling: ensure your preprocessing preserves the dataset’s normalized encoding; disable any unintended re-normalization that could remap code points and break label alignment. (Change motivated by the v2 standardization.)
Synthetic curriculum: if you used difficulty-based sampling on v1, re-tune sampling weights given the rebalanced synthetic subset.
Dataset scope (context)
KSTR includes 1,420 natural scene images and 19,872 cropped word samples across Kurdish (Sorani and Badini), Arabic, and English, plus 20,000 synthetic instances—details in the dataset record and paper. zenodo.org 

How to cite

 Dataset (specific version once v2 is public):
Kurdish Scene Text Recognition (KSTR), Version 2.0. Zenodo. DOI: 10.5281/zenodo.15038953 (link resolves to the latest version; please use the versioned DOI shown on the Zenodo “Versions” panel once v2 is live).
Article:
Salih, S. O., & Jacksi, K. (2025). KSTRV1: A scene text recognition dataset for central Kurdish (Arabic-Based) script. Data in Brief.
License
CC BY 4.0. You may reuse and redistribute with attribution. zenodo.org

Changelog (Keep-a-Changelog style)
Changed: Standardized Unicode encoding across all annotations.
Changed: Rebalanced a small synthetic subset to easy/medium difficulty.
Fixed: Minor spelling and labeling errors.
Note: KSTRV1 is deprecated for new experiments.
