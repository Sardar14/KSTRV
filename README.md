# KSTR — NEWS

## [2.0.0] - 2025-09-06
**Release name:** KSTRV2 (Kurdish Scene Text Recognition v2.0)

### Changed
- **Unicode normalization:** All annotations standardized to a single, consistent Unicode encoding to remove visually identical but distinct code points.
- **Synthetic subset balance:** Replaced a small set of overly hard synthetic samples with easy/medium ones to better match realistic difficulty while keeping diversity.
- **Annotation quality:** Corrected minor spelling and label errors found during validation.

### Notes
- **Do not mix** KSTRV1 and KSTRV2 when training/evaluating; report results separately.
- Ensure your data pipeline preserves the normalized Unicode; avoid unintended re-normalization.

### Links
- Dataset record (concept DOI): https://doi.org/10.5281/zenodo.15038953
- Descriptive article (Data in Brief, 2025): https://doi.org/10.1016/j.dib.2025.111648

---

## [1.0.0] - 2025-03-17
Initial public release (KSTRV1): 1,420 natural scene images, 19,872 cropped words (Kurdish—Sorani/Badini—Arabic, English) + 20,000 synthetic instances.
