# Changelog

All notable changes to the **Emuuriimu** font project will be documented in this file.

## [0.8.0] - 2024-06-06
### Added
- **Better Syllable Parser:** Added logic to identify when a consonant cluster (like `ks`, `mp`, `rt`) needs to be split across two syllables if a vowel follows (e.g., `syök-syy`).
- **Nasal Assimilation Support:** Added `nt` and `rj` clusters to the logic pool.

### Fixed
- **V-CV Syllabification:** Implemented the V-CV rule. Single consonants between vowels now correctly anchor as Initials to the following vowel (e.g., fixing the `em-uu` vs `e-muu` collision).
- **Inter-syllabic Spacing:** Resolved collisions between Vowels and Initial Consonants using GPOS `kern` lookups. Syllables now have a consistent gap.
- **Metric Proportions:** Standardized glyph widths to a 1:2 ratio (Consonants 880 / Vowels 1760) to ensure the grid remains consistent.
- **Normalized Space Width:** Re-calibrated the space key width to 1760 units (equal to a standard Vowel block) for consistent word delimitation.

---

## [0.1.0] - 2024-06-01
### Added
- Initial release of the rune-based font system.
- Basic mapping for identified Finnish letters.
- Support for Ligature, docking inside syllables.